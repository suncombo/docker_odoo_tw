FROM odoo:10.0
MAINTAINER Mick Tseng <suncombo@gmail.com>

USER root

# Set OS timezone to Taipei
RUN ln -sf /usr/share/zoneinfo/Asia/Taipei /etc/localtime

# Set Odoo timezone to Taipei (will be set at startup thanks to Odoo
# parameter substitution)
ENV ODOO_TIMEZONE=Asia/Taipei

# Generate locales
RUN apt-get update \
    && apt-get -y install ttf-wqy-zenhei ttf-wqy-microhei \
                          locales locales-all
ENV LC_ALL zh_TW.UTF-8
ENV LANG zh_TW.UTF-8
ENV LANGUAGE zh_TW.UTF-8

RUN pip install python-slugify

USER odoo