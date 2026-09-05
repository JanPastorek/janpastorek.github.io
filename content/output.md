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

<div class="topic-filter" role="group" aria-label="Filter by research theme">
<button type="button" class="topic-chip is-active" data-topic="all">All</button>
<button type="button" class="topic-chip" data-topic="graphs">Algebraic graph theory</button>
<button type="button" class="topic-chip" data-topic="aimath">AI for mathematics</button>
<button type="button" class="topic-chip" data-topic="complex">Complex systems</button>
<button type="button" class="topic-chip" data-topic="cogsci">Cognitive science</button>
</div>
<script>
(function () {
  var MAP = {
    graphs: ["asymmetric", "automorphism", "weisfeiler", "toroidal", "fullerene", "conference graph", "graph isomorphism", "defective coloring", "token graph", "partial symmetr", "girth", "cubic graph", "graph embedding"],
    aimath: ["autographforge", "lean formalization", "automated graph theory", "conjectur"],
    complex: ["causal emergence", "social cohesion", "brain network", "emergent"],
    cogsci: ["cogsci", "cognitive science", "semantic primitive", "ernst mach", "word embedding"]
  };
  function topicsOf(el) {
    var out = {};
    Array.prototype.forEach.call(el.querySelectorAll("a.tag-link"), function (a) {
      var slug = (a.dataset.slug || "").replace(/^tags\//, "");
      if (MAP[slug]) { out[slug] = true; }
    });
    var t = (el.textContent || "").toLowerCase();
    Object.keys(MAP).forEach(function (k) {
      if (MAP[k].some(function (w) { return t.indexOf(w) !== -1; })) { out[k] = true; }
    });
    return out;
  }
  function setup() {
    var bar = document.querySelector(".topic-filter");
    if (!bar) { return; }
    var root = bar.closest("article") || document;
    var groups = [], current = null;
    Array.prototype.forEach.call(root.querySelectorAll("h3, p, li"), function (el) {
      if (el.closest(".topic-filter")) { return; }
      if (el.tagName === "H3") { current = { head: el, items: [] }; groups.push(current); return; }
      if (!current) { return; }
      if (el.closest("details")) { return; }
      if (el.tagName === "P" && el.closest("li")) { return; }
      current.items.push({ el: el, topics: topicsOf(el) });
    });
    function apply(topic) {
      groups.forEach(function (g) {
        var shown = 0;
        g.items.forEach(function (it) {
          var vis = topic === "all" || !!it.topics[topic];
          it.el.style.display = vis ? "" : "none";
          if (vis) { shown++; }
        });
        g.head.style.display = (!g.items.length || shown) ? "" : "none";
      });
      Array.prototype.forEach.call(bar.querySelectorAll(".topic-chip"), function (c) {
        c.classList.toggle("is-active", c.dataset.topic === topic);
      });
      Array.prototype.forEach.call(root.querySelectorAll("a.tag-link"), function (a) {
        var slug = (a.dataset.slug || "").replace(/^tags\//, "");
        a.classList.toggle("is-active", topic !== "all" && slug === topic);
      });
    }
    function go(t) {
      history.replaceState(null, "", t === "all" ? location.pathname : location.pathname + "#topic-" + t);
      apply(t);
    }
    bar.onclick = function (e) {
      var c = e.target.closest(".topic-chip");
      if (c) { go(c.dataset.topic); }
    };
    window.__topicGo = go;
    var m = /#topic-([a-z]+)/.exec(location.hash);
    apply(m && MAP[m[1]] ? m[1] : "all");
  }
  if (document.readyState !== "loading") { setup(); } else { document.addEventListener("DOMContentLoaded", setup); }
  if (!window.__topicFilterNav) {
    window.__topicFilterNav = 1;
    document.addEventListener("nav", setup);
    document.addEventListener("click", function (e) {
      var a = e.target.closest && e.target.closest("a.tag-link");
      if (!a || !a.closest("article") || !window.__topicGo) { return; }
      var slug = (a.dataset.slug || "").replace(/^tags\//, "");
      if (!MAP[slug]) { return; }
      e.preventDefault();
      e.stopImmediatePropagation();
      window.__topicGo(slug);
    }, true);
  }
})();
</script>

### preprint
Jajcayová, T., Pastorek, J. "Maximal asymmetric depth of graphs" #graphs

Pastorek, J. "Extremal Asymmetric Depth of Planar Graphs and Hidden Near-Mirror Symmetries of IPR Fullerenes." Preprint: [arXiv:2609.02585](https://arxiv.org/abs/2609.02585) #graphs

### in preparation
Maceková, M., Pastorek, J., Soták, R., Švecová, D. "Four-color defective colorings of toroidal graphs." #graphs

Pastorek, J., Sarto-Jackson, I. "Austrian Roots of Cognitive Science: An Interdisciplinary Analysis of Ernst Mach's Contributions." #cogsci #complex

Jedlička, P., Pastorek, J., Varchola, J. "Causal emergence." #complex

### papers in conference proceedings
Pastorek, J. (2026). "AutoGraphForge: Towards Automated Graph Theory Discovery." Accepted, to appear in ITAT 2026, Aachen: CEUR-WS. Preprint: [arXiv:2609.03478](https://arxiv.org/abs/2609.03478) #aimath #graphs

Cingel, V., Jajcayová, T., Pastorek, J. (2024). "Partial automorphisms and level of symmetry of asymmetric graphs." In ITAT 2024, Aachen: CEUR-WS, pp. 162-170. #graphs

### invited talks
- Pastorek, J. (2026). Title to be announced, [Mirka Miller Combinatorics Webinar Series](http://combinatoricswiki.org/wiki/Mirka_Miller%27s_Combinatorics_Webinar_Series), 18.11.2026 #graphs

### contributed talks
- Pastorek, J. (2026). "AutoGraphForge: Towards Automated Graph Theory Discovery" at [ITAT 2026](https://itat.ics.upjs.sk/index.php?id=program#cadm2) #aimath #graphs
- Pastorek, J. (2026). "AutoGraphForge: Conjecturing, Refutation and Lean Formalization in One Loop" at [CICM 2026, AI4Math](https://cicm-conference.org/2026/cicm.php?event=ai4math&menu=program) #aimath #graphs
- Pastorek, J. (2026). "Extremal asymmetric depth of planar and higher-genus graphs" at [CSGT 2026](https://csgt2026.tuke.sk/) #graphs
	<details class="abstract-inline">
	<summary>Abstract</summary>
	
	Although almost all graphs are known to be asymmetric — having no nontrivial global automorphisms — they may still possess local symmetries in the form of isomorphisms between induced subgraphs, i.e., partial automorphisms. We study such local symmetries via *asymmetric depth*, defined as $d(\Gamma) = n - k_{\max}(\Gamma)$, where $k_{\max}(\Gamma)$ is the maximum rank of a nontrivial partial automorphism of an $n$-vertex graph $\Gamma$. Continuing this line of work on specific graph classes, we prove a tight upper bound $d(\Gamma) \leq 5$ in the class of planar graphs and show that duals of IPR fullerenes can attain this extremal value: any fullerene whose dual achieves $d=5$ must satisfy the *isolated pentagon rule*, the smallest examples occurring on $90$ and $92$ vertices. Exhaustive computations up to $n = 120$ indicate that almost all IPR fullerenes are asymmetric with depth $4$, and those that fail to attain the maximum exhibit hidden, almost-global symmetries broken only locally. We extend the bound to surfaces of higher genus, obtaining $d(\Gamma) \leq 5 + \sqrt{1+48g}$. Paralleling Frucht's gadget technique, we construct an explicit family $\{A_h\}_{h \geq 2}$ by attaching columns of varying lengths of $h$-dimensional hypercubes to a central copy of $Q_h$, and prove $d(A_h) = 2(h-2)$ for $h \geq 3$. Combined with a depth-monotonicity result for induced subgraphs, this realizes every positive integer as an asymmetric depth with increasingly high genus.
	
	</details>
- Pastorek, J. (2025). "Deeply Asymmetric Structures." [Doctoral Colloquia](https://dai.fmph.uniba.sk/w/Doctoral_Colloquia/en) at Comenius University, 8.12.2025 #graphs #complex
	<details class="abstract-inline">
	<summary>Abstract</summary>
	
	What are symmetries? Symmetries are typically understood globally: an object is symmetric if it has nontrivial automorphisms—transformations preserving the whole structure. It is well-established that almost all graphs are asymmetric, possessing no “global” symmetries. However, global asymmetry does not imply a lack of structure. Every graph exhibits rich “local” symmetries, which we study using isomorphisms between induced subgraphs, known as partial automorphisms. How far can graphs be from having global symmetries? We investigate this question through the measure of asymmetric depth of graphs defined through the order of the domain of the largest non-trivial partial automorphism. We will report on our progress from previous years. Earlier, we established a new, tight upper bound for the asymmetric depth of any graph. We proved that any graph achieving this bound must be a strongly regular graph. We implemented a parallel algorithm on high-performing cluster Clara for checking asymmetric depth on a high-performance cluster. Using this algorithm, we identified an asymmetric conference graph on 37 vertices that attains this bound, thereby proving its tightness. Given that most real-world networks such as brain networks are sparse due to connection costs, we have begun extending this investigation to sparse graphs where we can improve the general upper bound. For planar graphs, we established a tight upper bound by finding duals of asymmetric fullerenes.
	
	</details>
- Pastorek, J. (2025). "Partial automorphisms and Asymmetric depth of not only sparse graphs." Košický kombinatorický seminár, 28.10.2025 #graphs #complex
	<details class="abstract-inline">
	<summary>Abstract</summary>
	
	While it is well-established that almost all graphs are asymmetric, possessing no nontrivial global automorphisms, all graphs contain non-trivial local symmetries which we study using isomorphisms between induced subgraphs, known as partial automorphisms. The set of all partial automorphisms, along with the operations of partial composition and partial inverse of partial maps, forms an inverse monoid, which is a rich and complex algebraic structure. However, it is hard to compute. In this talk, we are motivated by the study of partial automorphism inverse monoids of graphs initiated by [1]. We investigate the extent of these local symmetries through the measure of asymmetric depth of graphs defined through the rank of the largest non-trivial partial automorphism. We established a new, tight lower bound for the asymmetric depth of any simple graph Γ on n vertices. Any graph achieving this bound must be a strongly regular graph with parameters (n, (n−1)/2, (n−5)/4, (n−1)/4), also known as a conference graph. We implemented a parallel algorithm for checking asymmetric depth on a high-performance cluster. Using this algorithm, we identified an asymmetric conference graph on 37 vertices that attains this bound, thereby proving its tightness. We also showed that it is one of the smallest possible graphs to attain this bound by checking all asymmetric conference graphs up to 37 vertices. We showed how the bound applies to sparse graphs such as planar graphs.
	
	</details>
- Pastorek, J. (2025). "Maximal Asymmetric Depth and Conference Graphs." Bratislavský seminár z teórie grafov, 23.10.2025 #graphs
	<details class="abstract-inline">
	<summary>Abstract</summary>
	
	Almost all graphs are asymmetric, possessing no nontrivial global automorphisms. Despite this fact, all graphs contain non-trivial local symmetries which we study using isomorphisms between induced subgraphs, known as partial automorphisms. We investigate the extent of asymmetry of graphs through the measure of asymmetric depth defined through the rank of the largest non-trivial partial automorphism. We will show a lower bound for the asymmetric depth of any simple graph Γ on n vertices. Any graph achieving this bound must be a strongly regular graph with parameters (n, (n−1)/2, (n−5)/4, (n−1)/4), also known as a conference graph. We implemented a parallel algorithm for checking asymmetric depth on a high-performance cluster. Using this algorithm, we identified an asymmetric conference graph on 37 vertices that attains this bound, thereby proving its tightness. We showed that it is of the smallest possible order to attain this bound by checking all asymmetric conference graphs up to 37 vertices. The talk is based on joint work with Tatiana Jajcayová
	
	</details>
- Pastorek, J. (2025). "Partial automorphisms and Asymmetric depth of graphs." 12th PhD Summer School in Discrete Mathematics, Koper, Slovenia #graphs
	<details class="abstract-inline">
	<summary>Abstract</summary>
	
	While it is well-established that almost all graphs are asymmetric, possessing no nontrivial global automorphisms, all graphs contain non-trivial local symmetries which we study using isomorphisms between induced subgraphs, known as partial automorphisms. The set of all partial automorphisms, along with the operations of partial composition and partial inverse of partial maps, forms an inverse monoid, which is a rich and complex algebraic structure. However, it is hard to compute. In this talk, we are motivated by the study of partial automorphism inverse monoids of graphs initiated by [1]. We investigate the extent of these local symmetries through the measure of asymmetric depth of graphs defined through the rank of the largest non-trivial partial automorphism. In [2], we established a new, tight lower bound for the asymmetric depth of any simple graph Γ on nvertices. Any graph achieving this bound must be a strongly regular graph with parameters (n , (n−1)/2 , (n−5)/4,(n −1) /4 ) also known as conference graph. We implemented a parallel algorithm for checking asymmetric depth on a high-performance cluster. Using this algorithm, we identified an asymmetric conference graph on 37 vertices that meets this bound, thereby proving its tightness. We also showed that it is one of the smallest possible graphs to meet this bound by checking all asymmetric conference graphs up to 37 vertices.
	
	</details>
- Pastorek, J. (2025). "Graph isomorphism, asymmetric graphs and partial symmetries", [Doctoral Colloquia](https://dai.fmph.uniba.sk/w/Doctoral_Colloquia/en) at Comenius University in Bratislava #graphs
- Pastorek, J., Jajcayová, T. (2024). "Asymmetric Graphs and Partial Automorphisms." In Abstracts, CSGT 2024, Ostrava: VŠB–TU Ostrava, pp. 28-29. #graphs
- Jajcayová, T., Pastorek, J. (2024). "Partial automorphism monoid of graphs and k-Weisfeiler-Lehman." In [CSD 10](https://csd10.be/), Leuven: KU Leuven, p. 26. #graphs
- Pastorek, J., Jajcayová, T. (2024). "Partial automorphism monoid of graphs and Weisfeiler-Leman." In Študentská vedecká konferencia FMFI UK, Bratislava, p. 366. (https://zona.fmph.uniba.sk/fileadmin/fmfi/studentska_vedecka_konferencia/zbierka2024/svk2024_zbornik.pdf#page=376) #graphs
- Cingel, V., Jajcayová, T., Pastorek, J. (2024). "Partial automorphisms and level of symmetry of asymmetric graphs." In ITAT CADM 2024 #graphs
- Pastorek, J. (2024). "Search for correspondences between operations on partial automorphisms and k-dimensional Weisfeiler-Leman algorithm." During workshop named: Constructions of Expanders and Extremal Graphs. (http://euler.doa.fmph.uniba.sk/Austria-Slovakia.html) #graphs
- Pastorek, J. (2023). "Global Versus Local Symmetries." MEi: CogSci Conference. [[symmetries_extended_abstract_2023.pdf|PDF]] #cogsci #graphs
	<details class="abstract-inline">
	<summary>Abstract</summary>

	Symmetry has been a cornerstone of human thought and aesthetics since ancient times in various civilizations. While the ancient interpretation of symmetry encompassed the idea of equal arrangement and proportion, the modern understanding is limited to the set of transformations that leave the object invariant. We investigate the concept of partial (local) symmetry, which may be viewed as a sort of return to the original meaning of the term symmetry, stressing the importance of proportionality but capturing the current meaning of symmetry as well. Moreover, we investigate its significance in various disciplines, such as neuroaesthetics and mathematics. Furthermore, we argue that the concept of local (partial) symmetry, as opposed to global (total) symmetry, is more natural, more general, and better describes natural phenomena and symmetries in abstract structures.

	</details>
- Pastorek, J. (2023). "Semantic Primitives in Word Embeddings." MEi: CogSci Conference. [[semPrimitives.pdf|PDF]] · [[2022 Semester Project - Poster.png|Poster]] #cogsci
	<details class="abstract-inline">
	<summary>Abstract</summary>

	Semantic primitives are the core concepts that possibly all humans share. They cannot be defined by any other concepts, for the chain of definitions ends in them. Finding such a set would provide us with a common communication "mother language". We could use such a set to communicate ethical norms to less developed communities. The list of such primes is already stable, numbering 65 in total including words such as TRUE, GOOD, NOT, YOU, etc. Modern NLP models can capture the semantic similarity of words based on statistical co-occurrences of words. Such models create global embeddings, vectors for each word that occurs in the training where words that co-occur in similar contexts should occupy a similar place in the vector space. The vector spaces produced by these models are based on co-occurrence statistics, and the models do not explicitly encode the fundamental semantic properties associated with semantic primitives. Do the vectors corresponding to semantic primitives emerge near mathematically special regions in the vector spaces of NLP models, despite their lack of explicit encoding in those places? In other words, are the primes close to SVD singular vectors, PCA components, or K-Means cluster centers?

	</details>
- Pastorek, J., Sarto-Jackson, I. (2023). "Unraveling the Hidden Influence of Ernst Mach on the Foundations of Cognitive Science - Interdisciplinary Approach." Kognícia a umelý život 2023 Conference. [[mach.pdf|PDF]] · [[2023 KUZ - Mach.png|Poster]] #cogsci #complex
	<details class="abstract-inline">
	<summary>Abstract</summary>

	Existing narratives often overlook the significant impact of Ernst Mach and the Vienna Circle on the foundations of cognitive science. In this study, we delve into the underexplored influence of Mach's theories on the emergence of cognitive science, employing a unique interdisciplinary approach that blends rigorous argumentation with cutting-edge computational methods in network science and natural language processing. Our findings reveal multiple, previously unrecognized pathways of influence from Mach to pivotal figures in cognitive science, thereby showcasing the efficacy of our combined approach in illuminating the intricate web of intellectual connections. This innovative method offers valuable insights into tracing the potential influences of key thinkers, addressing a longstanding challenge in the history of science arising from the ever-growing corpus of academic literature. To our knowledge, this is one of the first papers to use both citation networks and natural language processing for the investigations of the history of cognitive science.

	</details>


### Software
- **AutoGraphForge** — automated conjecturing, refutation and Lean formalization for graph theory (see the ITAT 2026 paper above) #aimath #graphs
- **Parallel asymmetric-depth checker** — computes asymmetric depth on the Clara high-performance cluster; used to identify the extremal conference graph on 37 vertices #graphs
- Further repositories: [github.com/JanPastorek](https://github.com/JanPastorek?tab=repositories)
