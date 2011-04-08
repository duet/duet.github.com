---
layout: default
title: Duet Object Lifecycle
---
# {{page.title}}

A duet object goes through several different states during its lifespan and there are specific actions that can be called on a duet to move it from one state to another.  The diagram below illustrates this.

<img src="/images/duet-object-lifecycle.png" alt="{{page.title}}">

Some important notes:

<ul class="text">
  <li>The body of duet can only be edited as long as a duet has not been proposed to someone (i.e. it is in the unpaired state).</li>
  <li>Once a duet has been proposed to someone, it can only be accepted or declined by that person.</li>
  <li>If a duet is declined by the person you proposed it to, you can then (re-)propose the duet to another person.</li>
  <li>Once a proposed duet is accepted it will be in the active state.  From there is can be canceled or completed by either of the parties involved in the duet.</li>
  <li>If a duet is active and is canceled by one of the participating parties, it is moved into the declined state.  The other party involved then has the option to propose the duet to someone else, or, if they opt to cancel the duet as well, destroy the duet.</li>
</div>