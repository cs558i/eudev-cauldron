## eudev-cauldron

# eudev action plan/topics for discussion

Please prefix your proposed edits by your nick, e.g. (whoever) whatever

(bb|hcb) eudev-project action plan https://github.com/eudev-project/eudev

I)) Annouce adoption in progress; current text, I have already commited it to avoid confusion:

ADOPTION NOTICE (2021-09-14)

Currently eudev is in the process of being adopted by a newly formed project by Alpine, Devuan and Gentoo contributors (a-z order). Some of the below links and/or contacts may be outdated until the process is complete and all the infra set up.

As of now we are hanging on ircs://irc.libera.chat:6697/#eudev  https://web.libera.chat/#eudev    https://libera.chat/

II)) Before editing the README, lets first make consensus on the following topics:

1) Do we need a home page, besides https://github.com/eudev-project/eudev

  - (golinux) Premature at this point IMO.
    - (bb|hcb) Had to ask for completeness; I believe that even in the long run we don't
  - (bb|hcb) No objections/ideas, I would consider this one solved, with resolution: we don't

2) Do we need separate releases, as long as we can publish xz and xz.asc along with the gh tag based ones

  - (plasma41) Separate from what exactly?
     - (golinux) I assume the other participating distributions
  - (bb|hcb) There is http://dev.gentoo.org/~blueness/eudev/ Instead of setting separate page, I think that uploading the .xz and .xz.asc in the GH release should suffice; of course supporting signed tags, git-archive and etc. modern stuff is welcome. About distributions - nothing should change besides the upstream (this project) tarball/git url
  - (bb|hcb) No objections/ideas, I would consider this one solved, with resolution: we don't

3) Let's delay IRC channels until the rename/redirect/log are done for the new one; also the plan is to ask blueness to do the redirect for the #gentoo-eudev one, so we gather everyone interested in a single place (joerg, bb|hcb - both tasks done)

  - (bb|hcb) #devuan-eudev is redirected; #gentoo-udev will continue to be active but focusing on systemd separated udev - then both redirect/note are not needed

4) We need to rework the Committers section - I would insist on keeping people formerly involved in some way, that does not attract reports and questions to them

5) We need to setup CI (as with IRC I am lacking in this and will rely on help)

  - (bb|hcb) Thanks to Arsen this is done

6) Ask blueness to add link/redirect in Gentoo eudev's home page (https://wiki.gentoo.org/wiki/Project:Eudev) to this project; also add a note on http://dev.gentoo.org/~blueness/eudev/ that these are historic and point to the new ones

7) [least urgent] I have put some quick gimp made image in the project, feel free to propose a better one

  - (plasma41) Who is "I" and why are images needed for a device manager?
     - (golinux) There is a simple project logo which I believe bb put together since he authored this document.  You can see it here: https://github.com/eudev-project  If this project gets some traction, we might want something more memorable.  Certainly not a priority atm.
  - (bb|hcb) Exactly

III)) After finalizing the above, lets decide on review/clear/merge non-upstream stuff

1) Decide on pushing changes in master - e.g. propose, 2 reviews with approve and then merge; or maybe something simpler, but it will be for the best to follow blueness' advice and throw away our hubris and always go via some kind of review before pushing changes...

  - (Ariadne) if it has one review, it should be fine.  small team, avoid bureaucracy imo.

  - (bb|hcb) Yep, should be OK

2) Process the various distribution specific patches out there and merge the appropriate ones:
https://git.devuan.org/devuan/eudev/src/branch/suites/unstable/debian/patches

3) PRs on GH

4) Issues on GH (that goes best together with the upstream changes review - it may help closing some of those)

IV)) Start syncing upstream [to be expanded, split between people, etc.]

  - (bb|hcb) Two approaches discussed:
    1. File PRs for things that differ from systemd in current code base (bb|hcb started doing that)
    2. Re-fork again as branch eudev-5 (Arsen is working on that)

(Arsen) I am unable to fully commit to this, but I have began this effort and researched into it:
https://git.sr.ht/~arsen/eudev-new/
https://git.sr.ht/~arsen/eudev-new/tree/master/item/tools/systemd_upstream_filter.py
https://git.aarsen.me/systemd-udevonly.git/
Do reach out on IRC about it.


