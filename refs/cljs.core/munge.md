## cljs.core/munge



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>

<samp>(munge name)</samp><br>

---

 <samp>
(__munge__ name)<br>
</samp>

---







Source code @ [github]():

```clj
(defn munge [name]
  (let [name' (munge-str (str name))
        name' (cond
                (identical? name' "..") "_DOT__DOT_"
                (js-reserved? name') (str name' "$")
                :else name')]
    (if (symbol? name)
      (symbol name')
      (str name'))))
```

<!--
Repo - tag - source tree - lines:

 <pre>

</pre>

-->

---



###### External doc links:

[`cljs.core/munge` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/munge.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/munge.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "munge",
 :signature ["[name]"],
 :name-encode "munge",
 :history [["+" "1.7.10"]],
 :type "function",
 :full-name-encode "cljs.core/munge",
 :source {:code "(defn munge [name]\n  (let [name' (munge-str (str name))\n        name' (cond\n                (identical? name' \"..\") \"_DOT__DOT_\"\n                (js-reserved? name') (str name' \"$\")\n                :else name')]\n    (if (symbol? name)\n      (symbol name')\n      (str name'))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.8.40",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [10316 10324],
          :url "https://github.com/clojure/clojurescript/blob/r1.8.40/src/main/cljs/cljs/core.cljs#L10316-L10324"},
 :usage ["(munge name)"],
 :full-name "cljs.core/munge",
 :cljsdoc-url "https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/munge.cljsdoc"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/munge"]))
```

-->