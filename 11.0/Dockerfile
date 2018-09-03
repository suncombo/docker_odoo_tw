FROM suncombo/odoo:11.0

USER root

# Generate locales
RUN set -x; \
    apt-get update \
    && apt-get -y install ttf-wqy-zenhei ttf-wqy-microhei                      

# Set Odoo timezone to Taipei (will be set at startup thanks to Odoo
# parameter substitution)
ENV ODOO_TIMEZONE=Asia/Taipei

USER odoo