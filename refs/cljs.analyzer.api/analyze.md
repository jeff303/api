## cljs.analyzer.api/analyze



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3208"><img valign="middle" alt="[+] 0.0-3208" title="Added in 0.0-3208" src="https://img.shields.io/badge/+-0.0--3208-lightgrey.svg"></a> </td>
</tr>
</table>

<samp>(analyze env form)</samp><br>
<samp>(analyze env form name)</samp><br>
<samp>(analyze env form name opts)</samp><br>
<samp>(analyze state env form name opts)</samp><br>

---

 <samp>
(__analyze__ env form)<br>
</samp>
 <samp>
(__analyze__ env form name)<br>
</samp>
 <samp>
(__analyze__ env form name opts)<br>
</samp>
 <samp>
(__analyze__ state env form name opts)<br>
</samp>

---





Source docstring:

```
Given an environment, a map containing {:locals (mapping of names to bindings), :context
(one of :statement, :expr, :return), :ns (a symbol naming the
compilation ns)}, and form, returns an expression object (a map
containing at least :form, :op and :env keys). If expr has any (immediately)
nested exprs, must have :children [exprs...] entry. This will
facilitate code walking without knowing the details of the op set.
```


Source code @ [github]():

```clj
(defn analyze
  ([env form] (analyze env form nil))
  ([env form name] (analyze env form name nil))
  ([env form name opts]
   (analyze
     (if-not (nil? env/*compiler*)
       env/*compiler*
       (env/default-compiler-env opts))
     env form name opts))
  ([state env form name opts]
   (env/with-compiler-env state
     (binding [ana/*cljs-warning-handlers* (:warning-handlers opts ana/*cljs-warning-handlers*)]
       (ana/analyze env form name opts)))))
```

<!--
Repo - tag - source tree - lines:

 <pre>

</pre>

-->

---



###### External doc links:

[`cljs.analyzer.api/analyze` @ crossclj](http://crossclj.info/fun/cljs.analyzer.api/analyze.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.analyzer.api/analyze.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.analyzer.api",
 :name "analyze",
 :signature ["[env form]"
             "[env form name]"
             "[env form name opts]"
             "[state env form name opts]"],
 :name-encode "analyze",
 :history [["+" "0.0-3208"]],
 :type "function",
 :full-name-encode "cljs.analyzer.api/analyze",
 :source {:code "(defn analyze\n  ([env form] (analyze env form nil))\n  ([env form name] (analyze env form name nil))\n  ([env form name opts]\n   (analyze\n     (if-not (nil? env/*compiler*)\n       env/*compiler*\n       (env/default-compiler-env opts))\n     env form name opts))\n  ([state env form name opts]\n   (env/with-compiler-env state\n     (binding [ana/*cljs-warning-handlers* (:warning-handlers opts ana/*cljs-warning-handlers*)]\n       (ana/analyze env form name opts)))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.8.40",
          :filename "src/main/clojure/cljs/analyzer/api.clj",
          :lines [68 86],
          :url "https://github.com/clojure/clojurescript/blob/r1.8.40/src/main/clojure/cljs/analyzer/api.clj#L68-L86"},
 :usage ["(analyze env form)"
         "(analyze env form name)"
         "(analyze env form name opts)"
         "(analyze state env form name opts)"],
 :full-name "cljs.analyzer.api/analyze",
 :docstring "Given an environment, a map containing {:locals (mapping of names to bindings), :context\n(one of :statement, :expr, :return), :ns (a symbol naming the\ncompilation ns)}, and form, returns an expression object (a map\ncontaining at least :form, :op and :env keys). If expr has any (immediately)\nnested exprs, must have :children [exprs...] entry. This will\nfacilitate code walking without knowing the details of the op set.",
 :cljsdoc-url "https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.analyzer.api/analyze.cljsdoc"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.analyzer.api/analyze"]))
```

-->