=====================================================
knife client
=====================================================

.. include:: ../../includes_security/includes_security_chef_validator.rst

.. include:: ../../includes_knife/includes_knife_client.rst
   
bulk delete
=====================================================
.. include:: ../../includes_knife/includes_knife_client_bulk_delete.rst

**Syntax**

.. include:: ../../includes_knife/includes_knife_client_bulk_delete_syntax.rst

**Options**

|no_options|

**Examples**

None.

create
=====================================================
.. include:: ../../includes_knife/includes_knife_client_create.rst

**Syntax**

.. include:: ../../includes_knife/includes_knife_client_create_syntax.rst

**Options**

.. include:: ../../includes_knife/includes_knife_client_create_options.rst

**knife.rb File Settings**

.. include:: ../../includes_knife/includes_knife_using_knife_rb.rst

..note:: See :doc:`knife.rb </config_rb_knife>` for more information about how to add optional settings to the |knife rb| file.

.. include:: ../../includes_knife/includes_knife_client_create_settings.rst

**Examples**

For example, to create a |chef client admin| with the name "exampleorg" and save its private key to a file, enter:

.. code-block:: bash

   $ knife client create exampleorg -a -f "/etc/chef/client.pem"

When running the ``create`` argument on |chef hosted| or |chef private|, be sure to omit the ``-a`` option:

.. code-block:: bash

   $ knife client create exampleorg -f "/etc/chef/client.pem"

delete
=====================================================
.. include:: ../../includes_knife/includes_knife_client_delete.rst

**Syntax**

.. include:: ../../includes_knife/includes_knife_client_delete_syntax.rst

**Options**

|no_options|

**Examples**

For example, to delete a client with the name "client_foo", enter:

.. code-block:: bash

   $ knife client delete client_foo

Type ``Y`` to confirm a deletion.

edit
=====================================================
.. include:: ../../includes_knife/includes_knife_client_edit.rst

**Syntax**

.. include:: ../../includes_knife/includes_knife_client_edit_syntax.rst

**Options**

|no_options|

**Examples**

For example, to edit a client with the name "exampleorg", enter:

.. code-block:: bash

   $ knife client edit exampleorg

list
=====================================================
.. include:: ../../includes_knife/includes_knife_client_list.rst

**Syntax**

.. include:: ../../includes_knife/includes_knife_client_list_syntax.rst

**Options**

.. include:: ../../includes_knife/includes_knife_client_list_options.rst

**Examples**

.. include:: ../../step_knife/step_knife_client_list_all.rst

.. include:: ../../step_knife/step_knife_client_list_authenticate.rst

reregister
=====================================================
.. include:: ../../includes_knife/includes_knife_client_reregister.rst

**Syntax**

.. include:: ../../includes_knife/includes_knife_client_reregister_syntax.rst

**Options**

.. include:: ../../includes_knife/includes_knife_client_reregister_options.rst

**knife.rb File Settings**

.. include:: ../../includes_knife/includes_knife_using_knife_rb.rst

..note:: See :doc:`knife.rb </config_rb_knife>` for more information about how to add optional settings to the |knife rb| file.

.. include:: ../../includes_knife/includes_knife_client_reregister_settings.rst

**Examples**

For example, to regenerate the RSA key pair for a client named "testclient" and save it to a file named "rsa_key", enter:

.. code-block:: bash

   $ knife client regenerate testclient -f rsa_key

show
=====================================================
.. include:: ../../includes_knife/includes_knife_client_show.rst

**Syntax**

.. include:: ../../includes_knife/includes_knife_client_show_syntax.rst

**Options**

.. include:: ../../includes_knife/includes_knife_client_show_options.rst

**Examples**

For example, to view a client named "testclient", enter:

.. code-block:: bash

   $ knife client show testclient

to return something like:

.. code-block:: bash

   admin:       false
   chef_type:   client
   json_class:  Chef::ApiClient
   name:        testclient
   public_key:

To view information in |json| format, use the ``-F`` common option as part of the command like this:

.. code-block:: bash

   $ knife client show testclient -F json

Other formats available include ``text``, ``yaml``, and ``pp``.