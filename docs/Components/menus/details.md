
What's that? An HTML accordion you say? Yup! It's called the <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details">HTML Details Element.</a>
<div class="code-example">
<details>
  <summary>OOOH, WHAT'S IN THERE?</summary>
  <p>IT'S A PUPPY!</p>
  <img src="{{site.baseurl}}/assets/images/this is fine.gif" alt="dog sits in burning house drinking coffee sating, this is fine"/>
</details>
{% highlight html %}
<details>
  <summary>OOOH, WHAT'S IN THERE?</summary>
  <p>IT'S A PUPPY!</p>
  <img src="assets/images/this is fine.gif" />
</details>
</div>
{% endhighlight %}

Pretty cool, right? Thought so. As of July 2020, it's accessible out of the box -- although I did notice in my testing that the "expanded" and "collapsed" states are not toggled when there is no SUMMARY element nested in the DETIALS element.

The DETAILS element supports the TOGGLE event, so adding more functionality to it is pretty straightforward.
{% highlight js %}
details.addEventListener("toggle", event => {
  if (details.open) {
    /* the element was toggled open */
    //do awesome thing!
    } else {
      /* the element was toggled closed */
      // undo awesome thing
    }
  });
{% endhighlight %}