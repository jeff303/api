## cljs.core/\*print-err-fn\*



 <table border="1">
<tr>
<td>dynamic var</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/1.7.10"><img valign="middle" alt="[+] 1.7.10" title="Added in 1.7.10" src="https://img.shields.io/badge/+-1.7.10-lightgrey.svg"></a> </td>
</tr>
</table>







Source docstring:

```
Each runtime environment provides a different way to print error output.
Whatever function *print-fn* is bound to will be passed any
Strings which should be printed.
```


Source code @ [github]():

```clj
(defonce
  ^{:doc "Each runtime environment provides a different way to print error output.
  Whatever function *print-fn* is bound to will be passed any
  Strings which should be printed." :dynamic true}
  *print-err-fn*
  (fn [_]
    (throw (js/Error. "No *print-err-fn* fn set for evaluation environment"))))
```

<!--
Repo - tag - source tree - lines:

 <pre>

</pre>

-->

---



###### External doc links:

[`cljs.core/*print-err-fn*` @ crossclj](http://crossclj.info/fun/cljs.core.cljs/*print-err-fn*.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/STARprint-err-fnSTAR.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.core",
 :name "*print-err-fn*",
 :name-encode "STARprint-err-fnSTAR",
 :history [["+" "1.7.10"]],
 :type "dynamic var",
 :full-name-encode "cljs.core/STARprint-err-fnSTAR",
 :source {:code "(defonce\n  ^{:doc \"Each runtime environment provides a different way to print error output.\n  Whatever function *print-fn* is bound to will be passed any\n  Strings which should be printed.\" :dynamic true}\n  *print-err-fn*\n  (fn [_]\n    (throw (js/Error. \"No *print-err-fn* fn set for evaluation environment\"))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.8.40",
          :filename "src/main/cljs/cljs/core.cljs",
          :lines [51 57],
          :url "https://github.com/clojure/clojurescript/blob/r1.8.40/src/main/cljs/cljs/core.cljs#L51-L57"},
 :full-name "cljs.core/*print-err-fn*",
 :docstring "Each runtime environment provides a different way to print error output.\nWhatever function *print-fn* is bound to will be passed any\nStrings which should be printed.",
 :cljsdoc-url "https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.core/STARprint-err-fnSTAR.cljsdoc"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.core/*print-err-fn*"]))
```

-->