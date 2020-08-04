---
layout: default
title: Menu Button
parent: Menus
grand_parent: Components
nav_order: 3

---

# Menu Buttons

Here is an example of the menu button being activated on the click event.
<div class="code-example">
<nav>
	<button id="menu-btn-example1" aria-expanded="false" aria-haspopup="true">Press me!</button>
		<ul role="menu" class="menu-btn-example-ul" hidden>
			<li>
			<a href="#" role="menuitem">Option 1</a>
		</li>
		<li>
			<a href="#" role="menuitem">Option 2</a>
		</li>
		<li>
			<a href="#" role="menuitem">Option 3</a>
		</li>
</nav>
</div>
{% highlight html %}
<nav>
	<button id="menu-btn-example"  aria-expanded="false" aria-haspopup="true">Press me!</button>
	<ul class="menu-btn-example-ul" role="menu" hidden>
		<li>
			<a href="#" role="menuitem">Option 1</a>
		</li>
		<li>
			<a href="#" role="menuitem">Option 2</a>
		</li>
		<li>
			<a href="#" role="menuitem">Option 3</a>
		</li>
	</ul>
</nav>
	
{% endhighlight %}

{% highlight js %}
const menuButton = document.getElementById('menu-btn-example');

menuButton.addEventListener('click', function(){
	let expanded = this.getAttribute('aria-expanded') === 'true';
	this.setAttribute('aria-expanded', !expanded);
	let exampleMenu = this.nextElementSibling;
	exampleMenu.hidden = !exampleMenu.hidden;
})

{% endhighlight %}