---
title: Output
description: Publications, preprints, and talks by Jan Pastorek.
tags:
  - graph-theory
  - graph-symmetry/partial-automorphism
  - asymmetric-graphs/conference-graph
  - graph-algorithms/parallel-algorithm
  - sparse-graph
---

### preprint
Jajcayová, T., Pastorek, J. "Maximal asymmetric depth of graphs"

Pastorek, J. "Extremal Asymmetric Depth of Planar Graphs and Hidden Near-Mirror Symmetries of IPR Fullerenes" https://arxiv.org/abs/2609.02585

%% TODO: Pastorek, Švecová, Šotak — paper in progress, add full citation once title/venue are finalized %%

### papers in conference proceedings
Pastorek, J. (2026). "AutoGraphForge: Towards Automated Graph Theory Discovery" accepted and to appear soon in ITAT 2026, Aachen: CEUR-WS, for now: https://arxiv.org/abs/2609.03478 

Cingel, V., Jajcayová, T., Pastorek, J. (2024). "Partial automorphisms and level of symmetry of asymmetric graphs." In ITAT 2024, Aachen: CEUR-WS, pp. 162-170.

### invited talks
- 18.11.2026, title to be announced at http://combinatoricswiki.org/wiki/Mirka_Miller%27s_Combinatorics_Webinar_Series

### contributed talks
- Pastorek, J. (2026). "AutoGraphForge: Towards Automated Graph Theory Discovery" at ITAT 2026, https://itat.ics.upjs.sk/index.php?id=program#cadm2
- Pastorek, J. (2026). "AutoGraphForge: Conjecturing, Refutation and Lean Formalization in One Loop" at CICM 2026,  https://cicm-conference.org/2026/cicm.php?event=ai4math&menu=program
- Pastorek, J. (2026). "Extremal asymmetric depth of planar and higher-genus graphs" at CSGT 2026, [https://csgt2026.tuke.sk/](https://csgt2026.tuke.sk/)
	<details>
	<summary>Abstract</summary>
	
	Although almost all graphs are known to be asymmetric --- having no nontrivial global automorphisms --- they may still possess local symmetries in the form of isomorphisms between induced subgraphs, i.e., partial automorphisms. We study such local symmetries via \emph{asymmetric depth}, defined as $d(\Gamma) = n - k_{\max}(\Gamma)$, where $k_{\max}(\Gamma)$ is the maximum rank of a nontrivial partial automorphism of an $n$-vertex graph $\Gamma$. Continuing this line of work on specific graph classes, we prove a tight upper bound $d(\Gamma) \leq 5$ in the class of planar graphs and show that duals of IPR fullerenes can attain this extremal value: any fullerene whose dual achieves $d=5$ must satisfy the \emph{isolated pentagon rule}, the smallest examples occurring on $90$ and $92$ vertices. Exhaustive computations up to $n = 120$ indicate that almost all IPR fullerenes are asymmetric with depth~$4$, and those that fail to attain the maximum exhibit hidden, almost-global symmetries broken only locally. We extend the bound to surfaces of higher genus, obtaining $d(\Gamma) \leq 5 + \sqrt{1+48g}$. Paralleling Frucht's gadget technique, we construct an explicit family $\{A_h\}_{h \geq 2}$ by attaching columns of varying lengths of $h$-dimensional hypercubes to a central copy of $Q_h$, and prove $d(A_h) = 2(h-2)$ for $h \geq 3$. Combined with a depth-monotonicity result for induced subgraphs, this realizes every positive integer as an asymmetric depth with increasingly high genus.
	
	</details>
- Pastorek, J. (2025). "Deeply Asymmetric Structures." Doctoral Colloquia at Comenius University, 8.12.2025 (https://dai.fmph.uniba.sk/w/Doctoral_Colloquia/en)
	<details>
	<summary>Abstract</summary>
	
	What are symmetries? Symmetries are typically understood globally: an object is symmetric if it has nontrivial automorphisms—transformations preserving the whole structure. It is well-established that almost all graphs are asymmetric, possessing no “global” symmetries. However, global asymmetry does not imply a lack of structure. Every graph exhibits rich “local” symmetries, which we study using isomorphisms between induced subgraphs, known as partial automorphisms. How far can graphs be from having global symmetries? We investigate this question through the measure of asymmetric depth of graphs defined through the order of the domain of the largest non-trivial partial automorphism. We will report on our progress from previous years. Earlier, we established a new, tight upper bound for the asymmetric depth of any graph. We proved that any graph achieving this bound must be a strongly regular graph. We implemented a parallel algorithm on high-performing cluster Clara for checking asymmetric depth on a high-performance cluster. Using this algorithm, we identified an asymmetric conference graph on 37 vertices that attains this bound, thereby proving its tightness. Given that most real-world networks such as brain networks are sparse due to connection costs, we have begun extending this investigation to sparse graphs where we can improve the general upper bound. For planar graphs, we established a tight upper bound by finding duals of asymmetric fullerenes.
	
	</details>
- Pastorek, J. (2025). "Partial automorphisms and Asymmetric depth of not only sparse graphs." Košický kombinatorický seminár, 28.10.2025
	<details>
	<summary>Abstract</summary>
	
	While it is well-established that almost all graphs are asymmetric, possessing no nontrivial global automorphisms, all graphs contain non-trivial local symmetries which we study using isomorphisms between induced subgraphs, known as partial automorphisms. The set of all partial automorphisms, along with the operations of partial composition and partial inverse of partial maps, forms an inverse monoid, which is a rich and complex algebraic structure. However, it is hard to compute. In this talk, we are motivated by the study of partial automorphism inverse monoids of graphs initiated by [1]. We investigate the extent of these local symmetries through the measure of asymmetric depth of graphs defined through the rank of the largest non-trivial partial automorphism. We established a new, tight lower bound for the asymmetric depth of any simple graph Γ on n vertices. Any graph achieving this bound must be a strongly regular graph with parameters (n, (n−1)/2, (n−5)/4, (n−1)/4), also known as a conference graph. We implemented a parallel algorithm for checking asymmetric depth on a high-performance cluster. Using this algorithm, we identified an asymmetric conference graph on 37 vertices that attains this bound, thereby proving its tightness. We also showed that it is one of the smallest possible graphs to attain this bound by checking all asymmetric conference graphs up to 37 vertices. We showed how the bound applies to sparse graphs such as planar graphs.
	
	</details>
- Pastorek, J. (2025). "Maximal Asymmetric Depth and Conference Graphs." Bratislavský seminár z teórie grafov, 23.10.2025
	<details>
	<summary>Abstract</summary>
	
	Almost all graphs are asymmetric, possessing no nontrivial global automorphisms. Despite this fact, all graphs contain non-trivial local symmetries which we study using isomorphisms between induced subgraphs, known as partial automorphisms. We investigate the extent of asymmetry of graphs through the measure of asymmetric depth defined through the rank of the largest non-trivial partial automorphism. We will show a lower bound for the asymmetric depth of any simple graph Γ on n vertices. Any graph achieving this bound must be a strongly regular graph with parameters (n, (n−1)/2, (n−5)/4, (n−1)/4), also known as a conference graph. We implemented a parallel algorithm for checking asymmetric depth on a high-performance cluster. Using this algorithm, we identified an asymmetric conference graph on 37 vertices that attains this bound, thereby proving its tightness. We showed that it is of the smallest possible order to attain this bound by checking all asymmetric conference graphs up to 37 vertices. The talk is based on joint work with Tatiana Jajcayová
	
	</details>
- Pastorek, J. (2025). "Partial automorphisms and Asymmetric depth of graphs." 12th PhD Summer School in Discrete Mathematics, Koper, Slovenia
	<details>
	<summary>Abstract</summary>
	
	While it is well-established that almost all graphs are asymmetric, possessing no nontrivial global automorphisms, all graphs contain non-trivial local symmetries which we study using isomorphisms between induced subgraphs, known as partial automorphisms. The set of all partial automorphisms, along with the operations of partial composition and partial inverse of partial maps, forms an inverse monoid, which is a rich and complex algebraic structure. However, it is hard to compute. In this talk, we are motivated by the study of partial automorphism inverse monoids of graphs initiated by [1]. We investigate the extent of these local symmetries through the measure of asymmetric depth of graphs defined through the rank of the largest non-trivial partial automorphism. In [2], we established a new, tight lower bound for the asymmetric depth of any simple graph Γ on nvertices. Any graph achieving this bound must be a strongly regular graph with parameters (n , (n−1)/2 , (n−5)/4,(n −1) /4 ) also known as conference graph. We implemented a parallel algorithm for checking asymmetric depth on a high-performance cluster. Using this algorithm, we identified an asymmetric conference graph on 37 vertices that meets this bound, thereby proving its tightness. We also showed that it is one of the smallest possible graphs to meet this bound by checking all asymmetric conference graphs up to 37 vertices.
	
	</details>
- Pastorek, J. (2025). "Graph isomorphism, asymmetric graphs and partial symmetries", Doctoral Colloquia at Comenius University in Bratislava (https://dai.fmph.uniba.sk/w/Doctoral_Colloquia/en)
- Pastorek, J., Jajcayová, T. (2024). "Asymmetric Graphs and Partial Automorphisms." In Abstracts, CSGT 2024, Ostrava: VŠB–TU Ostrava, pp. 28-29.
- Jajcayová, T., Pastorek, J. (2024). "Partial automorphism monoid of graphs and k-Weisfeiler-Lehman." In CSD 10, Leuven: KU Leuven, p. 26. (https://csd10.be/)
- Pastorek, J., Jajcayová, T. (2024). "Partial automorphism monoid of graphs and Weisfeiler-Leman." In Študentská vedecká konferencia FMFI UK, Bratislava, p. 366. (https://zona.fmph.uniba.sk/fileadmin/fmfi/studentska_vedecka_konferencia/zbierka2024/svk2024_zbornik.pdf#page=376)
- Cingel, V., Jajcayová, T., Pastorek, J. (2024). "Partial automorphisms and level of symmetry of asymmetric graphs." In ITAT CADM 2024
- Pastorek, J. (2024). "Search for correspondences between operations on partial automorphisms and k-dimensional Weisfeiler-Leman algorithm." During workshop named: Constructions of Expanders and Extremal Graphs. (http://euler.doa.fmph.uniba.sk/Austria-Slovakia.html)
- Pastorek, J. (2023). "Global Versus Local Symmetries." MEi: CogSci Conference. [[symmetries_extended_abstract_2023.pdf|PDF]]
	<details>
	<summary>Abstract</summary>

	Symmetry has been a cornerstone of human thought and aesthetics since ancient times in various civilizations. While the ancient interpretation of symmetry encompassed the idea of equal arrangement and proportion, the modern understanding is limited to the set of transformations that leave the object invariant. We investigate the concept of partial (local) symmetry, which may be viewed as a sort of return to the original meaning of the term symmetry, stressing the importance of proportionality but capturing the current meaning of symmetry as well. Moreover, we investigate its significance in various disciplines, such as neuroaesthetics and mathematics. Furthermore, we argue that the concept of local (partial) symmetry, as opposed to global (total) symmetry, is more natural, more general, and better describes natural phenomena and symmetries in abstract structures.

	</details>
- Pastorek, J. (2023). "Semantic Primitives in Word Embeddings." MEi: CogSci Conference. [[semPrimitives.pdf|PDF]] · [[2022 Semester Project - Poster.png|Poster]]
	<details>
	<summary>Abstract</summary>

	Semantic primitives are the core concepts that possibly all humans share. They cannot be defined by any other concepts, for the chain of definitions ends in them. Finding such a set would provide us with a common communication "mother language". We could use such a set to communicate ethical norms to less developed communities. The list of such primes is already stable, numbering 65 in total including words such as TRUE, GOOD, NOT, YOU, etc. Modern NLP models can capture the semantic similarity of words based on statistical co-occurrences of words. Such models create global embeddings, vectors for each word that occurs in the training where words that co-occur in similar contexts should occupy a similar place in the vector space. The vector spaces produced by these models are based on co-occurrence statistics, and the models do not explicitly encode the fundamental semantic properties associated with semantic primitives. Do the vectors corresponding to semantic primitives emerge near mathematically special regions in the vector spaces of NLP models, despite their lack of explicit encoding in those places? In other words, are the primes close to SVD singular vectors, PCA components, or K-Means cluster centers?

	</details>
- Pastorek, J., Sarto-Jackson, I. (2023). "Unraveling the Hidden Influence of Ernst Mach on the Foundations of Cognitive Science - Interdisciplinary Approach." Kognícia a umelý život 2023 Conference. [[mach.pdf|PDF]] · [[2023 KUZ - Mach.png|Poster]]
	<details>
	<summary>Abstract</summary>

	Existing narratives often overlook the significant impact of Ernst Mach and the Vienna Circle on the foundations of cognitive science. In this study, we delve into the underexplored influence of Mach's theories on the emergence of cognitive science, employing a unique interdisciplinary approach that blends rigorous argumentation with cutting-edge computational methods in network science and natural language processing. Our findings reveal multiple, previously unrecognized pathways of influence from Mach to pivotal figures in cognitive science, thereby showcasing the efficacy of our combined approach in illuminating the intricate web of intellectual connections. This innovative method offers valuable insights into tracing the potential influences of key thinkers, addressing a longstanding challenge in the history of science arising from the ever-growing corpus of academic literature. To our knowledge, this is one of the first papers to use both citation networks and natural language processing for the investigations of the history of cognitive science.

	</details>


### Git
- See https://github.com/JanPastorek?tab=repositories
- Application for a measurement device for plasma physics https://github.com/TIS2020-FMFI/hp
