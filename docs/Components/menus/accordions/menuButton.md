---
layout: default
title: Menu Button
parent: Menus
grand_parent: Components
nav_order: 3

---

# Menu Buttons

<div class="code-example">
	<button class="menu-btn-example">
		<ul class="menu-btn-example-ul" aria-expanded="false">
			<li>
				<a>Option 1</a>
			</li>
			<li>
				<a>Option 2</a>
			</li>
			<li>
				<a>Option 3</a>
			</li>
		</ul>
	</button>
</div>
{% highlight html %}
{% endhighlight %}

{% highlight css %}
.d-none {
  display: none !important;
}
.d-block {
  display: block !important;
}
.menu-btn-example {
	
}

{% endhighlight %}
{% highlight js %}
const menuButton = document.querySelector('menu-btn-example');

menuButton.addEventListener('click', function(){
	let expanded = this.getAttribute('aria-expanded') === 'true';
	this.setAttribute('aria-expanded', !expanded);
	let exampleMenu = this.nextElementSibling;
	exampleMenu.hidden = !menu.hidden;
})

{% endhighlight %}