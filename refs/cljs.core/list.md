## cljs.core/list



 <table border="1">
<tr>
<td>function/macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/list</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/list)
</td>
</tr>
</table>


 <samp>
(__list__ & items)<br>
</samp>

---

Creates a new list containing `items`.



---


###### See Also:

[`cljs.core/vector`](../cljs.core/vector.md)<br>
[`cljs.core/list?`](../cljs.core/listQMARK.md)<br>

---




Function code @ [github](https://github.com/clojure/clojurescript/blob/r2080/src/cljs/cljs/core.cljs#L1980-L1993):

```clj
(defn list [& xs]
  (let [arr (if (instance? IndexedSeq xs)
              (.-arr xs)
              (let [arr (array)]
                (loop [^not-native xs xs]
                  (if-not (nil? xs)
                    (do
                      (.push arr (-first xs))
                      (recur (-next xs)))
                    arr))))]
    (loop [i (alength arr) ^not-native r ()]
      (if (> i 0)
        (recur (dec i) (-conj r (aget arr (dec i))))
        r))))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2080
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1980-1993](https://github.com/clojure/clojurescript/blob/r2080/src/cljs/cljs/core.cljs#L1980-L1993)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2080/src/clj/cljs/core.clj#L1300-L1303):

```clj
(defmacro list
  ([] `cljs.core.List.EMPTY)
  ([x & xs]
    `(-conj (list ~@xs) ~x)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2080
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:1300-1303](https://github.com/clojure/clojurescript/blob/r2080/src/clj/cljs/core.clj#L1300-L1303)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/list` @ clojuredocs](http://clojuredocs.org/clojure.core/list)<br>
[`clojure.core/list` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/list/)<br>
[`clojure.core/list` @ crossclj](http://crossclj.info/fun/clojure.core/list.html)<br>
[`cljs.core/list` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/list.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/list.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Creates a new list containing `items`.",
 :ns "cljs.core",
 :name "list",
 :signature ["[& items]"],
 :history [["+" "0.0-927"]],
 :type "function/macro",
 :related ["cljs.core/vector" "cljs.core/list?"],
 :full-name-encode "cljs.core/list",
 :source {:code "(defn list [& xs]\n  (let [arr (if (instance? IndexedSeq xs)\n              (.-arr xs)\n              (let [arr (array)]\n                (loop [^not-native xs xs]\n                  (if-not (nil? xs)\n                    (do\n                      (.push arr (-first xs))\n                      (recur (-next xs)))\n                    arr))))]\n    (loop [i (alength arr) ^not-native r ()]\n      (if (> i 0)\n        (recur (dec i) (-conj r (aget arr (dec i))))\n        r))))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2080",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1980 1993]},
 :extra-sources [{:code "(defmacro list\n  ([] `cljs.core.List.EMPTY)\n  ([x & xs]\n    `(-conj (list ~@xs) ~x)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2080",
                  :filename "src/clj/cljs/core.clj",
                  :lines [1300 1303]}],
 :full-name "cljs.core/list",
 :clj-symbol "clojure.core/list"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/list"]))
```

-->