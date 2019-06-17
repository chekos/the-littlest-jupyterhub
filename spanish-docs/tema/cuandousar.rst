.. _tema/cuandousar:

===================================
Cuando usar The Littlest JupyterHub
===================================

Esta página es una pequeña guía para determinar el uso de The Littlest JupyterHub
(TLJH) o `Zero to JupyterHub for Kubernetes <https://zero-to-jupyterhub.readthedocs.io/en/latest/>`_ (Z2JH).
Muchas de estas ideas fueron introducidas en un 
`blog post anunciando TLJH <http://words.yuvi.in/post/the-littlest-jupyterhub/>`_.

`**The Littlest JupyterHub (TLJH)** <https://the-littlest-jupyterhub.readthedocs.io/en/latest/>`_ es una 
distribución opinionada y pre-configurada para desplegar un JupyterHub en **una sola máquina** 
(en la nube o en tu propio hardware). Esta diseñado para ser una solución más ligera y mantenible 
para casos donde el tamaño, escalabilidad, y ahorro de costos no son una gran preocupación.

`**Zero to JupyterHub on Kubernetes** <https://zero-to-jupyterhub.readthedocs.io/en/latest/>`_ te permite
desplegar JupyterHub en **Kubernetes**. Esto permite que JupyterHub escale a miles de usuarios,
crezca/reduzca el tamaño de los recursos que necesita, y use tecnología de contenedores para 
administrar las sesiones de usuarios.

Cuando usar TLJH vs. Z2JH
=========================

La decisión de utilizar TLJH y Z2JH ultimadamente depende de un par de preguntas:

1. ¿Quieres que tu Hub y todos sus usuarios vivan en **una máquina grande** o esparcidos en un **grupo de máquinas más pequeñas** que pueden escalar en tamaño?

   * Si puedes utilizar una sola máquina, te recomendamos **The Littlest JupyterHub**.
   * Si quieres utilizar multiples máquinas, te recomendamos **Zero to JupyterHub for Kubernetes**.
2. ¿Necesitas **usar tecnología de contenedores**?

   * Si no, te recomendamos **The Littlest JupyterHub**.
   * Si si, te recomendamos **Zero to JupyterHub for Kubernetes**.
