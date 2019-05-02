# Setting up an editor for programming (OPTIONAL)

An editor is a program that lets us write longer programs than we can
write on the `>>>` prompt. Then we can save the programs to files and
run them as many times as we want without writing them again.

When programmers say "editor" they don't mean programs like Microsoft
Word or LibreOffice/OpenOffice Writer. These programs are for writing
text documents, not for programming. **Programming editors don't support
things like bigger font sizes for titles or underlining bits of text**,
but instead they have features that are actually useful for programming,
like automatically displaying different things with different colors.

If you are on Windows or Mac OSX you have probably noticed that your
Python came with an editor called IDLE. We are not going to use it
because it's lacking some important features, and most experienced
programmers (including me) don't use it or recommend it.

## Which editor?

The choice of an editor is a very personal thing. There are many
editors, and most programmers have a favorite editor that they use for
everything and recommend to everyone.

Suggested editors:

- [PyCharm](https://www.jetbrains.com/pycharm/)
- [Sublime Text](https://www.sublimetext.com/)
- [Atom](https://atom.io/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Vim](https://www.vim.org/) - for shell experts
- [emacs](https://www.gnu.org/software/emacs/) - for octopuses :laughing:

This list doesn't contain all editors, but these are editors that
people often try to use.

## Editor or `>>>` prompt?

So far we have used the `>>>` prompt for everything. But now we also
have an editor that lets us write longer programs. So why not just
always use the editor?

The `>>>` prompt is meant to be used for experimenting with things. For
example, if you want to know what `"hello" + 123` does, just open the
prompt and run it.

If you want to write something once and then run it many times, write
the code to a file. For example, if you want to make a program that asks
the user to enter a word and then echoes it back, write a program that
does that in a file and run it as many times as you want to.

Note that if you write something like `'hello'` to the `>>>` prompt it
echoes it back, but if you make a file that contains nothing but a
`'hello'` it won't do anything when you run it. You need to use
`print('hello')` instead when your code is in a file.

***

[Previous](using-functions.md) | [Next](if.md) |
[List of contents](../README.md#basics)
