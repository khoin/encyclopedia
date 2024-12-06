---
layout: blank
title: Koi Nil

---

<style>
:root {
	--card-height: 80%;
}

.card {
	width: 100%;
	height: var(--card-height); 
	left: 0;
	top: 0;
	display: flex;
	align-items: center;
	padding: 6vh;
	box-sizing: border-box;
	font-size: 7vh;
	font-style: italic;
}

#t1 {
	background: whitesmoke;
	color: cadetblue;
}

#t2 {
	top: calc(var(--card-height) * 1);
	background: cadetblue;
	color:whitesmoke;
}
#t2 a { color: whitesmoke; margin: auto 5pt; }

#nan ~ * { display: none; }

</style>

<div class="card" id="t1">
koi.<br>nil.<br>seattle.<br>wa.<br>us
</div>

<div class="card" id="t2">
	<div>
	<a href="" onclick="alert('please email me with your inquiry: koi at nil.seattle.wa.us')">résumé</a>
	<a href="https://www.linkedin.com/in/kpn/">linkedin</a><br>
	<span id="hr1">--</span> <span id="hr2">--</span> <br>
	<a href="https://instagram.com/koi.nil.seattle.wa.us">instagram</a>
	<a href="https://github.com/khoin">github</a>
	</div>
</div>

<div id="nan">&nbsp;
</div>

<script>
let ppp = "";
hr2.onclick = e => { ppp += (ppp & 0x20)? nan.id++ :  "1"; }
</script>


# Notebook

{% include nav.html %}

Welcome to my notebook! I created this when I was at the [University of Washington](uw). The first 12 articles were made there (2017-2019).

In 2024, I had some more time to revisit this notebook and turned the section above into a "link tree". I will soon resume writing, or adapt writings from other platforms that I've written over the past years.

To follow this notebook, subscribe to the RSS **Feed** -- linked at the bottom of the page. The RSS Feed is the only place where pages are sorted by their published date.

The nature of a notebook is that: it is personal and opinionated; it records what I encountered, researched, and thought. But a notebook is also a sketching ground for ideas, fantasies and fiction. I don't say which pages are which; I can't even claim to _know_ which pages are which.

Contact: <a href="mailto:koi@nil.seattle.wa.us">koi@nil.seattle.wa.us</a>

----

{% include footer.html %}