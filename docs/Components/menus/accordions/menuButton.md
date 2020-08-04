---
layout: default
title: Menu Button
parent: Menus
grand_parent: Components
nav_order: 3

---

# Menu Buttons

<div class="code-example">
<nav>
	<button id="menu-btn-example"  aria-expanded="false">
		Press me!
		<ul class="menu-btn-example-ul" hidden>
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
</nav>
</div>
{% highlight html %}
<nav>
	<button id="menu-btn-example"  aria-expanded="false">Press me!</button>
	<ul class="menu-btn-example-ul" hidden>
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