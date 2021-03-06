# Command constructs

<p style="text-align: justify;">
Command constructs allows one to run specific commands against Jtwig. An important aspect common to all commands is that they never produce content, they only produce side effects.
</p>

## `set` command

<p style="text-align: justify;">
The set command allows to specify an assignment operation inside a Jtwig template, it will assign to the result of an expression to the specified variable.
</p>

```twig
{% set var = 2 + 3 %}
```

<p style="text-align: justify;">
In the previous example one assigned the result of evaluating the expression <code>2 + 3</code> to the variable <code>var</code>. Note again that the output of the previous example will be empty because, as mentioned before, <code>set</code> as a command, does not produce content, it just affects the context defining, or redefining a variable.
</p>

## `do` command

<p style="text-align: justify;">
The <code>do</code> command just evaluates a given expression.
</p>

```twig
{% do something.run() %}
```

<p style="text-align: justify;">
There is not a lot to say about this construct, it might be usefull to trigger behaviour from the template by running a Java method for example.
</p>

## `flush` command

<p style="text-align: justify;">
A common operation over streams is the <code>flush</code> operation. As a template engine Jtwig is very much associated with output buffers, which can be explicitly flushed. This forces the buffer to be flushed, for example, in a web application it will force the data to be sent over the wire.
</p>

```twig
{% flush %}
```

