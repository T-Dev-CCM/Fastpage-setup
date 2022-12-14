---
keywords: fastai
description: Practice with identifying and correcting code blocks
title: Big Idea 1 'Identifying and Correcting Errors'
layout: default
badges: false
permalink: /collegeboard/error
image: /images/apcsp.png
categories: [1.B, 4.C]
type: ap
week: 7
nb_path: _notebooks/2022-10-03-AP-error_testing.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-03-AP-error_testing.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p><a href="https://apclassroom.collegeboard.org/103/home?unit=1">College Board Big Idea 1</a></p>
<h2 id="Identifying-and-Correcting-Errors-(Unit-1.4)">Identifying and Correcting Errors (Unit 1.4)<a class="anchor-link" href="#Identifying-and-Correcting-Errors-(Unit-1.4)"> </a></h2><blockquote><p>Become familiar with types of errors and strategies to fixing them</p>
<ul>
<li>Lightly Review Videos and take notes on topics with Blog</li>
<li>Complete assigned MCQ questions</li>
</ul>
</blockquote>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Here-are-some-code-segments-you-can-practice-fixing:">Here are some code segments you can practice fixing:<a class="anchor-link" href="#Here-are-some-code-segments-you-can-practice-fixing:"> </a></h1>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">alphabet</span> <span class="o">=</span> <span class="s2">&quot;abcdefghijklmnopqrstuvwxyz&quot;</span>

<span class="n">alphabetList</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">alphabet</span><span class="p">:</span>
    <span class="n">alphabetList</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="n">alphabetList</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[&#39;a&#39;, &#39;b&#39;, &#39;c&#39;, &#39;d&#39;, &#39;e&#39;, &#39;f&#39;, &#39;g&#39;, &#39;h&#39;, &#39;i&#39;, &#39;j&#39;, &#39;k&#39;, &#39;l&#39;, &#39;m&#39;, &#39;n&#39;, &#39;o&#39;, &#39;p&#39;, &#39;q&#39;, &#39;r&#39;, &#39;s&#39;, &#39;t&#39;, &#39;u&#39;, &#39;v&#39;, &#39;w&#39;, &#39;x&#39;, &#39;y&#39;, &#39;z&#39;]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The intended outcome is to determine where the letter is in the alphabet using a while loop</p>
<ul>
<li>There are two changes you can make</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">letter</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What letter would you like to check?&quot;</span><span class="p">)</span>

<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="mi">26</span><span class="p">:</span>
    <span class="k">if</span> <span class="n">alphabetList</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">==</span> <span class="n">letter</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The letter &quot;</span> <span class="o">+</span> <span class="n">letter</span> <span class="o">+</span> <span class="s2">&quot; is the &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">i</span><span class="o">+</span><span class="mi">1</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; letter in the alphabet&quot;</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>The letter b is the 2 letter in the alphabet
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The intended outcome is to determine where the letter is in the alphabet using a for loop</p>
<ul>
<li>There are two changes you can make</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">letter</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What letter would you like to check?&quot;</span><span class="p">)</span> 
   
<span class="n">count</span> <span class="o">=</span> <span class="mi">1</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">alphabetList</span><span class="p">:</span>

    <span class="k">if</span> <span class="n">i</span> <span class="o">==</span> <span class="n">letter</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The letter &quot;</span> <span class="o">+</span> <span class="n">letter</span> <span class="o">+</span> <span class="s2">&quot; is the &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">count</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; letter in the alphabet&quot;</span><span class="p">)</span>
    <span class="n">count</span> <span class="o">+=</span> <span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>The letter z is the 26 letter in the alphabet
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code should output the evens numbers from 0 - 10 using a while loop.</p>
<ul>
<li>How can you change the code to only print the odd numbers in the list?</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">evens</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;=</span> <span class="mi">10</span><span class="p">:</span>
    <span class="n">evens</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">2</span>

<span class="nb">print</span><span class="p">(</span><span class="n">evens</span><span class="p">)</span>    
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_text output_error">
<pre>
<span class="ansi-red-fg">---------------------------------------------------------------------------</span>
<span class="ansi-red-fg">NameError</span>                                 Traceback (most recent call last)
<span class="ansi-green-intense-fg ansi-bold">/home/trey-dev/Fastpage-setup-9/_notebooks/2022-10-03-AP-error_testing.ipynb Cell 10</span> in <span class="ansi-cyan-fg">&lt;cell line: 4&gt;</span><span class="ansi-blue-fg">()</span>
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/trey-dev/Fastpage-setup-9/_notebooks/2022-10-03-AP-error_testing.ipynb#X12sdnNjb2RlLXJlbW90ZQ%3D%3D?line=1&#39;&gt;2&lt;/a&gt;</span> i = 0
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/trey-dev/Fastpage-setup-9/_notebooks/2022-10-03-AP-error_testing.ipynb#X12sdnNjb2RlLXJlbW90ZQ%3D%3D?line=3&#39;&gt;4&lt;/a&gt;</span> while i &lt;= 10:
<span class="ansi-green-fg">----&gt; &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/trey-dev/Fastpage-setup-9/_notebooks/2022-10-03-AP-error_testing.ipynb#X12sdnNjb2RlLXJlbW90ZQ%3D%3D?line=4&#39;&gt;5&lt;/a&gt;</span>     evens.append(numbers[i])
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/trey-dev/Fastpage-setup-9/_notebooks/2022-10-03-AP-error_testing.ipynb#X12sdnNjb2RlLXJlbW90ZQ%3D%3D?line=5&#39;&gt;6&lt;/a&gt;</span>     i += 2
<span class="ansi-green-intense-fg ansi-bold">      &lt;a href=&#39;vscode-notebook-cell://wsl%2Bubuntu/home/trey-dev/Fastpage-setup-9/_notebooks/2022-10-03-AP-error_testing.ipynb#X12sdnNjb2RlLXJlbW90ZQ%3D%3D?line=7&#39;&gt;8&lt;/a&gt;</span> print(evens)

<span class="ansi-red-fg">NameError</span>: name &#39;numbers&#39; is not defined</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code should output the odd numbers from 0 - 10 using a while loop.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">evens</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;=</span> <span class="mi">10</span><span class="p">:</span>
    <span class="n">evens</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">2</span>

<span class="nb">print</span><span class="p">(</span><span class="n">evens</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code should output the evens numbers from 0 - 10 using a for loop.</p>
<ul>
<li>How can you change the code to only print the odd numbers in the list?</li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">6</span><span class="p">,</span><span class="mi">7</span><span class="p">,</span><span class="mi">8</span><span class="p">,</span><span class="mi">9</span><span class="p">,</span><span class="mi">10</span><span class="p">]</span>
<span class="n">evens</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">1</span><span class="p">):</span>
        <span class="n">evens</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">evens</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[1, 3, 5, 7, 9]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>This code should output the odd numbers from 0 - 10 using a for loop.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">6</span><span class="p">,</span><span class="mi">7</span><span class="p">,</span><span class="mi">8</span><span class="p">,</span><span class="mi">9</span><span class="p">,</span><span class="mi">10</span><span class="p">]</span>
<span class="n">evens</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">1</span><span class="p">):</span>
        <span class="n">evens</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">evens</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[1, 3, 5, 7, 9]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>The intended outcome is printing a number between 1 and 100 once, if it is a multiple of 2 or 5</p>
<ul>
<li>3 changes to the code will give the expected outcome. </li>
</ul>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">newNumbers</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;=</span> <span class="mi">100</span><span class="p">:</span>
    <span class="n">numbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="n">numbers</span> <span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="k">pass</span>
    <span class="k">elif</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">5</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="n">newNumbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
    <span class="k">elif</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="n">newNumbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">newNumbers</span><span class="p">)</span> 
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[2, 4, 5, 6, 8, 10, 12, 14, 15, 16, 18, 20, 22, 24, 25, 26, 28, 30, 32, 34, 35, 36, 38, 40, 42, 44, 45, 46, 48, 50, 52, 54, 55, 56, 58, 60, 62, 64, 65, 66, 68, 70, 72, 74, 75, 76, 78, 80, 82, 84, 85, 86, 88, 90, 92, 94, 95, 96, 98, 100]
</pre>
</div>
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">my_Menu</span> <span class="o">=</span>  <span class="p">{</span><span class="s2">&quot;burger&quot;</span><span class="p">:</span> <span class="mf">3.99</span><span class="p">,</span>
            <span class="s2">&quot;fries&quot;</span><span class="p">:</span> <span class="mf">1.99</span><span class="p">,</span>
            <span class="s2">&quot;drink&quot;</span><span class="p">:</span> <span class="mf">0.99</span><span class="p">}</span>  <span class="c1"># define my menu as a dictionary data type, key is the name of food, value is price </span>

<span class="n">price_total</span> <span class="o">=</span> <span class="mi">0</span>  <span class="c1">#set initial value  </span>


<span class="k">for</span> <span class="n">x</span><span class="p">,</span><span class="n">y</span> <span class="ow">in</span> <span class="n">my_Menu</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="s2">&quot;: &quot;</span><span class="p">,</span><span class="s2">&quot;$&quot;</span><span class="p">,</span><span class="n">y</span><span class="p">)</span>


<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Please Select an Item&quot;</span><span class="p">)</span>  <span class="c1">#prompt user input</span>
<span class="n">myUserInput</span> <span class="o">=</span> <span class="s2">&quot;burger&quot;</span>  <span class="c1">#define and set initial value</span>
<span class="n">myUserInput</span> <span class="o">=</span> <span class="nb">input</span><span class="p">()</span> <span class="c1">#define variable to hold user input</span>
<span class="n">myUserOrderKey</span> <span class="o">=</span> <span class="n">myUserInput</span>  <span class="c1">#define and set initial value-- used to print out user&#39;s selected key and value</span>
<span class="n">myCounter</span> <span class="o">=</span> <span class="mi">0</span> <span class="c1">#count through the loop </span>
<span class="n">myError</span> <span class="o">=</span> <span class="s2">&quot;Whoops, try again&quot;</span>

<span class="k">for</span> <span class="n">x</span><span class="p">,</span><span class="n">y</span> <span class="ow">in</span> <span class="n">my_Menu</span><span class="o">.</span><span class="n">items</span><span class="p">():</span> <span class="c1">#loop through my menu</span>
    <span class="k">if</span> <span class="n">x</span> <span class="o">==</span> <span class="n">myUserInput</span><span class="p">:</span> <span class="c1">#if the user input matches a key in my menu dictionary</span>
        <span class="nb">print</span><span class="p">(</span><span class="n">x</span><span class="p">,</span><span class="n">y</span><span class="p">)</span> <span class="c1">#then print the key and value </span>
        <span class="k">break</span> <span class="c1">#stop looping when you get result </span>
    <span class="k">else</span><span class="p">:</span>
       <span class="n">myCounter</span> <span class="o">+=</span> <span class="mi">1</span> 
       <span class="k">if</span> <span class="n">myCounter</span> <span class="o">==</span> <span class="mi">3</span><span class="p">:</span>
            <span class="nb">print</span><span class="p">(</span><span class="n">myError</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>burger :  $ 3.99
fries :  $ 1.99
drink :  $ 0.99
Please Select an Item
burger 3.99
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Hacks">Hacks<a class="anchor-link" href="#Hacks"> </a></h2><blockquote><p>Now is a good time to think about Testing of your teams final project...</p>
<ul>
<li>What errors may arise in your project?</li>
<li>What are some test cases that can be used?</li>
<li>Make sure to document any bugs you encounter and how you solved the problem.</li>
</ul>
</blockquote>

</div>
</div>
</div>
</div>
 

