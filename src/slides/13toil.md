---
title: 'Google SRE: Toil'
type: 'content'
order: 13
part: 'frameworks'
section: 'toil'
---

<div class="not-prose text-sm uppercase tracking-[0.2em] text-teal-600 font-mono mb-6">Industry Frameworks · Toil</div>

Google's _Site Reliability Engineering_ discipline names a specific category of work: **Toil**.

Manual, repetitive work that grows linearly with the system — regardless of the value it delivers.

<div class="not-prose grid grid-cols-2 gap-5 mt-6">
  <div class="bg-gray-900 rounded-2xl p-7 flex flex-col gap-3">
    <div class="text-sm uppercase tracking-widest text-gray-500">Examples</div>
    <div class="text-2xl leading-relaxed">Manual deployments · manual approvals · manual certificate renewals</div>
  </div>
  <div class="bg-gray-900 rounded-2xl p-7 flex flex-col gap-3">
    <div class="text-sm uppercase tracking-widest text-gray-500">The scale problem</div>
    <div class="text-2xl leading-relaxed">If the system doubles in size, the toil doubles with it</div>
  </div>
  <div class="bg-gray-900 rounded-2xl p-7 flex flex-col gap-3">
    <div class="text-sm uppercase tracking-widest text-gray-500">The ownership link</div>
    <div class="text-2xl leading-relaxed">Models that route every decision through a human generate work that scales with system size, not value</div>
  </div>
  <div class="bg-gray-900 rounded-2xl p-7 border border-teal-900 flex flex-col gap-3">
    <div class="text-sm uppercase tracking-widest text-teal-600">SRE's answer</div>
    <div class="text-2xl leading-relaxed">Automate the toil away — permanently, not repeatedly</div>
  </div>
</div>
