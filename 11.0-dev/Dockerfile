FROM suncombo/odoo-tw:11.0

USER root

RUN pip3 install ptvsd==3.0.0

RUN sed -i -e '2iimport ptvsd\nptvsd.enable_attach("my_secret", ("0.0.0.0", 3000))\nprint("ptvsd is started")' /odoo/source/odoo-bin

EXPOSE 3000

USER odoo