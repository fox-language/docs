# Les modules
Un module permet d'exporter ou importer des fonctions, des classes, de la data ou une interface entre différents fichiers.

## Définir un module
Vous pouvez déclarer un module afin de l'exporter où vous souhaitez.
A l'intérieur du fichier, vous pouvez utiliser le nom de votre module pour pouvoir l'utiliser à l'intérieur à votre guise qu'importe la méthode.
Le Type défini qu'est ce que le module exporte. La méthode féini s'il est accessible en dehors du module et le Name est le nom unique que vous lui donnez.
<pre data-lang="fox">
<code><span class="hljs-keyword">export module</span>[<span class="hljs-type">type</span>] (<span class="hljs-keyword">method</span>) <span class="hljs-class">Name</span> {
  <span class="hljs-comment"># ... #</span>
};
</code></pre>

## Types de module

<table>
  <thead>
    <th>Type</th>
    <th>Description</th>
  </thead>
  <tbody>
    <tr>
      <td>Data</td>
      <td>Ce type de module permet d'exporter des données à l'intérieur ou l'exterieur du module.</td>
    </tr>
    <tr>
      <td colspan=2 class="code"><pre data-lang="fox"><code><span class="hljs-keyword">export module</span>[<span class="hljs-type">data</span>] (<span class="hljs-keyword">public</span>) <span class="hljs-class">Data</span> {<br>  <span class="hljs-attr">name</span>: <span class="hljs-string">'Bastos'</span>,<br>  <span class="hljs-attr">surname</span>: <span class="hljs-string">'F.'</span>,<br>  <span class="hljs-attr">old</span>: <span class="hljs-number">17</span><br>};</code></pre>
      </td>
    </tr>
    <tr>
      <td>Function</td>
      <td>Ce type de module permet d'exporter des données à l'intérieur ou l'exterieur du module.</td>
    </tr>
    <tr>
      <td colspan=2 class="code"><pre data-lang="fox"><code><span class="hljs-keyword">export module</span>[<span class="hljs-type">data</span>] (<span class="hljs-keyword">public</span>) <span class="hljs-class"><span class="hljs-function">myFunction</span></span>(<span class="hljs-var_">args</span>[<span class="hljs-type">number</span>]) {<br>  <span class=hljs-keyword>return</span> [<span class="hljs-var_">args</span>];<br>};</code></pre>
      </td>
    <tr>
      <td>Class</td>
      <td>Ce module permet l’export d’une classe utilisable à l’intérieur ou l'extérieur du module en fonction de sa méthode.</td>
    </tr>
    <tr>
      <td colspan=2 class="code">
        <pre data-lang="fox"><code><span class="hljs-keyword">export module</span>[<span class="hljs-type">class</span>] (<span class="hljs-keyword">public</span>) <span class="hljs-class">MaClass</span> {<br>  <span class="hljs-keyword">constructor</span>(<span class="hljs-var_">args</span>) {<br>    <span class="hljs-keyword">this</span>.<span class="hljs-attr">args</span> = <span class="hljs-var_">args</span>;<br>  };<br>};</code></pre>
      </td>
    </tr>
      <td>Interfaces</td>
      <td>Ce module permet l’export d’une interface servant à typer les objets.</td>
    </tr>
    <tr>
      <td colspan=2 class="code">
        <pre data-lang="fox"><code><span class="hljs-keyword">export module</span>[<span class="hljs-type">interface</span>] (<span class="hljs-keyword">public</span>) <span class="hljs-interface">monType</span> {<br>    <span class="hljs-attr">id</span>[<span class="hljs-type">number</span>],<br>    <span class="hljs-attr">name</span>[<span class="hljs-type">string</span>],<br>    <span class="hljs-attr">old</span>?[<span class="hljs-type">number</span>],<br>    <span class="hljs-attr">birthday</span>[<span class="hljs-type">date</span> || <span class="hljs-type">string</span>],<br>    <span class="hljs-attr">hobbies</span>[<span class="hljs-type">array</span>&#60;<span class="hljs-type">string</span>&#62;],<br>    <span class="hljs-attr">friends</span>[<span class="hljs-type">array</span>&#60;<span class="hljs-type">autreInterface</span>&#62;],<br>};<br></code></pre>
      </td>
    </tr>
  </tbody>
</table>

## Méthodes
<table>
  <thead>
    <th>Type</th>
    <th>Description</th>
  </thead>
  <tbody>
    <tr>
      <td>Public</td>
      <td>Cette méthode permet l'usage du module avec un import.</td>
    </tr>
    <tr>
      <td colspan=2 class="code">
        <pre data-lang="fox"><code><span class="hljs-keyword">export</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">data</span>] (<span class="hljs-keyword">public</span>) <span class="hljs-data">Data</span> {<br>    <span class="hljs-attr">value</span>: <span class="hljs-string">'Bonjour !'</span>,<br>};<br><br><span class="hljs-keyword">export</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">function</span>] (<span class="hljs-keyword">public</span>) <span class="hljs-function"><span class="hljs-function">myFunction</span></span>() {<br>    <span class="hljs-class">Console</span>.<span class="hljs-class">log</span>(<span class="hljs-class">Data</span>.<span class="hljs-attr">value</span>);<br>};</code></pre>
      </td>
    </tr>
    <tr>
      <td colspan=2 class="code">
        <pre data-lang="fox"><code><span class="hljs-keyword">import</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">data</span>] { <span class="hljs-data">Data</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./fichier.fox'</span>;<br><span class="hljs-keyword">import</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">function</span>] { <span class="hljs-function"><span class="hljs-function">myFunction</span></span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./fichier.fox'</span>;<br><br><span class="hljs-class">Console</span>.<span class="hljs-class">log</span>(<span class="hljs-class">Data</span>.<span class="hljs-attr">value</span>);      <span class="hljs-comment">## 'Bonjour !'</span><br><span class="hljs-function"><span class="hljs-function">myFunction</span></span>();                 <span class="hljs-comment">## 'Bonjour !'</span></code></pre>
      </td>
    </tr>
    <tr>
      <td>Private</td>
      <td>Cette méthode ne permet pas l'usage du module en dehors de ce dernier.</td>
    </tr>
    <tr>
      <td colspan=2 class="code">
        <pre data-lang="fox"><code><span class="hljs-keyword">export</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">data</span>] (<span class="hljs-keyword">private</span>) <span class="hljs-data">Data</span> {<br>    <span class="hljs-attr">value</span>: <span class="hljs-string">'Bonjour !'</span>,<br>};<br><br><span class="hljs-keyword">export</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">function</span>] (<span class="hljs-keyword">public</span>) <span class="hljs-function"><span class="hljs-function">myFunction</span></span>() {<br>    <span class="hljs-class">Console</span>.<span class="hljs-class">log</span>(<span class="hljs-class">Data</span>.<span class="hljs-attr">value</span>);<br>};</code></pre>
      </td>
    </tr>
    <tr>
      <td colspan=2 class="code">
        <pre data-lang="fox"><code><span class="hljs-keyword">import</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">data</span>] { <span class="hljs-data">Data</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./fichier.fox'</span>;<br><span class="hljs-keyword">import</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">function</span>] { <span class="hljs-function"><span class="hljs-function">myFunction</span></span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./fichier.fox'</span>;<br><br><span class="hljs-class">Console</span>.<span class="hljs-class">log</span>(<span class="hljs-class">Data</span>.<span class="hljs-attr">value</span>);      <span class="hljs-error">## Cannot access to module ‘Data’ because it's private.</span><br><span class="hljs-function"><span class="hljs-function">myFunction</span></span>();                 <span class="hljs-comment">## 'Bonjour !'</span></code></pre>
      </td>
    </tr>
  </tbody>
</table>

## Import
Les imports sont relativement simple et suivent le même paterne. Vous pouvez ainsi importer des modules : Données, fonctions, classes et interfaces.
<pre data-lang="fox"><code><span class="hljs-comment">## ./fichier.fox</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">module</span>[data] (<span class="hljs-keyword">public</span>) <span class="hljs-data">Data1</span> {
  <span class="hljs-attr">value</span>: <span class="hljs-string">'Bonjour ! '</span>,
};

<span class="hljs-keyword">export</span> <span class="hljs-keyword">module</span>[data] (<span class="hljs-keyword">public</span>) <span class="hljs-data">Data2</span> {
  <span class="hljs-attr">value</span>: <span class="hljs-string">'Au revoir !'</span>,
};

<span class="hljs-keyword">export</span> <span class="hljs-keyword">module</span>[function] (<span class="hljs-keyword">public</span>) <span class="hljs-function">myFunction</span>() {
  <span class="hljs-keyword">return</span> 'Bonne journée !';
};
</code></pre>

<pre data-lang="fox"><code><span class="hljs-comment">## ./index.fox</span>
<span class="hljs-keyword">import</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">data</span>] { <span class="hljs-data">Data1</span>, <span class="hljs-data">Data2</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./fichier.fox'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">function</span>] { <span class="hljs-function">myFunction</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./fichier.fox'</span>;
<span class="hljs-data">Data1</span>.<span class="hljs-attr">value</span>;                 <span class="hljs-comment">## Bonjour !</span>
<span class="hljs-data">Data2</span>.<span class="hljs-attr">value</span>;                 <span class="hljs-comment">## Au revoir !</span>
<span class="hljs-function">myFunction</span>();                <span class="hljs-comment">## Bonne jounrée !</span>
<span class="hljs-comment">## ---</span>
<span class="hljs-keyword">import</span> <span class="hljs-keyword">module</span>[<span class="hljs-var_">*</span>] modules <span class="hljs-keyword">from</span> <span class="hljs-string">'./fichier.fox'</span>;
modules.<span class="hljs-data">Data1</span>.<span class="hljs-attr">value</span>;         <span class="hljs-comment">## Bonjour !</span>
modules.<span class="hljs-data">Data2</span>.<span class="hljs-attr">value</span>;         <span class="hljs-comment">## Au revoir !</span>
modules.<span class="hljs-function">myFunction</span>();        <span class="hljs-comment">## Bonne journée !</span>
<span class="hljs-comment">## ---</span>
<span class="hljs-keyword">import</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">data</span>] datas <span class="hljs-keyword">from</span> <span class="hljs-string">'./fichier.fox'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-keyword">module</span>[<span class="hljs-type">function</span>] functions <span class="hljs-keyword">from</span> <span class="hljs-string">'./fichier.fox'</span>;
data.<span class="hljs-data">Data1</span>.<span class="hljs-attr">value</span>;            <span class="hljs-comment">## Bonjour !</span>
data.<span class="hljs-data">Data2</span>.<span class="hljs-attr">value</span>;            <span class="hljs-comment">## Au revoir !</span>
functions.<span class="hljs-function">myFunction</span>();      <span class="hljs-comment">## Bonne journée !</span>
</code></pre>
