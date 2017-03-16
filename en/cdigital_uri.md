# cdigital:// protocol
## Purpose 
The cdigital:// protocol allows to open the application on a specific environment or to triggers specific actions from an URL or a NFC tag event:
- `cdigital://launch` : Opens the Compositeur Digital application from a web browser
- `cdigital://launch?rootItem=Ma%20Banque` : Opens the "Ma Banque" environment in the Compositeur Digital 
- `cdigital://launch?firstName=Jean&lastName=Dupont` : positions context data [données de contexte](config.md#valueKeys) in the current environment.
- `cdigital://launch?action=showmenu_recents` : opens the environment's recent documents. Other possible values are :
	- showmenu_home,
	- showmenu_search,
	- showmenu_recents,
	- showmenu_mostused,
	- showmenu_papers,
	- showmenu_profile,
	- showmenu_basket,
	- showmenu_about

[Revenir au menu](home.md)
