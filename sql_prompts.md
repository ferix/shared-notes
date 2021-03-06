#### Notes
* These prompts assume you're working in a Postgres environment with
the [`world` sample database](http://pgfoundry.org/projects/dbsamples/)
installed.
* The prompts are ordered in increasing difficulty.
* A prompt can focus on one or more of the 3 core SQL operations: joins,
aggregates (`GROUP BY`'s), and filters (`WHERE`'s); the focus(es) will be
listed in square brackets before every prompt. While there are many ways
to approach the solution, do your best to craft a query that hits the
specified focus(es).
* **Every prompt is solvable with one query.**


##### General reminders
* Always select the columns you're filtering in a `WHERE` clause so you
can check whether your filtering logic is correct.
* Never trust the prompt to supply you with correct assumptions. Always
investigate the data.
* Always avoid sub-queries if possible. They're hurt performance because
the computation engine has to execute all sub-queries first and wait for
them to finish before it can execute the outer query.

# Prompts

1. [Filters] On-the-fly filtering

    Select the 4 countries that have a GNP per capita (GNP/population)
    greater than 0.035.

1. [Filters] Sub-query filtering

    In one query (sub-queries are allowed, but no unions), select
    the language with the longest spelling and count how many letters
    it takes to spell out that language.

1. [Joins] Join conditions
   
    Select only the cities where the city's population is larger than
    **its own** country's population without using a `WHERE` clause.
    (Hint: it's not a trick question; there are 2)

1. [Aggregates,Filters] Filtering after a group-by

    Without using a sub-query, select only the 5 countries that have
    exactly 6 cities in them.

1. [Filters] Window function

    In one query (sub-queries are allowed, but no unions), list only
    the top 5 most populous cities for **both** the UK **and** USA.
    (This means there should be 10 rows in the final table)

1. [Joins,Aggregates,Filters] Selecting only un-joined data

    Without using a sub-query, find the 6 countries that don't have a
    corresponding language and group them by continent and list how
    many countries are in each continent.

