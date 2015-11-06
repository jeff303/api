## cljs.core/pr-sequential-writer



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-1503"><img valign="middle" alt="[+] 0.0-1503" title="Added in 0.0-1503" src="https://img.shields.io/badge/+-0.0--1503-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__pr-sequential-writer__ writer print-one begin sep end opts coll)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2080/src/cljs/cljs/core.cljs#L6635-L6647):

```clj
(defn pr-sequential-writer [writer print-one begin sep end opts coll]
  (-write writer begin)
  (when (seq coll)
    (print-one (first coll) writer opts))
  (loop [coll (next coll) n (:print-length opts)]
    (when (and coll (or (nil? n) (not (zero? n))))
      (-write writer sep)
      (print-one (first coll) writer opts)
      (recur (next coll) (dec n))))
  (when (:print-length opts)
    (-write writer sep)
    (print-one "..." writer opts))
  (-write writer end))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2080
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:6635-6647](https://github.com/clojure/clojurescript/blob/r2080/src/cljs/cljs/core.cljs#L6635-L6647)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/pr-sequential-writer` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/pr-sequential-writer.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/pr-sequential-writer.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "pr-sequential-writer",
 :type "function",
 :signature ["[writer print-one begin sep end opts coll]"],
 :source {:code "(defn pr-sequential-writer [writer print-one begin sep end opts coll]\n  (-write writer begin)\n  (when (seq coll)\n    (print-one (first coll) writer opts))\n  (loop [coll (next coll) n (:print-length opts)]\n    (when (and coll (or (nil? n) (not (zero? n))))\n      (-write writer sep)\n      (print-one (first coll) writer opts)\n      (recur (next coll) (dec n))))\n  (when (:print-length opts)\n    (-write writer sep)\n    (print-one \"...\" writer opts))\n  (-write writer end))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2080",
          :filename "src/cljs/cljs/core.cljs",
          :lines [6635 6647]},
 :full-name "cljs.core/pr-sequential-writer",
 :full-name-encode "cljs.core/pr-sequential-writer",
 :history [["+" "0.0-1503"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/pr-sequential-writer"]))
```

-->