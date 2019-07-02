.. _insatll/digitalocean:

===========================
Instalando en Digital Ocean
===========================

Meta
====

Para el final de este tutorial deberías tener un JupyterHub con
algunos usuarios admin y un entorno para tus usuarios con paquetes
que quieres instalados corriendo en `DigitalOcean <https://digitalocean.com>`_.

Pre-requisitos
==============

#. Una cuenta DigitalOcean con un método de pago.

Paso 1: Instalando The Littlest JupyterHub
==========================================

Creemos el servidor en el que va a correr JupyterHub.

#. Inicia sesión en `DigitalOcean <https://digitalocean.com>`_. Tal vez quieras
   conectar una tarjeta de crédito o algún otro método de pago antes de proseguir
   con el tutorial.

#. Haz clic en el botón **Create** en la esquina superior derecha,
   selecciona **Droplets** en el menu. DigitalOcean llama **droplets** a sus servidores.

   .. image:: ../images/providers/digitalocean/create-menu.png
      :alt: Menu haciendo clic 'create' en la esquina superior derecha.

   Esto te lleva a una página llamada **Create Droplets** donde puedes 
   configurar tu servidor.

#. Bajo **Choose an image**, selecciona **18.04 x64** bajo **Ubuntu**.

   .. image:: ../images/providers/digitalocean/select-image.png
      :alt: Selecciona la imagen 18.04 x64 bajo Ubuntu

#. Bajo **Choose a size**, selecciona el tamaño del servidor que deseas. 
   
   La opción por defecto
   (4GB RAM, 2CPUs, 20 USD / mes) no es un mal inicio. Puedes cambiar el 
   tamaño de tu servidor más adelante si lo necesitas.

   Lee nnuestra guía práctica en Como :ref:`como/admin/estimando-recursos` para 
   ayudarte escoger cuanta Memoria, CPU y disco duro tu servidor necesita.

#. Más abajo en **Select additional options**, selecciona **User data**.

   .. image:: ../images/providers/digitalocean/additional-options.png
      :alt: Utiliza User Data en opciones adicionales.

   Esto abre una caja de texto donde puedes incluir un script que será
   ejecutado cuando se cree el servidor. Utilizaremos esto para configurar
   The Littlest JupyterHub en este servidor.

#. Copy the text below, and paste it into the user data text box. Replace
   ``<admin-user-name>`` with the name of the first **admin user** for this
   JupyterHub. This admin user can log in after the JupyterHub is set up, and
   can configure it to their needs. **Remember to add your username**!

   .. code-block:: bash

      #!/bin/bash
      curl https://raw.githubusercontent.com/jupyterhub/the-littlest-jupyterhub/master/bootstrap/bootstrap.py \
        | sudo python3 - \
          --admin <admin-user-name>

   .. note::

      See :ref:`topic/installer-actions` if you want to understand exactly what the installer is doing.
      :ref:`topic/customizing-installer` documents other options that can be passed to the installer.

#. Under the **Finalize and create** section, enter a ``hostname`` that descriptively
   identifies this server for you.

   .. image:: ../images/providers/digitalocean/hostname.png
      :alt: Select suitable hostname for your server

#. Click the **Create** button! You will be taken to a different screen,
   where you can see progress of your server being created.

   .. image:: ../images/providers/digitalocean/server-create-wait.png
      :alt: Server being created

#. In a few seconds your server will be created, and you can see the **public IP**
   used to access it.

   .. image:: ../images/providers/digitalocean/server-create-done.png
      :alt: Server finished creating, public IP available

#. The Littlest JupyterHub is now installing in the background on your new server.
   It takes around 5-10 minutes for this installation to complete.

#. Check if the installation is complete by copying the **public ip**
   of your server, and trying to access it with a browser. This will fail until
   the installation is complete, so be patient.

#. When the installation is complete, it should give you a JupyterHub login page.

   .. image:: ../images/first-login.png
      :alt: JupyterHub log-in page

#. Login using the **admin user name** you used in step 6, and a password. Use a
   strong password & note it down somewhere, since this will be the password for
   the admin user account from now on.

#. Congratulations, you have a running working JupyterHub!

Step 2: Adding more users
==========================

.. include:: add_users.txt

Step 3: Install conda / pip packages for all users
==================================================

.. include:: add_packages.txt