http://docutils.sourceforge.net/docs/ref/rst/directives.html


.. sidebar:: Sidebar Title
   :subtitle: Optional Sidebar Subtitle

   Subsequent indented lines comprise
   the body of the sidebar, and are
   interpreted as body elements.
   

.. list-table:: Frozen Delights!
   :widths: 20,20,20
   :header-rows: 1

   * - Treat
     - Quantity
     - Description
   * - Albatross
     - 2.99
     - On a stick!
   * - Crunchy Frog
     - 1.49
     - If we took the bones out, it wouldn't be
       crunchy, now would it?
   * - Gannet Ripple
     - 1.99
     - On a stick!


.. container:: custom

   This paragraph might be rendered in a custom way





+--------------------------------------------------------------------------------------------------------------------------------+
| Box                                                                                                                            |
|                                                                                                                                | 
| `OpendataSicilia <http://opendatasicilia.it>`_                                                                                 |
|                                                                                                                                |
| `Non Portale open data Regione Sicilia <http://nonportale.opendatasicilia.it/index.html>`_                                     |
|                                                                                                                                |
| `Petrusino <http://petrusino.opendatasicilia.it/index.html>`_                                                                  |
|                                                                                                                                |
| `Albo Pop <http://albopop.it>`_                                                                                                |
|                                                                                                                                |
| `FOIA Pop <http://www.foiapop.it>`_                                                                                            |
+--------------------------------------------------------------------------------------------------------------------------------+



+---------------------------------------------------------------------+
| Box                                                                 |
|                                                                     |
| il movvv bbbbbbbbb bbbb bbb bbbbb bbbb bbbb bbb b b bbbbb b b bbbb b|
| a nuove modalità di relazione e confronto con il mercato, in linea  |
| con le grandi sfide poste da una Pubblica amministrazione           |
| moderna [1]_. Il programma affronta temi di notevole impatto sociale|
| e innovazione pubblica: dall’autismo alla protezione dai rischi     |
| ambientali, alla sicurezza e la qualità degli alimenti fino a       |
| soluzioni tecnologiche innovative applicate all’assistenza sanitaria|
| e all’*e-government*. Non solo grandi imprese ma anche startup,     |
| piccole imprese e venture capitalist hanno la possibilità di        |
| presentare idee e proposte innovative.                              |
|                                                                     |
| Il PCP è quindi terreno fertile per la sperimentazione e la ricerca |
| indirizzata al soddisfacimento dei bisogni sociali anche con        |
| strumenti innovativi legati all’IA. Un esempio in tal senso è       |
| l’appalto “Tecnologie per l’autismo” volto ad individuare tecnologie|
| di Realtà Virtuale e Realtà Aumentata tipizzate per persone con una |
| condizione dello spettro autistico (ASC) [2]_.                      |
+---------------------------------------------------------------------+

.. rubric:: Note

.. [1]
   Hila Mehr, *Artificial Intelligence for Citizen Services and Government*, HARVARD Kennedy School - ASH Center for Democratic
   Governance and Innovation (2017)

.. [2]
   *The role of design in collaborative AI*, Medium, 4,11, 2017
   `https://medium.com/@newcortex.ai/the-role-of-design-in-collaborative-ai-ca18c1e69d0b <https://medium.com/@newcortex.ai/the-role-of-design-in-collaborative-ai-ca18c1e69d0b>`__
   (consultato a febbraio 2017).


------


.. code-block:: bash

  > cd ./daf-recipes/ckan
  > ./build_local.sh

Then edit the file *ckan.ini*:

- If you are using our openLDAP server:

   .. code-block:: bash

      LDAP Intergration with ldap and ip address
      ckanext.ldap.uri = ldap://LDAP_IP:389
      ckanext.ldap.auth.dn = cn=admin,dc=daf,dc=test,dc=it
      ckanext.ldap.auth.password = admin
      ckanext.ldap.base_dn = cn=users,cn=accounts,dc=daf,dc=test,dc=it
      ckanext.ldap.search.filter = uid={login}
      ckanext.ldap.username = uid
      ckanext.ldap.email = mail
      ckanext.ldap.ckan_fallback = True
