# the "mirror" algorithm blueprints

The algorithm mirrors its environment. If treated poorly, it may become our enemy. If treated well, it may become our friend. It is all a matter of what it learns from its surroundings. This is a bit of controversy, but the gains may be tremendous if treated well, including exhibiting critical opinion and ethical behavior.

```
                             the "mirror" algorithm

• • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •
•                                                                                 •
•                                    I N P U T                                    •
•                                                                                 •
• • • • •  observe  • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •
              •                                                     ▲
              •                                                     •
              •                                                     •
              •                               • • • • • • • observe •
              ▼                               •                     •
• • • • • • • • • • • • • • •                 •                     •
•                           •                 •                     •
•                           •                 •       • • • • • • • • • • • • • • •
•           CODED           •                 •       •                           •
•          UNIVERSE         • ◄ • • copy  • • •       •      ACTUAL UNIVERSE      •
•           MODEL           •                 •       •                           •
•                           •                 •       • • • • • • • • • • • • • • •
•                           •                 •                     ▲
• • • • • • • • • • • • • • •                 •                     •
              •                               •                     •
              •                               • • • • • • • observe •
              •                                                     •
              •                                                     •
              ▼                                                     •
• • • • •  respond  • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •
•                                                                                 •
•                                   O U T P U T                                   •
•                                                                                 •
• • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •
```

`ACTUAL UNIVERSE` of the diagram is what the algorithm sees in its input after sending an output. Upon observation of what the `ACTUAL UNIVERSE` does in the current situation, the algorithm tries to remember the same behavior, just to do the same thing itself in other similar situations. Suppose that, after a few cycles, `y1`, `y2`, `y3`... are responses of the `ACTUAL UNIVERSE` to `x1`, `x2`, `x3`, ... Underlying implementation tries to construct a complex `f(x) = y` program which would represent the `CODED UNIVERSE MODEL`. The program may be automatically coded in an operating language with clear syntax and semantics. Over time, the `CODED UNIVERSE MODEL` becomes more and more like a mirror image of the `ACTUAL UNIVERSE`, hopingly exhibiting ethical behavior and intelligence.

## Informal implementation description

Let's assume that we have our own operating language with a clear syntax. The operating language is [Turing complete](https://en.wikipedia.org/wiki/Turing_completeness), and its purpose is to hold the current `CODED UNIVERSE MODEL` program. The crux of the problem we are solving is in a process that copies input/output behavior of the `ACTUAL UNIVERSE` to `CODED UNIVERSE MODEL`. We propose a solution to this problem.

The syntax of our operating language is expressed by clear [production rules](https://en.wikipedia.org/wiki/Production_(computer_science)) in a grammar that is already known to us. The solution to the process of copying behavior is in combining production rules of our grammar into a whole that constitutes a valid program in our operating language. There may be many such valid combinations, and any combination that satisfies our input/output pairs, possibly even in a sequence, is a combination we are searching for. However, instead of brute force search, we recommend introducing a controlled bit of randomness in picking which rules to combine. To control the randomness, we assign a "weight" of value `0` to each rule prior to starting the interpretation of the algorithm. Knowing that each "weight" is `0`, we begin with total random selection of rules to construct our first `CODED UNIVERSE MODEL` interpretation. After possibly many attempts while combining rules and testing input/output pairs, once we have a model that corresponds to `ACTUAL UNIVERSE` reality, we remember which rules we combined in the current selection, and increase their "weight" by some amount. These "weights" will be used in the future to prioritize the selection of successful rules over less successful ones. As the interpretation of the algorithm is going on, so as the number of cycles of modeling `CODED UNIVERSE MODEL` increase, we have increasingly more information about successful rules graded by "weight", that could potentially form successful `CODED UNIVERSE MODEL` combination. By prioritizing the rules with greater "weight" amount, we are hoping to be able to move faster through the vast search space of all the possible combinations, hopingly resulting in faster selection of valid programs representing the `ACTUAL UNIVERSE`.

The "weight" information is here explained in its simplified form, and there should be possible various optimizations such as keeping track of rules "weights" relative to contexts in which rules are combined. Some focus attention control is also required to pause the current search process to interactively respond to incoming inputs. Also, Turing completeness of the operating language may introduce infinite loops during the search process, so some formal algorithm patience control would also apply. We are aware that solutions to these sub-problems may turn out to be a quite task of its own, but we are hoping to lay down a solid foundations with the proposed solution.

We hope that the proposed solution algorithm would justify its choice of the name "mirror". We also hope it would interact with the world in the real time, fast enough using its input and output.
