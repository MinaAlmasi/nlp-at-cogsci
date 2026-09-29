<style>

.footnote-list {
    display: none;
}
</style>

# Exercise 4. From the Ground Up: Word2Vec!
I originally planned to create a Word2Vec bottom-up tutorial, similar to the BPE tokenizer. Unfortunately I ran out of time !

However, I found this tutorial that I would encourage you to go through and try to implement in your own notebook (look at the hands-on below):

<center>
<a href="https://agombert.github.io/AdvancedNLPClasses/chapter3/Session_3_1_Word2Vec_Training/#1-introduction-to-word2vec">Word2Vec Implementation from Scratch</a>
</center>


:::{admonition} HANDS-ON 
:class: red

The tutorial above has a lot of different components, I would focus on ALL that has to do with Skip-gram
* [Sections 2 + 3](https://agombert.github.io/AdvancedNLPClasses/chapter3/Session_3_1_Word2Vec_Training/#2-preparing-the-data) (don't do the CBOW training pairs)
* [Section 4](https://agombert.github.io/AdvancedNLPClasses/chapter3/Session_3_1_Word2Vec_Training/#embedding-dimension) (but not 4.3)

Unlike one of my tutorials, here all of the code is given to you, so there isn't much space for creative coding. However, I still think you might find it useful to dig deeper into this code! 

**As an extra challenge, try two things:**
1. Use your own data rather than the tutorial's 
2. Try to re-create in PyTorch[^pytorch] rather than the tensorflow (see a [basics Pytorch tutorial](https://docs.pytorch.org/tutorials/beginner/basics/buildmodel_tutorial.html))

Point 2 is a *stretch* goal for those ambitious - it would also take me time to convert from one to another!
::::

[^pytorch]: There has been a long-standing rivalry between the two, but Pytorch has increasingly become the preferred option among researchers (see [Jetbrains blog](https://blog.jetbrains.com/pycharm/2026/05/pytorch-vs-tensorflow-choosing-framework-2026/))