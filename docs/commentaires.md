# Les commentaire
Les commentaires permettent de préciser des informations sur votre code, décrire des blocks, retirer temporairement du code mais aussi documenter.
---
## `##` - Simples
Ce commentaire est placé à la fin d'une ligne de code ou au début. Tout ce qui se trouve après jusqu'au prochain saut de ligne est ignoré.
<pre data-lang="fox"><code><span class="hljs-keyword">const</span> <span class="hljs-var_">element</span>[<span class="hljs-type">string</span>] = <span class="hljs-string">'Bonjour !'</span>; <span class="hljs-comment">## Ceci est un commentaire</span></code></pre>

## `# ... #` - Complexes
Ce commentaire dit "complexe" peut être glissé n'importe où dans le code. Vous pouvez écrire dedans et continuer votre code après. Tout ce qui se trouve entre les "#" sera
<pre data-lang="fox"><code><span class="hljs-keyword">const</span> <span class="hljs-var_">element</span>[<span class="hljs-type">string</span>] <span class="hljs-comment"># Ceci est un commentaire #</span> = <span class="hljs-string">'Bonjour !'</span>;</code></pre>


## `###` - Documentaires
Ce commentaire permet de documenter votr code. Il peut être utilisé pour réaliser des documentations.
<pre data-lang="fox"><code><span class="hljs-comment">### Commentaire quelconque</span>
<span class="hljs-comment">### <span class="hljs-keyword">@description</span> Cette fonction retourne l'argument dans un array</span>
<span class="hljs-comment">### <span class="hljs-keyword">@params</span> <span class="hljs">[ <span class="hljs-type">number</span> ] argument</span></span>
<span class="hljs-comment">### <span class="hljs-keyword">@return</span> <span class="hljs">[ <span class="hljs-type">array</span>&#60;<span class="hljs-type">number</span>&#62; ]</span></span>
<span class="hljs-keyword">function</span> <span class="hljs-var_">x</span>(<span class="hljs-var_">args</span>[<span class="hljs-type">number</span>]) {
  <span class="hljs-keyword">return</span> [<span class="hljs-var_">args</span>];
};
</code></pre>
