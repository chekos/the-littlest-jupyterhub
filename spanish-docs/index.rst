=======================
The Littlest JupyterHub
=======================

Una distribución simple de `JupyterHub <https://github.com/jupyterhub/jupyterhub>`_ para
un grupo pequeño de usuarios (0-100) en un servidor. Recomendamos leer 
:ref:`tema/cuandousar` para determinar si esta es la herramienta correcta para ti.


Estado de desarrollo
====================

Este proyecto se encuentra en estado **beta**. Varias personas han estado usando
instalaciones de TLJH por más de un año con gran exito. Auqnue nos esforzamos por no hacerlo,
todavía podría hacer cambios de última hora que no tienen una ruta de actualización clara.


Instalación
===========

The Littlest JupyterHub (TLJH) puede correr en cualquier servidor que utilice
por lo menos **Ubuntu 18.04**. Versiones anteriores de Ubuntu no son compatibles.
Tenemos un montón de tutoriales para que empieces.

- Tutoriales para crear un nuevo servidor desde cero en un proveedor de nube y 
  desplegar TLJH en él. Estos son **recomendados** si no tienes mucha experiencia
  configurando servirodres.

  .. toctree::
     :titlesonly:
     :caption: Instalación

     install/digitalocean
     install/ovh
     install/jetstream
     install/google
     install/amazon
     install/azure
     install/custom-server

Ya que estes lista para correr tu servidor es buena
idea proceder directamente a :doc:`como/admin/https`.

Guías prácticas
===============

Guías prácticas para responder la pregunta "¿Cómo hago...?" para muchos temas.

Contenido y Datos
-----------------

.. toctree::
   :titlesonly:
   :caption: Contenido y Datos

   como/content/nbgitpuller
   como/content/add-data
   como/content/share-data

Entorno del usuario
-------------------

.. toctree::
   :titlesonly:
   :caption: Entorno del usuario

   como/env/user-environment
   como/env/notebook-interfaces
   como/env/server-resources

Autenticación
--------------

Tenemos un conjunto especial de Guías prácticas sobre como usar varias formas de 
autenticación con tu JupyterHub. Para más información sobre Autenticación, vea
:ref:`tema/authenticator-configuration`

.. toctree::
   :titlesonly:
   :caption: Autenticación

   como/auth/dummy
   como/auth/github
   como/auth/firstuse
   como/auth/nativeauth

Administration and security
---------------------------

.. toctree::
   :titlesonly:
   :caption: Administration and security

   como/admin/admin-users
   como/admin/resource-estimation
   como/admin/resize
   como/admin/nbresuse
   como/admin/https
   como/admin/enable-extensions

Cloud provider configuration
----------------------------

.. toctree::
   :titlesonly:
   :caption: Cloud provider configuration

   como/providers/digitalocean
   como/providers/azure

Topic Guides
============

Topic guides provide in-depth explanations of specific topics.

.. toctree::
   :titlesonly:
   :caption: Topic guides

   tema/cuandousar
   topic/requirements
   topic/security
   topic/customizing-installer
   topic/installer-actions
   topic/tljh-config
   topic/authenticator-configuration
   topic/escape-hatch
   topic/idle-culler


Troubleshooting
===============

In time, all systems have issues that need to be debugged. Troubleshooting
guides help you find what is broken & hopefully fix it.

.. toctree::
   :titlesonly:
   :caption: Troubleshooting

   troubleshooting/logs

Often, your issues are not related to TLJH itself but to the cloud provider
your server is running on. We have some documentation on common issues you
might run into with various providers and how to fix them. We welcome contributions
here to better support your favorite provider!

.. toctree::
   :titlesonly:

   troubleshooting/providers/google
   troubleshooting/providers/amazon
   troubleshooting/providers/custom

Contributing
============

We want you to contribute to TLJH in the ways that are most useful
and exciting to you. This section contains documentation helpful
to people contributing in various ways.

.. toctree::
   :titlesonly:
   :caption: Contributing

   contributing/docs
   contributing/code-review
   contributing/dev-setup
   contributing/tests
   contributing/plugins
   contributing/packages
