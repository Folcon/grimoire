{% highlight clojure %}
(defn ex-data
  "Alpha - subject to change.
   Returns exception data (a map) if ex is an IExceptionInfo.
   Otherwise returns nil."
  {:added "1.4"}
  [ex]
  (when (instance? IExceptionInfo ex)
    (.getData ^IExceptionInfo ex)))
{% endhighlight %}
