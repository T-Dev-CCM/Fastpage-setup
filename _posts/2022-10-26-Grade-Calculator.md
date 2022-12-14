---
keywords: fastai
description: A discussion on user inputs using Javascript. The grade calculator takes multiple values and does a calculation on them. User input can be useful for other projects, such as being used as a query.
title: Javascript Inputs using a Grade Calculator
comments: false
permalink: /techtalk/javascriptinput
categories: [3.A, 5.B, C3.0, C3.1, C4.1]
type: pbl
week: 10
nb_path: _notebooks/2022-10-26-Grade-Calculator.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-26-Grade-Calculator.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">&lt;</span><span class="n">div</span> <span class="n">class</span><span class="o">=</span><span class="s2">&quot;container bg-primary&quot;</span><span class="o">&gt;</span>
    <span class="o">&lt;</span><span class="n">header</span> <span class="n">class</span><span class="o">=</span><span class="s2">&quot;pb-3 mb-4 border-bottom border-primary text-dark&quot;</span><span class="o">&gt;</span>
        <span class="o">&lt;</span><span class="n">span</span> <span class="n">class</span><span class="o">=</span><span class="s2">&quot;fs-4&quot;</span><span class="o">&gt;</span><span class="n">Grade</span> <span class="n">Calculator</span><span class="o">&lt;/</span><span class="n">span</span><span class="o">&gt;</span>
    <span class="o">&lt;/</span><span class="n">header</span><span class="o">&gt;</span>
        <span class="o">&lt;</span><span class="n">form</span><span class="o">&gt;</span>
        <span class="o">&lt;!</span>-- Totals --&gt;
        <span class="o">&lt;</span><span class="n">div</span> <span class="n">class</span><span class="o">=</span><span class="s2">&quot;form-group row&quot;</span><span class="o">&gt;</span>
            <span class="n">Total</span> <span class="p">:</span> <span class="o">&lt;</span><span class="n">span</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;total&quot;</span> <span class="n">class</span><span class="o">=</span><span class="s2">&quot;label label-primary&quot;</span><span class="o">&gt;</span><span class="mf">0.0</span><span class="o">&lt;/</span><span class="n">span</span><span class="o">&gt;</span>
            <span class="n">Count</span> <span class="p">:</span> <span class="o">&lt;</span><span class="n">span</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;count&quot;</span> <span class="n">class</span><span class="o">=</span><span class="s2">&quot;label label-primary&quot;</span><span class="o">&gt;</span><span class="mf">0.0</span><span class="o">&lt;/</span><span class="n">span</span><span class="o">&gt;</span>
            <span class="n">Average</span> <span class="p">:</span> <span class="o">&lt;</span><span class="n">span</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;average&quot;</span> <span class="n">class</span><span class="o">=</span><span class="s2">&quot;label label-primary&quot;</span><span class="o">&gt;</span><span class="mf">0.0</span><span class="o">&lt;/</span><span class="n">span</span><span class="o">&gt;</span>
        <span class="o">&lt;/</span><span class="n">div</span><span class="o">&gt;</span>
        <span class="o">&lt;!</span>-- Rows --&gt;
        <span class="o">&lt;</span><span class="n">div</span> <span class="n">class</span><span class="o">=</span><span class="s2">&quot;form-group row&quot;</span><span class="o">&gt;</span>
            <span class="n">Input</span> <span class="n">scores</span><span class="p">,</span> <span class="n">press</span> <span class="n">tab</span> <span class="n">to</span> <span class="n">add</span> <span class="n">new</span> <span class="n">number</span><span class="p">:</span>
            <span class="o">&lt;</span><span class="n">div</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;scores&quot;</span><span class="o">&gt;</span>
                <span class="o">&lt;</span><span class="nb">input</span> <span class="n">onblur</span><span class="o">=</span><span class="s2">&quot;calculator()&quot;</span> <span class="nb">type</span><span class="o">=</span><span class="s2">&quot;text&quot;</span> <span class="n">name</span><span class="o">=</span><span class="s2">&quot;score&quot;</span> <span class="nb">id</span><span class="o">=</span><span class="s2">&quot;score0&quot;</span><span class="o">/&gt;&lt;</span><span class="n">br</span><span class="o">&gt;</span>
                <span class="o">&lt;!</span>-- javascript generated inputs --&gt;
            <span class="o">&lt;/</span><span class="n">div</span><span class="o">&gt;</span>
        <span class="o">&lt;/</span><span class="n">div</span><span class="o">&gt;</span>
    <span class="o">&lt;/</span><span class="n">form</span><span class="o">&gt;</span>
<span class="o">&lt;/</span><span class="n">div</span><span class="o">&gt;</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">const</span> <span class="n">scoresContainer</span> <span class="o">=</span> <span class="n">document</span><span class="o">.</span><span class="n">getElementById</span><span class="p">(</span><span class="s2">&quot;scores&quot;</span><span class="p">);</span>

<span class="o">//</span> <span class="n">Creates</span> <span class="n">new</span> <span class="nb">input</span> <span class="n">line</span>
<span class="n">function</span> <span class="n">newInputLine</span><span class="p">(</span><span class="n">index</span><span class="p">)</span> <span class="p">{</span>
    <span class="o">//</span> <span class="n">Prepare</span> <span class="n">new</span> <span class="nb">input</span> <span class="n">line</span>
    <span class="n">var</span> <span class="nb">input</span> <span class="o">=</span> <span class="n">document</span><span class="o">.</span><span class="n">createElement</span><span class="p">(</span><span class="s2">&quot;input&quot;</span><span class="p">);</span>  <span class="o">//</span> <span class="nb">input</span> <span class="n">element</span>
    <span class="n">var</span> <span class="n">br</span> <span class="o">=</span> <span class="n">document</span><span class="o">.</span><span class="n">createElement</span><span class="p">(</span><span class="s2">&quot;br&quot;</span><span class="p">);</span>  <span class="o">//</span> <span class="n">line</span> <span class="k">break</span> <span class="n">element</span>
    <span class="o">//</span> <span class="n">Setup</span> <span class="nb">input</span> <span class="n">line</span> <span class="n">attributes</span>
    <span class="nb">input</span><span class="o">.</span><span class="n">setAttribute</span><span class="p">(</span><span class="s1">&#39;onblur&#39;</span><span class="p">,</span> <span class="s2">&quot;calculator()&quot;</span><span class="p">);</span>
    <span class="nb">input</span><span class="o">.</span><span class="n">setAttribute</span><span class="p">(</span><span class="s1">&#39;type&#39;</span><span class="p">,</span> <span class="s2">&quot;text&quot;</span><span class="p">);</span>
    <span class="nb">input</span><span class="o">.</span><span class="n">setAttribute</span><span class="p">(</span><span class="s1">&#39;name&#39;</span><span class="p">,</span> <span class="s2">&quot;score&quot;</span><span class="p">);</span>
    <span class="nb">input</span><span class="o">.</span><span class="n">setAttribute</span><span class="p">(</span><span class="s1">&#39;id&#39;</span><span class="p">,</span> <span class="s2">&quot;score&quot;</span> <span class="o">+</span> <span class="n">index</span><span class="p">);</span>
    <span class="o">//</span> <span class="n">Add</span> <span class="nb">input</span> <span class="ow">and</span> <span class="n">line</span> <span class="k">break</span> <span class="n">to</span> <span class="n">page</span>
    <span class="n">scoresContainer</span><span class="o">.</span><span class="n">appendChild</span><span class="p">(</span><span class="nb">input</span><span class="p">);</span>
    <span class="n">scoresContainer</span><span class="o">.</span><span class="n">appendChild</span><span class="p">(</span><span class="n">br</span><span class="p">);</span>
<span class="p">}</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="o">//</span> <span class="n">Calculates</span> <span class="n">totals</span>
<span class="n">function</span> <span class="n">calculator</span><span class="p">(){</span>
    <span class="n">var</span> <span class="n">array</span> <span class="o">=</span> <span class="n">document</span><span class="o">.</span><span class="n">getElementsByName</span><span class="p">(</span><span class="s1">&#39;score&#39;</span><span class="p">);</span> <span class="o">//</span> <span class="n">setup</span> <span class="n">array</span> <span class="n">of</span> <span class="n">scores</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">array</span><span class="p">[</span><span class="n">array</span><span class="o">.</span><span class="n">length</span><span class="o">-</span><span class="mi">1</span><span class="p">]</span><span class="o">.</span><span class="n">value</span><span class="o">.</span><span class="n">length</span> <span class="o">!=</span> <span class="mi">0</span><span class="p">)</span> <span class="p">{</span>   <span class="o">//</span> <span class="nb">input</span> <span class="n">cell</span> <span class="n">has</span> <span class="n">a</span> <span class="n">value</span>
        <span class="o">//</span> <span class="n">algorithm</span> <span class="n">to</span> <span class="n">calculate</span> <span class="n">results</span>
        <span class="n">var</span> <span class="n">total</span> <span class="o">=</span> <span class="mi">0</span><span class="p">;</span>  <span class="o">//</span> <span class="n">running</span> <span class="n">total</span>
        <span class="k">for</span><span class="p">(</span><span class="n">var</span> <span class="n">i</span> <span class="o">=</span> <span class="mi">0</span><span class="p">;</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="n">array</span><span class="o">.</span><span class="n">length</span><span class="p">;</span> <span class="n">i</span><span class="o">++</span><span class="p">){</span>  <span class="o">//</span> <span class="n">iterate</span> <span class="n">through</span> <span class="n">array</span>
            <span class="k">if</span><span class="p">(</span><span class="n">parseFloat</span><span class="p">(</span><span class="n">array</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">value</span><span class="p">))</span>  <span class="o">//</span> <span class="n">convert</span> <span class="n">to</span> <span class="nb">float</span>
                <span class="n">total</span> <span class="o">+=</span> <span class="n">parseFloat</span><span class="p">(</span><span class="n">array</span><span class="p">[</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">value</span><span class="p">);</span>  <span class="o">//</span> <span class="n">add</span> <span class="n">to</span> <span class="n">running</span> <span class="n">total</span>
        <span class="p">}</span>
        <span class="o">//</span> <span class="n">update</span> <span class="n">totals</span>
        <span class="n">document</span><span class="o">.</span><span class="n">getElementById</span><span class="p">(</span><span class="s1">&#39;total&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">innerHTML</span> <span class="o">=</span> <span class="n">total</span><span class="o">.</span><span class="n">toFixed</span><span class="p">(</span><span class="mi">2</span><span class="p">);</span>
        <span class="n">document</span><span class="o">.</span><span class="n">getElementById</span><span class="p">(</span><span class="s1">&#39;count&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">innerHTML</span> <span class="o">=</span> <span class="n">array</span><span class="o">.</span><span class="n">length</span><span class="p">;</span>
        <span class="n">document</span><span class="o">.</span><span class="n">getElementById</span><span class="p">(</span><span class="s1">&#39;average&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">innerHTML</span> <span class="o">=</span> <span class="p">(</span><span class="n">total</span> <span class="o">/</span> <span class="n">array</span><span class="o">.</span><span class="n">length</span><span class="p">)</span><span class="o">.</span><span class="n">toFixed</span><span class="p">(</span><span class="mi">2</span><span class="p">);</span>
        <span class="o">//</span> <span class="n">make</span> <span class="n">a</span> <span class="n">new</span> <span class="nb">input</span> <span class="n">line</span>
        <span class="n">newInputLine</span><span class="p">(</span><span class="n">array</span><span class="o">.</span><span class="n">length</span><span class="p">);</span>
        
    <span class="p">}</span>
    <span class="o">//</span> <span class="n">Set</span> <span class="n">cursor</span> <span class="n">focus</span> <span class="n">on</span> <span class="n">last</span> <span class="n">element</span><span class="p">;</span> <span class="n">this</span> <span class="n">could</span> <span class="n">be</span> <span class="n">new</span> <span class="ow">or</span> <span class="n">unchanged</span> <span class="n">element</span>
    <span class="n">document</span><span class="o">.</span><span class="n">getElementById</span><span class="p">(</span><span class="s2">&quot;score&quot;</span> <span class="o">+</span> <span class="p">(</span><span class="n">array</span><span class="o">.</span><span class="n">length</span><span class="o">-</span><span class="mi">1</span><span class="p">))</span><span class="o">.</span><span class="n">focus</span><span class="p">();</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

</div>
 

