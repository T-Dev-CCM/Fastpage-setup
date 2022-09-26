---
keywords: fastai
title: Curse of the Python
nb_path: _notebooks/2022-09-23-Adventure-Game.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-09-23-Adventure-Game.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span> 
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
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">getpass</span><span class="o">,</span> <span class="nn">sys</span>

<span class="k">def</span> <span class="nf">question_with_response</span><span class="p">(</span><span class="n">prompt</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span> <span class="n">prompt</span><span class="p">)</span>
    <span class="n">msg</span> <span class="o">=</span> <span class="nb">input</span><span class="p">()</span>
    <span class="k">return</span> <span class="n">msg</span>


<span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Hello, User&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Welcome to Curse of The Python, where your inputs will forge the output on your quest to escape&quot;</span><span class="p">)</span>
<span class="n">rsp</span> <span class="o">=</span> <span class="n">question_with_response</span><span class="p">(</span><span class="s2">&quot;Are you ready to embark on your adventure? Type Y or N&quot;</span><span class="p">)</span>




<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Y&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Very Well...&quot;</span><span class="p">)</span> 
    <span class="n">rsp</span> <span class="o">=</span> <span class="n">question_with_response</span><span class="p">(</span><span class="s2">&quot;Press Enter to Continue&quot;</span><span class="p">)</span>


<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;N&quot;</span><span class="p">:</span> 
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Perhaps another time then...&quot;</span><span class="p">)</span>

<span class="k">else</span><span class="p">:</span> 
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Sorry, I didn&#39;t get that, look at your choices and try again&quot;</span><span class="p">)</span>

<span class="n">rsp</span> <span class="o">=</span> <span class="n">question_with_response</span><span class="p">(</span><span class="s2">&quot;You wake up on the stone floor in a temple, as you drearily make your way to your feet, you see a python insignia staring at you, there are 3 doors, one made of wood, one made of rusty metal, and one with a skull painted on it. Which do you choose?&quot;</span><span class="p">)</span>


<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Wood&quot;</span><span class="p">:</span> 
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;You go through the room behind the wooden door, the creaking only being absorbed by the emptiness within it...except for some writing on the wall. Read it?&quot;</span><span class="p">)</span> 
    <span class="n">rsp</span> <span class="o">=</span> <span class="n">question_with_response</span> <span class="p">(</span><span class="s2">&quot;Read? or Don&#39;t?&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Don&#39;t&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Really? what else will you do?&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Read&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The text reads: &#39;I sing but never talk, Always run but don&#39;t walk, I have hands, but no arms, and a face, but no head&#39;&quot;</span><span class="p">)</span>
    <span class="n">rsp</span> <span class="o">=</span> <span class="n">question_with_response</span> <span class="p">(</span><span class="s2">&quot;What could the answer be?&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Clock&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;As you mutter the answer to yourself, you hear a little crumble, and as you say it again, the walls move slightly, showing the outside world. Then as you yell it one more time, the walls open completely, and you run outside&quot;</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;You got the intellect ending&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Metal&quot;</span><span class="p">:</span> 
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;As you push your weight against the door, it slowly creaks open as you stumble into the dimly lit room it holds. As you make your way in, you see a snake stuck in a cage with the key outside. The snake looks like it wants you to free it&quot;</span><span class="p">)</span>
    <span class="n">rsp</span> <span class="o">=</span> <span class="n">question_with_response</span> <span class="p">(</span><span class="s2">&quot;Free? or Leave?&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Leave&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Sensing your abandonment, the snake then spews venom at you, causing you to&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Free&quot;</span><span class="p">:</span> 
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The snake sees your moral kindness as you free it from the cage, and as it slithers away through a crevice, the room begins to shake as the stone walls open revealing the outside world.&quot;</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;You got the Compassion Ending&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Skull&quot;</span><span class="p">:</span> 
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The Door opens with relative ease, but upon setting foot in the room, spikes begin to come from the ceiling! As you observe what will be you impending doom, you notice a bone and a stick in the corner. Perhaps using one of these can save your life!&quot;</span><span class="p">)</span>
    <span class="n">rsp</span> <span class="o">=</span> <span class="n">question_with_response</span><span class="p">(</span><span class="s2">&quot;What do you reach for, Stick? or Bone?&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Stick&quot;</span><span class="p">:</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;You put the stick in between the floor and the ceiling, but the stick breaks under the pressure, and with that, you fell victim to the python&#39;s curse. Game over&quot;</span><span class="p">)</span>

<span class="k">if</span> <span class="n">rsp</span> <span class="o">==</span> <span class="s2">&quot;Bone&quot;</span><span class="p">:</span> 
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Thankfully, the bone withstood the pressure of the ceiling, and after attempting to crush you, it retracts, revealing a ladder up to the outside&quot;</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;You got the Near-Death Ending&quot;</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Hello, User
Welcome to Curse of The Python, where your inputs will forge the output on your quest to escape
Are you ready to embark on your adventure? Type Y or N
Sorry, I didn&#39;t get that, look at your choices and try again
You wake up on the stone floor in a temple, as you drearily make your way to your feet, you see a python insignia staring at you, there are 3 doors, one made of wood, one made of rusty metal, and one with a skull painted on it. Which do you choose?
You go through the room behind the wooden door, the creaking only being absorbed by the emptiness within it...except for some writing on the wall. Read it?
Read? or Don&#39;t?
The text reads: &#39;I sing but never talk, Always run but don&#39;t walk, I have hands, but no arms, and a face, but no head&#39;
What could the answer be?
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
