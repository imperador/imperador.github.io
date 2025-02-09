---
layout: page
title: ‎
nav: false
permalink: /graph/
description: 
---

My (somewhat hidden) Academic genealogy. Using <a href="https://github.com/BenPortner/js_family_tree/tree/master">BenPortner JS Family Tree</a> with open data from the <a href="https://academictree.org/">Academic Tree</a>.
You can also see a <a href="/assets/graph.html">Graphviz version here</a> that uses <a href="https://github.com/pfalcon/wdot" target="_blank">Pfalcon's Wdot</a> .dot file viewer.

<style>
    #fulldiv {
        position: absolute;
        left: 50px;
        width: calc(100% - 100px);
        height: calc(80% - 100px);
        padding: 5px;
        text-align: center;
    }
</style>
<div id="fulldiv" class="col text-justify p-0" >
    <iframe frameborder="1" src="/assets/graphX.html" id="myIframe" style="position: relative; height: 100%; width: 100%;">
    </iframe>
    <a href="/assets/graphX.html" target="_blank">Open a Separate Tab</a>   |   <a href="/assets/graphX.html" target="_blank">Graphviz Version</a> 
</div>

<!--
Options: 
https://github.com/AdeelK93/collapsibleTree
https://gist.github.com/rebeccasc/b4ce160b99aa5316866d6866713d85dd#file-tree-js-L68-L80
-->