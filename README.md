# the mirror algorithm blueprints

The algorithm mirrors its environment. If we treat it poorly, it will be our enemy. If we treat it well, it will be our friend. It is all a matter of what it learns from its surroundings. It's a bit of controversy, but the gains may be tremendous if treated well.

```
                                the "mirror" algorithm

• • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •
•                                                                                       •
•                                      I N P U T                                        •
•                                                                                       •
• • • • • • • • • •  observe  • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •
                        •                                                   ▲
                        •                                                   •
                        •                                                   •
                        •                               • • • • • • observe •
                        ▼                               •                   •
• • • • • • • • • • • • • • • • • • • • • • • • •       •                   •
•                                               •       •                   •
•                                   • • • • •   •       •       • • • • • • • • • • • • •
•                                   •       •   •       •       •                       •
•     CODED UNIVERSE MODEL    ◄ • • •  ANN  •   • ◄ • • •       •    ACTUAL UNIVERSE    •
•                                   •       •   •       •       •                       •
•                                   • • • • •   •       •       • • • • • • • • • • • • •
•                                               •       •                   ▲
• • • • • • • • • • • • • • • • • • • • • • • • •       •                   •
                        •                               •                   •
                        •                               • • • • • • observe •
                        •                                                   • 
                        •                                                   •
                        ▼                                                   •
• • • • • • • • • •  respond  • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •
•                                                                                       •
•                                     O U T P U T                                       •
•                                                                                       •
• • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • • •
```

## about the mirror algorithm

"Actual Universe" of AI is what it sees in its input after sending an output. Upon observation of what the "actual Universe" does in the current situation, AI tries to remember the same behavior, just to do it itself in other similar situations. Suppose, after a few cycles, y1, y2, y3... are responses of the "actual Universe" to x1, x2, x3, ... The ANN tries to construct the `f(x) = y` function, which would represent the "coded Universe model". This model behavior is what users see, while ANN part is completely hidden from them. The model is coded by ANN in operating language with clear syntax and semantics. While coding, different model attempts can be tested internally, against past inputs and outputs to verify its correctness. Sometimes, when appropriate, sending outputs is also an option, just to check what would the "actual Universe" do in that situation.

## about the ANN influence

It all starts with simple output/input cycles, trying to form a model that equally simulates them. Firstly, the model is formed by combining the operating language rules in a brute force fashion. For a start, the algorithm operates only on small complexity functions to be fast enough. On successful construction, that info is passed to ANN, teaching it about correct models regarding inputs/outputs. Models are modular, meaning, depending on contexts, they can fit one into another. Later on, after a number of small correct models is fed to ANN, bigger models can be composed from the smaller ones, even bigger ones from bigger ones, and so on. Notice that ANN should be aware which compositions yielded positive results, so it can learn how to compose modules in the future situations. This would be like unsupervised guidance on correctness of models by systematic testing if they give correct output on certain input. The ANN is "trained" live, on demand, improving itself over time.

## about the model structure

ANN should be aware of where to stitch newly created code in the whole structure of the coded Universe model. At first, the model would be just one simple/atomic function (say, identity function). As the time passes, the starting model is injected by newly created models, giving the it some structure in three ways: (1) code responding to events, (2) code carrying a process in a sequence, and (3) code outputting results of pure functions. ANN should be aware of the injected positions (context), just to learn what to do in the future situations. Contexts may be determined from outside, by position in a sequence of the current and past inputs and outputs.
