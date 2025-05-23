# Why Version Control?

We will motivate this answer in the context of code collaboration.

There are some possible solutions to collaborating on code. You can simply email
or message your collaborators with any new code, and they can do so as well when
they make any changes. This has problems because everyone has to make sure to
keep their code updated with what others have sent. People are very liable to
making human errors.

Well, manually keeping track of all collaboration seems like a hassle, so what
if we go to the other extreme? Imagine an RStudio built like Google Docs, where
you can invite collaborators to edit in real time. This is great for ease of
use---all your collaborators can code with no changes to their familiar RStudio
habits. But consider this scenario: you're tweaking some code to give a graph
axis labels. You've done this a thousand times before. But egads! Somehow,
RStudio complains about some inscutable error... It turns out your coworker was
editing at the same time as you, and some parenthesis was unclosed or something
at the time of you declaring "run all this code." Now what? Should you wait
until they're finished to run your code, and then have them wait for you to
finish when you're editing? Sounds like a hassle again.

```{note}
Well, you could both take care to work in your own designated code blocks. Then
any errors would be sandboxed within each block. This actually sounds quite nice
for small scale collaboration with little intermingling. Too bad Posit Cloud's
collaborative editing is locked behind a
[paywall](https://docs.posit.co/cloud/guide/accounts/#beta-features).
```

Our problem with _instant_ collaborative editing was that one person's editing
can affect another's while they are working on separate things. Thus, picture a
method of _delayed_ collaborative editing: an online repository of code will
hold what has been collaborated on. The key difference is that multiple people
can make a copy of that repository to their own computer and make updates. Once
someone is ready to merge their computer's copy back into the repository, they
can do so. The next person to merge may have to reconcile merge conflicts, but
they will suffer no forgetfullness in doing so.

This method of delayed collaboration for the purposes of keeping a project
up-to-date (i.e., controlling its version) is called version control.

```{note}
Fun fact: version control can be used for much more fine-grained control of
version. VCS users can restore deleted code, borrow lines from previous
iterations of files, view past histories, and more.

With more generality, you could say that version control systems have control over
any aspects of a project's version.
```
