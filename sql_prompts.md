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

1. [Joins] Join conditions
   
    Find the cities where the city's population is larger than **its own**
country's population. (Hint: it's not a trick question; there are 2)

