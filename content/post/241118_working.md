---
title: "A Better Search Engine?"
date: 2024-11-17
draft: true
Tags: ["Tag 1", "Tag 2", "Tag 3", "Tag 4"]
---

For the month of October 2024, the [Self Hosted](https://selfthosted.show) gang have been trying to go the month without using Google's search engine. I've been busy with other things and hadn't taken part, but in their [most recent](https://selfhosted.show/136) show, Alex and Chris were talking very highly of two self hosted services they had been making use of during the month.

The first one, [SearXNG](https://github.com/searxng/searxng) is a self hosted meta search engine. In stupid speech (in other words something ***I*** can understand), it takes you search query and farms it out to multiple other search engines. It then does "something" and presents what is more likely (hopefully) what you were actually looking for.

I had played with this project a couple of years ago and found it wasn't of much use, however Chris and Alex convinced me to give it another go, and there have been some significant improvements over the years, most notably the ability to search the Fedi. That's useful. As was the case the last time, the most difficult part of setting it up was getting my browsers to use it as their default search engine. At least it was until I figured out that I could add it as a search engine by going to the page, right clicking the URL and selecting the option to add it as a search engine. That's new. Firefox on mobile was even easier. Safari, not so much. Still working on that one. It does look like there is an extention to allow new search providers though.

The second service, [Perplexica](https://github.com/ItzCrazyKns/Perplexica), I haven't yet tried, but seems to be an LLM frontend to SearXNG. From the looks of it you can give it a question, it will start a search and summerize what it has found citing sources. But it is not an LLM itself, instead it hooks into whatever LLM backend you want and uses that to do the actual processing.
