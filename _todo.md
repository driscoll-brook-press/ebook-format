# To Do

## Expressions with Dots

If an expression uses a dot,
don't use the expression in multiple places.
Instead, assign the expression to a variable once,
and use that in multiple places.

## Optional Metadata Values

Some metadata variables may be given values in different places.
To determine the value,
a template must try one source, then another, then another,
until it finds a value or exhausts the sources.

Put that calculation in exactly one place.

If it is used in multiple files,
extract it into a file of its own.

## Suppressing Line Feeds

This construct:

    {% some expression%}
    {% some other expression %}

produces a line feed between the two expressions,
even if the expression produces no text.

Test whether this construct:

    {% some expression
    %}{% some other expression %}

suppresses the line feed.

Can also put all code tags flush left:

    {%
            for whatever
    %}{%
                if some indented whatever
    %}
