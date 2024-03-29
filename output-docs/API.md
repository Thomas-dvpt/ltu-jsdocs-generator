## Objects

<dl>
<dt><a href="#global">global</a> : <code>object</code></dt>
<dd><p>Description de mon nameSpace</p>
</dd>
<dt><a href="#general">general</a> : <code>object</code></dt>
<dd><p>Description de mon nameSpace</p>
</dd>
<dt><a href="#screenLayout">screenLayout</a> : <code>object</code></dt>
<dd><p>Description de mon nameSpace</p>
</dd>
<dt><a href="#screenHistory">screenHistory</a> : <code>object</code></dt>
<dd><p>Description de mon nameSpace</p>
</dd>
</dl>

## Constants

<dl>
<dt><a href="#CHECK_INTERVAL">CHECK_INTERVAL</a> : <code>number</code></dt>
<dd><p>Intervalle de vérification en ms</p>
</dd>
<dt><a href="#PLANT_HIERARCHY_PATH">PLANT_HIERARCHY_PATH</a> : <code>string</code></dt>
<dd><p>// Chemin de la fenêtre de vue principale</p>
</dd>
<dt><a href="#SCREEN_TOP_LVL_NAV_PATH">SCREEN_TOP_LVL_NAV_PATH</a> : <code>string</code></dt>
<dd></dd>
<dt><a href="#SCREEN_EXTENDED_NAV_PATH">SCREEN_EXTENDED_NAV_PATH</a> : <code>string</code></dt>
<dd></dd>
<dt><a href="#PREFIX_BP">PREFIX_BP</a> : <code>string</code></dt>
<dd></dd>
<dt><a href="#MAX_BP">MAX_BP</a> : <code>number</code></dt>
<dd></dd>
<dt><a href="#MAX_BP_EXTENDED">MAX_BP_EXTENDED</a> : <code>number</code></dt>
<dd><p>MAX_BP + 8</p>
</dd>
<dt><a href="#MAX_HISTORY_SIZE">MAX_HISTORY_SIZE</a> : <code>number</code></dt>
<dd><p>Taille maximale de l&#39;historique de navigation</p>
</dd>
<dt><a href="#SCREEN_MAIN">SCREEN_MAIN</a> : <code>string</code></dt>
<dd></dd>
<dt><a href="#SCREEN_MAIN">SCREEN_MAIN</a> : <code>string</code></dt>
<dd></dd>
</dl>

<a name="global"></a>

## global : <code>object</code>
Description de mon nameSpace

**Kind**: global namespace  

* [global](#global) : <code>object</code>
    * [._initRuntime()](#global._initRuntime)
    * [._config()](#global._config)

<a name="global._initRuntime"></a>

### global.\_initRuntime()
Cette fonction initialise des paramètres au lancement de la page web.

**Kind**: static method of [<code>global</code>](#global)  
**Throws**:

- <code>Error</code> 

**Since**: 2.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 2.0.1  
**Author**: Thomas HEURTAULT  
<a name="global._config"></a>

### global.\_config()
Description de ma fonction

**Kind**: static method of [<code>global</code>](#global)  
**Since**: 1.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 3.0.1  
**Author**: Thomas HEURTAULT  
<a name="general"></a>

## general : <code>object</code>
Description de mon nameSpace

**Kind**: global namespace  

* [general](#general) : <code>object</code>
    * [.general_logTrace(functionName, type, message)](#general.general_logTrace)
    * [.general_userAudit(type, message, [oldValue], [newValue])](#general.general_userAudit)
    * [.general_waitForUiElement(elementPath, [timeout])](#general.general_waitForUiElement) ⇒ <code>Promise.&lt;Object&gt;</code>

<a name="general.general_logTrace"></a>

### general.general\_logTrace(functionName, type, message)
Enregistre des messages de trace avec des paramètres d'entrée spécifiques

**Kind**: static method of [<code>general</code>](#general)  
**Throws**:

- <code>Error</code> - Paramètres d'entrée invalides

**Since**: 3.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 3.0.1  
**Author**: Thomas HEURTAULT  

| Param | Type | Description |
| --- | --- | --- |
| functionName | <code>string</code> | Nom de la fonction à journaliser |
| type | <code>string</code> | Type de message de journalisation (par exemple, 'success', 'error', 'warning', 'debug') |
| message | <code>string</code> | Le message de journalisation |

**Example** *(Tracer un succès)*  
```js
general_logTrace('myFunction', 'success', 'Opération réussie');
```
**Example** *(Tracer une erreur)*  
```js
general_logTrace('myFunction', 'error', 'Erreur critique');
```
**Example** *(Tracer un avertissement)*  
```js
general_logTrace('myFunction', 'warning', 'Avertissement non critique');
```
**Example** *(Tracer mon script pour debuger)*  
```js
general_logTrace('myFunction', 'debug', 'Je vérifie l'execution de mon script');
```
<a name="general.general_userAudit"></a>

### general.general\_userAudit(type, message, [oldValue], [newValue])
Effectue des opérations d'audit en enregistrant des messages selon le type spécifié.

**Kind**: static method of [<code>general</code>](#general)  
**Throws**:

- <code>Error</code> - Paramètres d'entrée invalides

**Since**: 3.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 3.0.1  
**Author**: Thomas HEURTAULT  

| Param | Type | Description |
| --- | --- | --- |
| type | <code>&#x27;text&#x27;</code> \| <code>&#x27;bool&#x27;</code> \| <code>&#x27;analog&#x27;</code> | Type d'audit (par exemple, 'text', 'bool', 'analog') |
| message | <code>string</code> | Le message d'audit |
| [oldValue] | <code>any</code> | La valeur précédente (utilisée pour 'bool' et 'analog') |
| [newValue] | <code>any</code> | La nouvelle valeur (utilisée pour 'bool' et 'analog') |

<a name="general.general_waitForUiElement"></a>

### general.general\_waitForUiElement(elementPath, [timeout]) ⇒ <code>Promise.&lt;Object&gt;</code>
* Cette fonction attend qu'un élément d'interface utilisateur (UI) soit disponible sur l'écran actifen fonction du chemin de l'élément spécifié (elementPath). La fonction vérifie périodiquementl'existence de l'élément jusqu'à ce qu'il soit trouvé ou que le délai d'attente (timeout) soit dépassé.

**Kind**: static method of [<code>general</code>](#general)  
**Returns**: <code>Promise.&lt;Object&gt;</code> - - Promesse qui retoune l'élément trouvé ou rejette une erreur si le délai est dépassé  
**Throws**:

- <code>Error</code> - Erreur qui peut être levée en cas de problème lors de l'exécution de la fonction

**Since**: 2.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 2.0.1  
**Author**: Thomas HEURTAULT  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| elementPath | <code>string</code> |  | Chemin de l'élément UI à rechercher sur l'écran actif |
| [timeout] | <code>number</code> | <code>10000</code> | Délai d'attente maximal en millisecondes (par défaut : 10000 ms) |

<a name="screenLayout"></a>

## screenLayout : <code>object</code>
Description de mon nameSpace

**Kind**: global namespace  

* [screenLayout](#screenLayout) : <code>object</code>
    * [.screenLayout_getHierarchyFirstLevel()()](#screenLayout.screenLayout_getHierarchyFirstLevel_new) ⇒ <code>Array</code>
    * [.screenLayout_setHierarchyNodes([RootNodeName])](#screenLayout.screenLayout_setHierarchyNodes) ⇒ <code>Promise.&lt;void&gt;</code>
    * [.screenLayout_setTopLevelNavigation()](#screenLayout.screenLayout_setTopLevelNavigation) ⇒ <code>void</code>
    * [.screenLayout_getHierarchyInfos()](#screenLayout.screenLayout_getHierarchyInfos) ⇒ <code>Promise.&lt;Object&gt;</code>
    * [.screenLayout_setSecondLevelNavigation(screenName, secondLvlNav)](#screenLayout.screenLayout_setSecondLevelNavigation) ⇒ <code>void</code>

<a name="screenLayout.screenLayout_getHierarchyFirstLevel_new"></a>

### screenLayout.screenLayout\_getHierarchyFirstLevel()() ⇒ <code>Array</code>
Cette fonction, filtre les objets "LTU_PO_Screen" de Plant Object,pour récupérer les cheminscontenant exactement un seul '/' et ne contenant pas le caractère '@'.Elle renvoie ensuite une liste d'objets contenant le chemin et le nom extraits de ces objets filtrés.

**Kind**: static method of [<code>screenLayout</code>](#screenLayout)  
**Returns**: <code>Array</code> - - Un tableau d'objets contenant les chemins des PO et leur noms filtrés.  
**Throws**:

- <code>Error</code> 

**Since**: 2.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 2.0.1  
**Author**: Thomas HEURTAULT  
<a name="screenLayout.screenLayout_setHierarchyNodes"></a>

### screenLayout.screenLayout\_setHierarchyNodes([RootNodeName]) ⇒ <code>Promise.&lt;void&gt;</code>
Cette fonction définit le nœud racine de l'objet "Plant_Navigation" et sélectionne un objet de vue.

**Kind**: static method of [<code>screenLayout</code>](#screenLayout)  
**Returns**: <code>Promise.&lt;void&gt;</code> - - Promesse résolue lors de la définition du nœud racine et de la sélection de la vue.  
**Throws**:

- <code>Error</code> -

**Since**: 2.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 2.0.1  
**Author**: Thomas HEURTAULT  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [RootNodeName] | <code>string</code> | <code>&quot;\&quot;\&quot;&quot;</code> | Nom du nœud à utiliser comme racine de navigation. |

<a name="screenLayout.screenLayout_setTopLevelNavigation"></a>

### screenLayout.screenLayout\_setTopLevelNavigation() ⇒ <code>void</code>
Cette fonction configure les boutons de navigation pour les éléments de niveau supérieur de la hiérarchie des objets "Synoptique" de Plant Object.Elle filtre ces objets en recherchant ceux dont le chemin contient exactement un seul '/' et configure les boutons de navigation correspondants.

**Kind**: static method of [<code>screenLayout</code>](#screenLayout)  
**Returns**: <code>void</code> - - Cette fonction ne renvoie pas de valeur.  
**Throws**:

- <code>Error</code> - Erreur qui peut être levée en cas de problème lors de l'exécution de la fonction.

**Since**: 3.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 3.0.1  
**Author**: Thomas HEURTAULT  
<a name="screenLayout.screenLayout_getHierarchyInfos"></a>

### screenLayout.screenLayout\_getHierarchyInfos() ⇒ <code>Promise.&lt;Object&gt;</code>
Cette fonction récupère des informations à partir d'un objet PlantNavigation.Elle extrait les informations telles que le chemin du premier objet Synoptique,le préfixe d'exécution, le préfixe de la hiérarchie et le nom de la hiérarchie.

**Kind**: static method of [<code>screenLayout</code>](#screenLayout)  
**Returns**: <code>Promise.&lt;Object&gt;</code> - - Une promesse qui résout un objet contenant les informations extraites ou rejette une erreur en cas de problème.  
**Throws**:

- <code>Error</code> - Erreur qui peut être levée en cas de problème lors de l'exécution de la fonction.

**Since**: 2.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 2.0.1  
**Author**: Thomas HEURTAULT  
<a name="screenLayout.screenLayout_setSecondLevelNavigation"></a>

### screenLayout.screenLayout\_setSecondLevelNavigation(screenName, secondLvlNav) ⇒ <code>void</code>
Cette fonction parcourt les éléments de navigation de second niveau fournis, puis les associe aux boutons de navigation correspondants sur l'écran actif.Si le nombre d'éléments de navigation est inférieur au nombre maximal de boutons de navigation de second niveau, les boutons excédentaires sont masqués.

**Kind**: static method of [<code>screenLayout</code>](#screenLayout)  
**Returns**: <code>void</code> - - Cette fonction ne renvoie pas de valeur.  
**Throws**:

- <code>Error</code> - Erreur qui peut être levée en cas de problème lors de l'exécution de la fonction.

**Since**: 1.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 1.0.1  
**Author**: Thomas HEURTAULT  

| Param | Type | Description |
| --- | --- | --- |
| screenName | <code>string</code> | Le nom de l'écran sur lequel configurer la navigation de second niveau. |
| secondLvlNav | <code>Array</code> | Le tableau des éléments de navigation de second niveau. |

<a name="screenHistory"></a>

## screenHistory : <code>object</code>
Description de mon nameSpace

**Kind**: global namespace  

* [screenHistory](#screenHistory) : <code>object</code>
    * [.screenHistory_changeScreen(screenName)](#screenHistory.screenHistory_changeScreen)
    * [.screenHistory_goBackScreen()](#screenHistory.screenHistory_goBackScreen)
    * [.screenHistory_goForwardScreen()](#screenHistory.screenHistory_goForwardScreen)
    * [.screenHistory_createStackDataset()](#screenHistory.screenHistory_createStackDataset)
    * [.screenHistory_updateButtonState()](#screenHistory.screenHistory_updateButtonState)

<a name="screenHistory.screenHistory_changeScreen"></a>

### screenHistory.screenHistory\_changeScreen(screenName)
Cette fonction gère l'historique de navigation.Elle ajoute le nom de l'écran actuel à l'historique, vide la pile de navigation suivant, et met à jour l'état des boutons de navigation.

**Kind**: static method of [<code>screenHistory</code>](#screenHistory)  
**Throws**:

- <code>Error</code> 

**Since**: 1.0.1  | 01/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 1.0.1  
**Author**: Thomas HEURTAULT  

| Param | Type | Description |
| --- | --- | --- |
| screenName | <code>string</code> | Nom de l'écran vers lequel naviguer. |

<a name="screenHistory.screenHistory_goBackScreen"></a>

### screenHistory.screenHistory\_goBackScreen()
Cette fonction est responsable de naviguer vers l'écran précédent dans l'historique de navigation.Elle récupère les DataSets d'historique et de pile avant, déplace l'état actuel vers la pile avant,charge l'écran précédent depuis l'historique et effectue le changement d'écran.Cette fonction est généralement appelée lorsque l'utilisateur appuie sur le bouton de retour.

**Kind**: static method of [<code>screenHistory</code>](#screenHistory)  
**Throws**:

- <code>Error</code> - Erreur qui peut être levée en cas de problème lors de la navigation vers l'écran précédent.

**Since**: 1.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 1.0.1  
**Author**: Thomas HEURTAULT  
<a name="screenHistory.screenHistory_goForwardScreen"></a>

### screenHistory.screenHistory\_goForwardScreen()
Cette fonction est responsable de naviguer vers l'écran suivant dans l'historique de navigation.Elle récupère les DataSets d'historique et de pile avant, déplace l'état suivant vers l'historique,charge l'écran suivant depuis la pile avant et effectue le changement d'écran.Cette fonction est généralement appelée lorsque l'utilisateur appuie sur le bouton de navigation vers l'avant.

**Kind**: static method of [<code>screenHistory</code>](#screenHistory)  
**Throws**:

- <code>Error</code> - Erreur qui peut être levée en cas de problème lors de la navigation vers l'écran suivant

**Since**: 1.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc
.  
**Version**: 1.0.1  
**Author**: Thomas HEURTAULT  
<a name="screenHistory.screenHistory_createStackDataset"></a>

### screenHistory.screenHistory\_createStackDataset()
Cette fonction crée les DataSets nécessaires pour stocker l'historique de navigation.Si les DataSets n'existent pas déjà, ils sont créés avec des tableaux vides pour stocker l'historique et la pile avant.Cette fonction est généralement appelée au démarrage de l'application pour initialiser les DataSets.

**Kind**: static method of [<code>screenHistory</code>](#screenHistory)  
**Throws**:

- <code>Error</code> - Erreur qui peut être levée en cas de problème lors de la navigation vers l'écran suivant

**Since**: 1.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 1.0.1  
**Author**: Thomas HEURTAULT  
<a name="screenHistory.screenHistory_updateButtonState"></a>

### screenHistory.screenHistory\_updateButtonState()
Cette fonction est responsable de mettre à jour l'état des boutons de navigation précédent/suivant de l'interface utilisateur.Elle récupère les DataSets d'historique et de pile avant pour déterminer si les boutons précédent et suivant doivent être activés ou désactivés.Cette fonction est généralement appelée après un changement d'écran pour mettre à jour l'état des boutons de navigation.

**Kind**: static method of [<code>screenHistory</code>](#screenHistory)  
**Throws**:

- <code>Error</code> - Erreur qui peut être levée en cas de problème lors de la mise à jour de l'état des boutons.

**Since**: 1.0.1  | 03/2024   | Thomas Heurtault  | implement JSDoc  
**Version**: 1.0.1  
**Author**: Thomas HEURTAULT  
<a name="CHECK_INTERVAL"></a>

## CHECK\_INTERVAL : <code>number</code>
Intervalle de vérification en ms

**Kind**: global constant  
**Default**: <code>100</code>  
<a name="PLANT_HIERARCHY_PATH"></a>

## PLANT\_HIERARCHY\_PATH : <code>string</code>
// Chemin de la fenêtre de vue principale

**Kind**: global constant  
**Default**: <code>&quot;\&quot;~/@Menu\&quot;&quot;</code>  
<a name="SCREEN_TOP_LVL_NAV_PATH"></a>

## SCREEN\_TOP\_LVL\_NAV\_PATH : <code>string</code>
**Kind**: global constant  
**Default**: <code>&quot;~/FV_@Header/FV_@Navigation/&quot;</code>  
<a name="SCREEN_EXTENDED_NAV_PATH"></a>

## SCREEN\_EXTENDED\_NAV\_PATH : <code>string</code>
**Kind**: global constant  
**Default**: <code>&quot;~~/FV_@NavigationExtended/&quot;</code>  
<a name="PREFIX_BP"></a>

## PREFIX\_BP : <code>string</code>
**Kind**: global constant  
**Default**: <code>&quot;BP_Nav_&quot;</code>  
<a name="MAX_BP"></a>

## MAX\_BP : <code>number</code>
**Kind**: global constant  
**Default**: <code>7</code>  
<a name="MAX_BP_EXTENDED"></a>

## MAX\_BP\_EXTENDED : <code>number</code>
MAX_BP + 8

**Kind**: global constant  
**Default**: <code>8</code>  
<a name="MAX_HISTORY_SIZE"></a>

## MAX\_HISTORY\_SIZE : <code>number</code>
Taille maximale de l'historique de navigation

**Kind**: global constant  
**Default**: <code>10</code>  
<a name="SCREEN_MAIN"></a>

## SCREEN\_MAIN : <code>string</code>
**Kind**: global constant  
**Default**: <code>&quot;//FV_@Main&quot;</code>  
<a name="SCREEN_MAIN"></a>

## SCREEN\_MAIN : <code>string</code>
**Kind**: global constant  
**Default**: <code>&quot;//FV_@Main&quot;</code>  
