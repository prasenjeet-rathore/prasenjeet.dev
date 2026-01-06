+++
title = ""
layout = "home"
+++

<div class="hx:mx-auto hx:max-w-5xl hx:py-12 hx:px-6">
  <h1 class="hx:mt-2 hx:text-4xl hx:font-bold hx:tracking-tight hx:text-slate-900 hx:dark:text-slate-100">Hi, Welcome to my blog 👋</h1>
  <p class="hx:mt-4 hx:text-lg hx:text-gray-600 hx:dark:text-neutral-300">
    I am a Data Scientist working in ING Hubs on credit risk modeling.
  </p>
</div>



<div class="hx:mx-auto hx:max-w-5xl hx:px-6 hx:pt-10 hx:pb-12">
  <div class="hx:flex hx:items-center hx:justify-between hx:mb-4">
    <h2 class="hx:text-2xl hx:font-semibold hx:text-gray-900 hx:dark:text-gray-50">Latest posts</h2>
    <a href="/blog" class="hx:text-sm hx:text-primary-600 hx:dark:text-primary-400">View all</a>
  </div>
  {{< posts-cards limit="4" section="blog" >}}
</div>
