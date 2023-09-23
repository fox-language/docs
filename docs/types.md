# Les types
---
<table>
  <thead>
    <th>Type</th>
    <th>Description</th>
  </thead>

  <tbody>
    <tr>
      <td class="type"><a href="#/docs/types?id=string" data-id="string" class="anchor">string</a></td>
      <td class="description">Une chaîne de caractère.</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
        <pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">string</span>] = <span class="hljs-keyword">new</span> <span class="hljs-class">String</span>();      <span class="hljs-comment">## ''</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">string</span>];                     <span class="hljs-comment">## ''</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">string</span>] = <span class="hljs-string">'Bonjour'</span>;         <span class="hljs-comment">## 'Bonjour !'</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">string</span>] = <span class="hljs-string">'Bonjour !'</span>;       <span class="hljs-comment">## 'Bonjour !'</span></code></pre>
      </td>
    </tr>
    <tr>
      <td class="type"><a href="#/docs/types?id=number" data-id="number" class="anchor">number</a></td>
      <td class="description">Un nombre entier ou décimal</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
          <pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">number</span>] = <span class="hljs-keyword">new</span> <span class="hljs-class">Number</span>();      <span class="hljs-comment">## 0</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">number</span>];                     <span class="hljs-comment">## 0</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">number</span>] = <span class="hljs-string">1.1</span>;               <span class="hljs-comment">## 1.1</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">number</span>] = <span class="hljs-string">.5</span>;                <span class="hljs-comment">## 0.5</span></code></pre>
        </td>
    </tr>
    <tr>
      <td class="type"><a href="#/docs/types?id=boolean" data-id="boolean" class="anchor">boolean</a></td>
      <td class="description">Une valeur vrai ou fausse</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
          <pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">boolean</span>] = <span class="hljs-keyword">new</span> <span class="hljs-class">Boolean</span>();    <span class="hljs-comment">## false</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">boolean</span>];                    <span class="hljs-comment">## false</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">boolean</span>] = <span class="hljs-string">false</span>;            <span class="hljs-comment">## false</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">boolean</span>] = <span class="hljs-string">true</span>;             <span class="hljs-comment">## true</span></code></pre>
        </td>
    </tr>
    <tr>
      <td class="type"><a href="#/docs/types?id=null" data-id="null" class="anchor">null</a></td>
      <td class="description">Une valeur null</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
          <pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">null</span>];                       <span class="hljs-comment">## null</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">null</span>] = <span class="hljs-string">null</span>;                <span class="hljs-comment">## null</span></code></pre>
        </td>
    </tr>
    <tr>
      <td class="type"><a href="#/docs/types?id=undefined" data-id="undefined" class="anchor">undefined</a></td>
      <td class="description">Une valeur non définie</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
          <pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">undefined</span>];                  <span class="hljs-comment">## undefined</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">undefined</span>] = <span class="hljs-string">undefined</span>;      <span class="hljs-comment">## undefined</span></code></pre>
        </td>
    </tr>
    <tr>
      <td class="type"><a href="#/docs/types?id=object" data-id="object" class="anchor">object</a></td>
      <td class="description">Un objet qui peut stocker d'autre type avec des "clé" et des "valeurs"</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
          <pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">object</span>] = <span class="hljs-keyword">new</span> <span class="hljs-class">Object</span>();      <span class="hljs-comment">## { }</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">object</span>];                     <span class="hljs-comment">## { }</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">object</span>] = <span class="hljs-string">{ }</span>;               <span class="hljs-comment">## { }</span></code></pre>
      </td>
    </tr>
    <tr>
      <td class="type"><a href="#/docs/types?id=array" data-id="array" class="anchor">array</a></td>
      <td class="description">Un tableau pouvant stocker d'autre type et accessible via des index</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
        <pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">array</span>] = <span class="hljs-keyword">new</span> <span class="hljs-class">Array</span>();        <span class="hljs-comment">## [ ]</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">array</span>];                      <span class="hljs-comment">## [ ]</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">array</span>] = [ ];                <span class="hljs-comment">## [ ]</span></code></pre>
      </td>
    </tr>
    <tr>
      <td class="type"><a href="#/docs/types?id=function" data-id="function" class="anchor">function</a></td>
      <td class="description">Un fonction pouvant simplifier des taches répétitives</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
        <pre data-lang="fox"><code><span class="hljs-keyword">function</span> <span class="hljs-var_">x</span>() { <span class="hljs-comment"># ... #</span> }</code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">function</span>] = <span class="hljs-keyword">function</span>() { <span class="hljs-comment"># ... #</span> }</code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">function</span>] = () => { <span class="hljs-comment"># ... #</span> }</code></pre>
      </td>
    </tr>
    <tr>
      <td class="type"><a href="#/docs/types?id=date" data-id="date" class="anchor">date</a></td>
      <td class="description">Un moyen d'interagir avec les timestamps</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
        <pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[<span class="hljs-type">date</span>] = <span class="hljs-keyword">new</span> <span class="hljs-class">Date</span>();         <span class="hljs-comment">## Sat Sep 23 2023 17:16:19 GMT+0200</span></code></pre>
      </td>
    </tr>
    <tr>
      <td class="type"><a href="#/docs/types?id=auto" data-id="auto" class="anchor">auto</a></td>
      <td class="description">Un moyen de typer rapidement et automatiquement</td>
    </tr>
    <tr>
      <td class="code" colspan=3>
        <pre data-lang="fox"><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[] = <span class="hljs-string">'Bonjour !'</span>;            <span class="hljs-comment">## typeof = string</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[] = <span class="hljs-number">12</span>;                     <span class="hljs-comment">## typeof = number</span></code><code><span class="hljs-keyword">alt</span> <span class="hljs-var_">x</span>[] = { };                    <span class="hljs-comment">## typeof = object</span></code></pre>
      </td>
    </tr>
  </tbody>
</table>