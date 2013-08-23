---
layout: post
title: "Common Git Command"
date: 2012-12-29 05:49
comments: true
categories: ["Rails"]
---

Undoing commit in some scenarios

1. Forgot adding files
<!-- -->
		{% codeblock %}	
		git commit --amend
		{% endcodeblock %}
2. Reset the repository to the last commited state (remove any current changes)
<!-- -->
		{% codeblock %}
		# clean stage index
		git reset --hard
		# clean unstage files
		git clean -d -f # use -n to dry-run
		{% endcodeblock %}
3. unstage
<!-- -->
		{% codeblock %}
		git reset HEAD
		{% endcodeblock %}
