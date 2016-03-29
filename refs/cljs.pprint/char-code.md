## cljs.pprint/char-code



 <table border="1">
<tr>
<td>function</td>
<td><a href="https://github.com/cljsinfo/cljs-api-docs/tree/0.0-3255"><img valign="middle" alt="[+] 0.0-3255" title="Added in 0.0-3255" src="https://img.shields.io/badge/+-0.0--3255-lightgrey.svg"></a> </td>
</tr>
</table>

<samp>(char-code c)</samp><br>

---

 <samp>
(__char-code__ c)<br>
</samp>

---





Source docstring:

```
Convert char to int
```


Source code @ [github]():

```clj
(defn char-code
  [c]
  (cond
    (number? c) c
    (and (string? c) (== (.-length c) 1)) (.charCodeAt c 0)
    :else (throw (js/Error. "Argument to char must be a character or number"))))
```

<!--
Repo - tag - source tree - lines:

 <pre>

</pre>

-->

---



###### External doc links:

[`cljs.pprint/char-code` @ crossclj](http://crossclj.info/fun/cljs.pprint.cljs/char-code.html)<br>

---

 <table>
<tr><td>
<img valign="middle" align="right" width="48px" src="http://i.imgur.com/Hi20huC.png">
</td><td>
Created for the upcoming ClojureScript website.<br>
[edit here] | [learn how]
</td></tr></table>

[edit here]:https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.pprint/char-code.cljsdoc
[learn how]:https://github.com/cljsinfo/cljs-api-docs/wiki/cljsdoc-files

<!--

This information was too distracting to show to readers, but I'll leave it
commented here since it is helpful to:

- pretty-print the data used to generate this document
- and show how to retrieve that data



The API data for this symbol:

```clj
{:ns "cljs.pprint",
 :name "char-code",
 :signature ["[c]"],
 :name-encode "char-code",
 :history [["+" "0.0-3255"]],
 :type "function",
 :full-name-encode "cljs.pprint/char-code",
 :source {:code "(defn char-code\n  [c]\n  (cond\n    (number? c) c\n    (and (string? c) (== (.-length c) 1)) (.charCodeAt c 0)\n    :else (throw (js/Error. \"Argument to char must be a character or number\"))))",
          :title "Source code",
          :repo "clojurescript",
          :tag "r1.8.40",
          :filename "src/main/cljs/cljs/pprint.cljs",
          :lines [62 68],
          :url "https://github.com/clojure/clojurescript/blob/r1.8.40/src/main/cljs/cljs/pprint.cljs#L62-L68"},
 :usage ["(char-code c)"],
 :full-name "cljs.pprint/char-code",
 :docstring "Convert char to int",
 :cljsdoc-url "https://github.com/cljsinfo/cljs-api-docs/blob/master/cljsdoc/cljs.pprint/char-code.cljsdoc"}

```

Retrieve the API data for this symbol:

```clj
;; from Clojure REPL
(require '[clojure.edn :as edn])
(-> (slurp "https://raw.githubusercontent.com/cljsinfo/cljs-api-docs/catalog/cljs-api.edn")
    (edn/read-string)
    (get-in [:symbols "cljs.pprint/char-code"]))
```

-->