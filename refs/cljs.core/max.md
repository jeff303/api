## cljs.core/max



 <table border="1">
<tr>
<td>function/macro</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-927"><img valign="middle" alt="[+] 0.0-927" title="Added in 0.0-927" src="https://img.shields.io/badge/+-0.0--927-lightgrey.svg"></a> </td>
<td>
[<img height="24px" valign="middle" src="http://i.imgur.com/1GjPKvB.png"> <samp>clojure.core/max</samp>](http://clojure.github.io/clojure/branch-master/clojure.core-api.html#clojure.core/max)
</td>
</tr>
</table>


 <samp>
(__max__ x)<br>
</samp>
 <samp>
(__max__ x y)<br>
</samp>
 <samp>
(__max__ x y & more)<br>
</samp>

---

Returns the greatest number argument.



---


###### See Also:

[`cljs.core/min`](../cljs.core/min.md)<br>
[`cljs.core/max-key`](../cljs.core/max-key.md)<br>

---


Source docstring:

```
Returns the greatest of the nums.
```


Function code @ [github](https://github.com/clojure/clojurescript/blob/r2080/src/cljs/cljs/core.cljs#L1511-L1516):

```clj
(defn ^number max
  ([x] x)
  ([x y] (cljs.core/max x y))
  ([x y & more]
   (reduce max (cljs.core/max x y) more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2080
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:1511-1516](https://github.com/clojure/clojurescript/blob/r2080/src/cljs/cljs/core.cljs#L1511-L1516)</ins>
</pre>

-->

---

Macro code @ [github](https://github.com/clojure/clojurescript/blob/r2080/src/clj/cljs/core.clj#L450-L454):

```clj
(defmacro ^::ana/numeric max
  ([x] x)
  ([x y] `(let [x# ~x, y# ~y]
            (~'js* "((~{} > ~{}) ? ~{} : ~{})" x# y# x# y#)))
  ([x y & more] `(max (max ~x ~y) ~@more)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2080
└── src
    └── clj
        └── cljs
            └── <ins>[core.clj:450-454](https://github.com/clojure/clojurescript/blob/r2080/src/clj/cljs/core.clj#L450-L454)</ins>
</pre>
-->

---


###### External doc links:

[`clojure.core/max` @ clojuredocs](http://clojuredocs.org/clojure.core/max)<br>
[`clojure.core/max` @ grimoire](http://conj.io/store/v1/org.clojure/clojure/1.7.0-beta3/clj/clojure.core/max/)<br>
[`clojure.core/max` @ crossclj](http://crossclj.info/fun/clojure.core/max.html)<br>
[`cljs.core/max` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/max.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/max.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:description "Returns the greatest number argument.",
 :return-type number,
 :ns "cljs.core",
 :name "max",
 :signature ["[x]" "[x y]" "[x y & more]"],
 :history [["+" "0.0-927"]],
 :type "function/macro",
 :related ["cljs.core/min" "cljs.core/max-key"],
 :full-name-encode "cljs.core/max",
 :source {:code "(defn ^number max\n  ([x] x)\n  ([x y] (cljs.core/max x y))\n  ([x y & more]\n   (reduce max (cljs.core/max x y) more)))",
          :title "Function code",
          :repo "clojurescript",
          :tag "r2080",
          :filename "src/cljs/cljs/core.cljs",
          :lines [1511 1516]},
 :extra-sources [{:code "(defmacro ^::ana/numeric max\n  ([x] x)\n  ([x y] `(let [x# ~x, y# ~y]\n            (~'js* \"((~{} > ~{}) ? ~{} : ~{})\" x# y# x# y#)))\n  ([x y & more] `(max (max ~x ~y) ~@more)))",
                  :title "Macro code",
                  :repo "clojurescript",
                  :tag "r2080",
                  :filename "src/clj/cljs/core.clj",
                  :lines [450 454]}],
 :full-name "cljs.core/max",
 :clj-symbol "clojure.core/max",
 :docstring "Returns the greatest of the nums."}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/max"]))
```

-->