# Les variables
Les variables permettent de sauvegarder et réinitialiser des valeurs. Il existe 2 types de variables possèdant leurs spécificité. <br>
Conventionnellement, les altérables et constantes doivent s'écrire en `camelCase`.
```fox
notation nom[type] = valeur;
```
---

## `const` - Constantes
Les constantes sont des variables ayant lors de leurs déclarations une valeur constante qui ne peut changer, être redéfini ou retypé.
<pre data-lang="fox"><code><span class="hljs-keyword">const</span> <span class="hljs-var_">element</span>[<span class="hljs-type">string</span>] = <span class="hljs-string">'Bonjour !'</span>; <span class="hljs-comment">## 'Bonjour !'</span>
<span class="hljs-var_">element</span> = <span class="hljs-string">'Au revoir.'</span>; <span class="hljs-error">## Assignment to constant variable</span></code></pre>

## ` alt ` - Altérables
Les altérables sont des variables pouvant être déclarées sans valeur ou sans type. Elles peuvent être résignée mais pas retypé.
<pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">element</span>[<span class="hljs-type">string</span>] = <span class="hljs-string">'Bonjour !'</span>; <span class="hljs-comment">## 'Bonjour !'</span>
<span class="hljs-var_">element</span> = <span class="hljs-string">'Au revoir.'</span>; <span class="hljs-comment">## 'Au revoir !'</span>
<span class="hljs-var_">element</span> = <span class="hljs-number">10</span>; <span class="hljs-error">## Type ‘string’ is not assignable to type ‘number’</span></code></pre>