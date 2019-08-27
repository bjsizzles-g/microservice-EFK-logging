FROM fluent/fluentd:v1.4.2-2.0

USER root
RUN gem install fluent-plugin-elasticsearch
USER fluent
WORKDIR /home/fluent
ENV PATH /home/fluent/.gem/ruby/2.2.0/bin:$PATH

EXPOSE 24284
VOLUME /fluentd/log

CMD fluentd -c /fluentd/etc/$FLUENTD_CONF -p /fluentd/plugins $FLUENTD_OPT