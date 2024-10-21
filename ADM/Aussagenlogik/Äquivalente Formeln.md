Zwei Aussagen sind **semantisch** äquivalent, wenn sie die gleiche Wahrheitsbelegung haben, also in den gleichen Fällen wahr oder falsch sind. 
Eine Formel heißt #gültig wenn sie für jede Belegung an Wahrheitswerten wahr ist.  Heißt #unerfüllbar wenn sie für keine Belegung an Wahrheitswerten wahr ist. Und #erfüllbar wenn sie für zumindest eine Belegung an Wahrheitswerten wahr ist.

folgende logische Regeln beschreiben die Äquivalenz zwischen verschiedenen Aussagen.
- (i) $a \land b \iff b \land a ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~a \lor b \iff b \lor a$
- (ii) $a \land (b \land c) \iff (a \land b)\land c ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~a\lor(b\lor c)\iff(a\lor b)\lor c$
- (iii) $a\land(a\lor b)\iff a~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~a\lor(a\land b)$
- (iv) $a\land(b\lor c)\iff(a\land b)\lor(a\land c)~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~a\lor(b\land c)\iff(a\lor b)\land(a\lor c)$ 
- (v) #DeMorgansche_Regel $\lnot(a\land b)\iff \lnot a\lor \lnot b~~~~~~~~~~~~\lnot(a\lor b)\iff \lnot a\land \lnot b$
- (vi) $a\land b\iff \lnot(a\implies \lnot b)~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~a\lor b \iff \lnot a \implies b$
- (vii) $(a \iff b) \iff(a\implies b)\land(b\implies a)\iff \lnot ((a \implies b)\implies \lnot(b \implies a))$
- (viii) $a\implies b \iff \lnot a \lor b~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~(a\iff b)\iff (a\land b)\lor(\lnot a \land \lnot b)$
- (ix) #indirekten_Beweis $a \implies b \iff \lnot b \implies \lnot a ~~~~~~~~~~\lnot(a\implies b)\iff a\land \lnot b$
