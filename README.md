Condorcet
=========

Plurality voting, the election method that most people know, is horrible.
It doesn't allow voters to fully express their preference, leading to
situations such as "voting for the lesser of two evils" because voting for
the preferred third-party candidate would be "throwing your vote away", or
the possibility of "spoiler candidates" such as Nader in the 2000 U.S.
presidential election.  Better election methods exist, and have been known
since the 1700s, and aren't even difficult to explain.  Further discussion
of election methods is beyond the scope of these file header comments, but
well worth your time to research. :)

The Condorcet family of election methods includes all methods which elect
the "Condorcet winner" if one exists.  A Condorcet winner is a candidate
who would beat all other candidates in hypothetical pairwise elections.
(Two-candidate elections are easy, and all sensible election methods yield
the same results.  It's when there are more than two candidates that things
get complicated.)  A single "vote" in a Condorcet election is an ordered
list of preferred candidates, indicating e.g. "A > B > C > D > others".

This script counts votes and attempts to elect a Condorcet winner, if
one exists.  It does not attempt to resolve elections where there is no
Condorcet winner.  (This could be done using Tideman ranked pairs, Schulze
(a.k.a. Schwartz sequential dropping), or several other methods.)

Input data for this script follows this format:

    # Full-line and in-line comments are allowed, indicated by "#"
    # Blank lines are ignored
    
    # Each non-blank non-comment line is a vote
    # Each vote lists candidates in order of preference
    
    # Here is a single sample vote:
    AwesomeCandidate GoodCandidate OkayCandidate LousyCandidate
    
    # Candidate identifiers can be arbitrary strings, but must contain no spaces
    # Votes don't need to list all candidates
    # Unmentioned candidates rank beneath all candidates that were mentioned

For more on Condorcet election methods, see [Wikipedia](http://en.wikipedia.org/wiki/Condorcet_method).
