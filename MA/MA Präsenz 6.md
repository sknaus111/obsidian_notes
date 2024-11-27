## Aufgabe 1. 
Sei $X = \{1, 2, \{3\}, \{\{4\}, \{5\}\}\}$. Stellen Sie den Wahrheitswert der folgenden Aussagen
fest:
- a) $3 ∈ X$ 
  falsch
- b) $\{\{3\}\} ⊆ X$
  wahr
- c) $\{1, 3\} ⊆ X$
  falsch
- d) $\{\{4\}, \{5\}\} ∈ X$
  wahr
- e) $\{1, \{3\}\} ∈ P(X )$
  wahr
- f) $\{\{4\}, \{5\}\} ∈ P(X )$
  falsch
- g) $\{1, \{3\}, \{\{4\}\}\} ⊆ X$
  falsch
- h) $\{\{2\}, \{\{3\}\}\} ⊆ P(X )$
  wahr
## Aufgabe 2. 
Wir definieren die Mengen $\mathbb{Z}^{+} = \{n ∈ \mathbb{Z} | n > 0\}, \mathbb{Z}^{-} = \{n ∈ \mathbb{Z} | n < 0\},G = \{2n | n ∈ \mathbb{Z}\}$ und $U = \{2n + 1 | n ∈ \mathbb{Z}\}$ sowie die Funktionen $f : \mathbb{Z} → \mathbb{Z}, n  → n^{2},g : \mathbb{Z} → \mathbb{Z}, n → n + 1$ und $h : \mathbb{Z} → \mathbb{Z}, n  → −n$. Geben Sie möglichst einfache Beschreibungen der folgenden Mengen an.

- a) $(\mathbb{Z}^{+} \setminus G )^{c}$
  $\mathbb{Z}^{-} \cup G$
- b) $\mathbb{Z}^{-} \setminus h(g (\mathbb{Z}^{+}))$
  $\{ -1 \}$
- c) $(G ∩ \mathbb{Z}^{+}) ∪ g (\mathbb{Z}^{-} ∩ U)$
  G
- d) $f (g (G )) \setminus U$
  $\emptyset$
## Aufgabe 3. 
Für $m, a ∈ \mathbb{Z}$ mit $m \not= 0$ sei $P_{m,a} = \{mq + a | q ∈ \mathbb{Z}\}$. Zeigen Sie:

- a) $b ∈ P_{m,a}$ impliziert $P_{m,b} = P_{m,a}$
  $P_{m,a}=\{ mq+a|q\in \mathbb{Z} \}=\{ f_{m,a}(q)|q\in \mathbb{Z} \}$ mit $f:\mathbb{Z}\rightarrow \mathbb{Z}$ $q \rightarrow mq+a$
  $b\in P_{m,a}\implies \exists p\in \mathbb{Z}:mp+a=b\implies a=m(-p)+b$
  $\forall q \in \mathbb{Z}:f_{m,a}(q)=f_{m,a}(q-p) \implies mq+a =mq+m(-p)+b=m(q-p)+b$
  $f_{m,b}(q)=f_{m,a}(q+p) \implies mq+b=mq+mb+a=m(q+b)+a$
- b) $m_{1} | m_{2}$ genau dann wenn $P_{m_{2},a} ⊆ P_{m_{1},a}$
  $\forall b:(b\in P_{m_{2},a}\implies b\in P_{m_{2},a})$
  $\implies m_{1}|m_{2} \iff \exists k:m_{1}k=m_{2}$
  Sei $b\in P_{m_{2},a}$ bel. $\implies \exists q: b=m_{2}q+a$
  $\implies b=m_{1}(kq)+a\in P_{m_{1},a}$
  
  $\impliedby: \forall b:b\in P_{m_{2},a} \implies b\in P_{m_{1},a}$
  $m_{2}+a \in P_{m_{1},a} \implies \exists q: m_{1}q+a=m_{2}+a$
  $m_{2}=m_{1}*q \iff m_{1}|m_{2}$
  
- c) Für $m_{1}, m_{2}, a ∈ \mathbb{Z}$ und $m = kgV(m_{1}, m_{2})$ gilt: $P_{m,a} = P_{m_{1},a} ∩ P_{m_{2},a}$.
  $\subseteq: b\in P_{m,a}$ bel. $\exists q:b=mq+a$
  $m_{1}|m \land m_{2}|m$
  $m_{1}p_{1}=m \land m_{2}p_{2}=m$
  $b=m_{1}p_{1}q+a \implies b\in P_{m_{1},a}$
  $b=m_{2}p_{2}q+a \implies b\in P_{m_{2},a}$
  
  $\exists q_{1}:b=m_{1}q_{1}+a$
  $\exists q_{2}:b=m_{2}q_{2}+a$
  $m_{1}q_{1}=m_{2}q_{2}$
  $m|m_{1}q_{1} \land m|m_{2}q_{2}$
  $mk_{1}=m_{1}q_{1}$
  $b=mk_{1}+a\in P_{m,a}$
  
- d) Falls $P_{m_{1}a_{1}} ∩ P_{m_{2}a_{2}} \not= ∅$, dann gibt es m, a so dass $P_{m_{1},a_{1}} ∩ P_{m_{2},a_{2}} = P_{m,a}$.
$P_{m_{1}a_{1}} \cap P_{m_{2},a_{2}} \not= \emptyset \iff \exists x\in P_{m_{1}a_{1}} \cap P_{m_{2},a_{2}}$
$$  
  
  




Hinweis: Im Beweis von d) sind a) und c) nützlich.

