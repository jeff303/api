## cljs.core/entries-iterator



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-2268"><img valign="middle" alt="[+] 0.0-2268" title="Added in 0.0-2268" src="https://img.shields.io/badge/+-0.0--2268-lightgrey.svg"></a> </td>
</tr>
</table>


 <samp>
(__entries-iterator__ coll)<br>
</samp>

---







Source code @ [github](https://github.com/clojure/clojurescript/blob/r2277/src/cljs/cljs/core.cljs#L4379-L4380):

```clj
(defn entries-iterator [coll]
  (EntriesIterator. (seq coll)))
```

<!--
Repo - tag - source tree - lines:

 <pre>
clojurescript @ r2277
└── src
    └── cljs
        └── cljs
            └── <ins>[core.cljs:4379-4380](https://github.com/clojure/clojurescript/blob/r2277/src/cljs/cljs/core.cljs#L4379-L4380)</ins>
</pre>

-->

---



###### External doc links:

[`cljs.core/entries-iterator` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/entries-iterator.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/entries-iterator.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "entries-iterator",
 :type "function",
 :signature ["[coll]"],
 :source {:code "(defn entries-iterator [coll]\n  (EntriesIterator. (seq coll)))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r2277",
          :filename "src/cljs/cljs/core.cljs",
          :lines [4379 4380]},
 :full-name "cljs.core/entries-iterator",
 :full-name-encode "cljs.core/entries-iterator",
 :history [["+" "0.0-2268"]]}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/entries-iterator"]))
```

-->