# DerivedApplicationTrees
Parse a language for expressing relationships between abstract symbols.

A Derived Application Tree is similar to a Rose Tree in that a given node can have 0 or more leaves. Each node has a name and an arity, and each occurrence of the same name should have the same arity. Unlike a Rose Tree, a Derived Application Tree can't be formed directly, but must be formed by composing Transition Rules. This process models the derivation of mathematical theorems by constructing proofs.

A Transition Rule specifies how to transform a list of derived trees into a new derived tree. A Class is a set of (name, arity) pairs and a set of transition rules referencing the given (name, arity) pairs. Each Class specifies a stand-alone formal language which can be thought of as a subset of all possible Rose Trees constructed from nodes with the given names.

From each Class, a parser combinator is constructed which reads derivations, then outputs "valid" or "invalid." A valid derivation of a candidate tree is a proof that said tree belongs to the Class which validates the derivation. This tool will serve as the foundation for a platform for comparing and extending formal languages. This platform's goal is the research, transmission, and publication of mathematics.
