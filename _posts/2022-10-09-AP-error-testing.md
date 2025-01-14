---
keywords: fastai
description: Practice with identifying and correcting code blocks
title: Identifying and Correcting Errors
toc: true
categories: [Jupyter, Trimester 1, Tri 1 Assignments]
comments: true
nb_path: _notebooks/2022-10-09-AP-error-testing.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-10-09-AP-error-testing.ipynb
-->

<div class="container" id="notebook-container">
        
<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Alphabet-List:">Alphabet List:<a class="anchor-link" href="#Alphabet-List:"> </a></h2>
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
<h2 id="Alphabet-Numbering:-While-Loop">Alphabet Numbering: While Loop<a class="anchor-link" href="#Alphabet-Numbering:-While-Loop"> </a></h2>
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
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;The letter &quot;</span> <span class="o">+</span> <span class="n">letter</span> <span class="o">+</span> <span class="s2">&quot; is the &quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">i</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot; letter in the alphabet&quot;</span><span class="p">)</span> <span class="c1">#adds 1 to the number that is counted by the program to make the number outputted true</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>The letter a is the 1 letter in the alphabet
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Alphabet-Numbering-System:-Count">Alphabet Numbering System: Count<a class="anchor-link" href="#Alphabet-Numbering-System:-Count"> </a></h2>
</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">letter</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;What letter would you like to check?&quot;</span><span class="p">)</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">alphabetList</span><span class="p">:</span>
    <span class="n">count</span> <span class="o">=</span> <span class="mi">1</span> <span class="c1"># counting is started at 1 instead of 0</span>
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
<pre>The letter a is the 1 letter in the alphabet
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Number-List:-While-Loop">Number List: While Loop<a class="anchor-link" href="#Number-List:-While-Loop"> </a></h2>
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
    <span class="n">evens</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">2</span>

<span class="nb">print</span><span class="p">(</span><span class="n">evens</span><span class="p">)</span>    
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[0, 2, 4, 6, 8, 10]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Outputting odd numbers:</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">odds</span> <span class="o">=</span> <span class="p">[]</span>
<span class="n">i</span> <span class="o">=</span> <span class="mi">0</span>

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;=</span> <span class="mi">10</span><span class="p">:</span>
    <span class="n">odds</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span> <span class="c1"># starts at 1 instead of 0 to give odd numbers</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">2</span>

<span class="nb">print</span><span class="p">(</span><span class="n">odds</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>[1, 3, 5, 7, 9, 11]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Number-List:-For-Loop">Number List: For Loop<a class="anchor-link" href="#Number-List:-For-Loop"> </a></h2>
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
    <span class="k">if</span> <span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">):</span> 
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
<pre>[0, 2, 4, 6, 8, 10]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Outputting odd numbers:</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">numbers</span> <span class="o">=</span> <span class="p">[</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">6</span><span class="p">,</span><span class="mi">7</span><span class="p">,</span><span class="mi">8</span><span class="p">,</span><span class="mi">9</span><span class="p">,</span><span class="mi">10</span><span class="p">]</span>
<span class="n">odds</span> <span class="o">=</span> <span class="p">[]</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">1</span><span class="p">):</span> <span class="c1"># start at 1 instead of 0 in order to get odd numbers</span>
        <span class="n">odds</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>

<span class="nb">print</span><span class="p">(</span><span class="n">odds</span><span class="p">)</span>
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
<h2 id="Printing-Numbers-That-Are-Multiples-of-2-or-5:">Printing Numbers That Are Multiples of 2 or 5:<a class="anchor-link" href="#Printing-Numbers-That-Are-Multiples-of-2-or-5:"> </a></h2>
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

<span class="k">while</span> <span class="n">i</span> <span class="o">&lt;</span> <span class="mi">100</span><span class="p">:</span>
    <span class="n">numbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">i</span> <span class="o">+=</span> <span class="mi">1</span>

<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">numbers</span><span class="p">:</span>
    <span class="k">if</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span> <span class="c1"># skips the number 0, so that the list is from 1 to 100</span>
        <span class="k">pass</span>
    <span class="k">elif</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">5</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
        <span class="n">newNumbers</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">])</span>
    <span class="k">elif</span> <span class="n">numbers</span><span class="p">[</span><span class="n">i</span><span class="p">]</span> <span class="o">%</span> <span class="mi">2</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span> <span class="c1"># elif makes the code not repeat numbers</span>
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
<pre>[2, 4, 5, 6, 8, 10, 12, 14, 15, 16, 18, 20, 22, 24, 25, 26, 28, 30, 32, 34, 35, 36, 38, 40, 42, 44, 45, 46, 48, 50, 52, 54, 55, 56, 58, 60, 62, 64, 65, 66, 68, 70, 72, 74, 75, 76, 78, 80, 82, 84, 85, 86, 88, 90, 92, 94, 95, 96, 98]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

<div class="cell border-box-sizing text_cell rendered"><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Challenge">Challenge<a class="anchor-link" href="#Challenge"> </a></h1><p>This code segment is at a very early stage of implementation.</p>
<ul>
<li>What are some ways to (user) error proof this code?</li>
<li>The code should be able to calculate the cost of the meal of the user</li>
</ul>
<p>Hint:</p>
<ul>
<li>write a “single” test describing an expectation of the program of the program</li>
<li>test - input burger, expect output of burger price</li>
<li>run the test, which should fail because the program lacks that feature</li>
<li>write “just enough” code, the simplest possible, to make the test pass</li>
</ul>
<p>Then repeat this process until you get program working like you want it to work.</p>

</div>
</div>
</div>
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">menu</span> <span class="o">=</span>  <span class="p">{</span><span class="s2">&quot;hyderabadi mutton biryani&quot;</span><span class="p">:</span> <span class="mf">24.99</span><span class="p">,</span>
         <span class="s2">&quot;chicken garlic malai kabab&quot;</span><span class="p">:</span> <span class="mf">19.99</span><span class="p">,</span>
         <span class="s2">&quot;chicken tikka masala&quot;</span><span class="p">:</span> <span class="mf">14.99</span><span class="p">,</span>
         <span class="s2">&quot;mango lassi&quot;</span><span class="p">:</span> <span class="mf">5.25</span><span class="p">,</span>
         <span class="s2">&quot;masala cheese dosa&quot;</span><span class="p">:</span> <span class="mf">19.99</span><span class="p">}</span>
<span class="n">total</span> <span class="o">=</span> <span class="mi">0</span>
<span class="n">price</span> <span class="o">=</span> <span class="mi">0</span>
<span class="c1">#shows the user the menu and prompts them to select an item</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Royal India Menu&quot;</span><span class="p">)</span>
<span class="k">for</span> <span class="n">k</span><span class="p">,</span><span class="n">v</span> <span class="ow">in</span> <span class="n">menu</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
    <span class="nb">print</span><span class="p">(</span><span class="n">k</span> <span class="o">+</span> <span class="s2">&quot;  $&quot;</span> <span class="o">+</span> <span class="nb">str</span><span class="p">(</span><span class="n">v</span><span class="p">))</span> <span class="c1">#why does v have &quot;str&quot; in front of it?</span>

<span class="c1">#ideally the code should prompt the user multiple times</span>
<span class="k">while</span> <span class="n">total</span> <span class="o">&lt;</span> <span class="mi">3</span><span class="p">:</span>
    <span class="n">item</span> <span class="o">=</span> <span class="nb">input</span><span class="p">(</span><span class="s2">&quot;Please select 3 items from the menu&quot;</span><span class="p">)</span>
    <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Item ordered:&quot;</span><span class="p">,</span> <span class="n">item</span><span class="o">.</span><span class="n">lower</span><span class="p">())</span>
    <span class="k">for</span> <span class="n">k</span><span class="p">,</span><span class="n">v</span> <span class="ow">in</span> <span class="n">menu</span><span class="o">.</span><span class="n">items</span><span class="p">():</span>
        <span class="k">if</span> <span class="n">item</span><span class="o">.</span><span class="n">lower</span><span class="p">()</span> <span class="o">==</span> <span class="n">k</span><span class="p">:</span>
            <span class="n">price</span><span class="o">=</span><span class="p">(</span><span class="n">price</span><span class="o">+</span><span class="n">menu</span><span class="p">[</span><span class="n">item</span><span class="o">.</span><span class="n">lower</span><span class="p">()])</span>
            <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Your total order is $&quot;</span><span class="p">,</span> <span class="n">price</span><span class="p">)</span>
            <span class="n">total</span> <span class="o">=</span> <span class="p">(</span><span class="n">total</span> <span class="o">+</span> <span class="mi">1</span><span class="p">)</span>
            <span class="k">break</span>

    <span class="k">if</span> <span class="n">item</span><span class="o">.</span><span class="n">lower</span><span class="p">()</span> <span class="o">!=</span> <span class="n">k</span><span class="p">:</span>
        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Try choosing your item again.&quot;</span><span class="p">)</span>
        <span class="k">continue</span>

<span class="c1">#code should add the price of the menu items selected by the user </span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Royal India Menu
hyderabadi mutton biryani  $24.99
chicken garlic malai kabab  $19.99
chicken tikka masala  $14.99
mango lassi  $5.25
masala cheese dosa  $19.99
Please select 3 items from the menuhyderabadi chicken biryani
Item ordered: hyderabadi chicken biryani
Try choosing your item again.
Please select 3 items from the menuhyderabadi mutton biryani
Item ordered: hyderabadi mutton biryani
Your total order is $ 24.99
Please select 3 items from the menumango lassi
Item ordered: mango lassi
Your total order is $ 30.24
Please select 3 items from the menuchicken tikka masala
Item ordered: chicken tikka masala
Your total order is $ 45.23
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
<li>What are “single” tests that you will perform on your project? Or, your part of the project?<ul>
<li>As Hack Design and Test plan action … Divide these “single” tests into Issues for Scrum Board prior to coding. FYI, related tests could be in same Issue by using markdown checkboxes to separate tests.</li>
</ul>
</li>
</ul>
</blockquote>

</div>
</div>
</div>
</div>
 

