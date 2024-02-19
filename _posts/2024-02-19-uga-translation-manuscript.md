---
layout: post
title:  "New article: Evolution of UGA codon translation in ciliates"
date:   2024-02-19
categories: publications
---

A new paper from my former lab is out as a reviewed preprint in eLife. It's a
short manuscript written in response to a study from another lab on stop codon
reassignment.

[Swart EC, Emmerich C, Seah BKB, Singh M, Shulgina Y, Singh A. 2024. "How did
UGA codon translation as tryptophan evolve in certain ciliates? A critique of
Kachale et al. 2023 Nature", *eLife* 93502.1](https://doi.org/10.7554/eLife.93502.1)


## Background - Alternative genetic codes

The genetic code, which specifies which codons in
mRNA are translated into which amino acids in proteins, is "universal" in the
sense that all cellular life uses a genetic code, but these codes are not all
identical. Many organisms use alternative codes, that typically differ in one
or a handful of codons that code for different amino acids compared to the
"standard" code (egotistically, the "standard code" is the one used by us
humans and other vertebrate animals).

The most intriguing alternative codes are the ones where stop codons are
repurposed to code for amino acids. If a stop codon is reassigned to code for
an amino acid, you'd expect to find a tRNA with the complementary anticodon.
However, organisms that recode the stop codon UGA to tryptophan were especially
puzzling because the corresponding tRNA was not found in their genomes.
UGA->Tryptophan has evolved at least four times. All known cases are in
microbial eukaryotes, including twice in the ciliates, which are the group that
my former lab's research was focussed on.


## What the earlier study claims

[A study](https://www.nature.com/articles/s41586-022-05584-2) published just
over a year ago found the likely answer to the question of the missing tRNA:
instead of a typical tRNA with a 5 base-pair anticodon stem structure and the
expected anticodon UCA, they use a tRNA with a 4 base-pair stem and the
anticodon CCA. They showed that this tRNA is found in two different organisms,
a tryposomatid species with the apt moniker [*Blastocrithidia
nonstop*](https://doi.org/10.1016/j.cub.2016.06.064), and a ciliate
*Condylostoma magnum*. They engineered 4-bp variant tRNAs in other model
species and showed that the variants increased the rate of translational
"readthrough" of the erstwhile stop codons, evidence that they are indeed
binding to UGAs to translate them.

They also reported that a specific point mutation in the protein eRF1
(eukaryotic release factor 1), a key player in translation termination, is
associated with UGA->Tryptophan. eRF1 is involved in recognizing the stop codon
and releasing the nascent polypeptide chain, as its full name implies. They
argued that this mutation was also necessary for UGA reassignment, by reducing
the ability of eRF1 to recognize UGA. If so, it would no longer compete as much
with the tRNA for UGAs, facilitating their translation.


## What we found by looking at more species

It's the second claim about the mutant eRF1 that our article responds to,
because it doesn't hold up if we look at more species. We dug into the genomic
data for different species of ciliates, taking advantage of how incredibly
diverse they are in the genetic codes that they use. The data covered species
using a number of different codes, some with the UGA->Tryptophan reassignment,
others without. However, the mutation in eRF1 was not correlated at all with
the UGA reassignment: some had the mutation, others didn't. In contrast, we
found the 4-bp stem variant tRNA in all species with UGA reassignment, lending
support to their first point.

So why does this matter? The authors of the earlier study hypothesized that the
mutation was mechanistically relevant, that eRF1 was "giving way" to tRNAs, so
to speak. We think instead that this mutation is not necessary for this trait,
and indeed there are signs in the genomes of some ciliates that there is still
competition between tRNA and eRF1 for binding with UGAs, so alternative models
for the evolution of this stop codon reassignment are still not ruled out.


--- 

## Thoughts on the eLife publishing model

This is our first time publishing in eLife, which was founded as a nonprofit
life sciences publisher in 2012 by three major scientific organizations. Since
then it has been a platform for trying out different models of peer review and
scientific publishing. At the end of 2022 they switched away from the
traditional "accept/reject" model of publication. All manuscripts submitted
have to be already publicly accessible as "preprints". Editors still decide
whether or not to send a manuscript out for review, but if sent for peer
review, they will be published alongside their reviews, as "reviewed
preprints". Authors can choose to revise and resubmit a final "version of
record". As a comparison, in most journals, crossing the editor's desk is the
first hurdle, but if reviews are negative (or worse - one positive and one
negative...) they can still be rejected for publication.

I think this is a step forward. Yes, editors still act as gatekeepers, but they
are there in the traditional model too. The advance here is to save on the time
and uncompensated labor when a paper is sent for review but rejected and is
then shopped around to other journals, where the process is repeated until it's
either accepted or the authors give up. Each round represents time invested by
authors in submitting, waiting and responding to reviews, and also by peer
reviewers and editors.

I can see how there would be more pressure on editors to be discerning in what
they send out for review. Hypothetically, in the traditional model, an editor
could indiscriminately send everything for review, regardless of quality, and
just wait for the reviewers to filter out the bad ones. That's of course a huge
waste of everyone's time, but no one would ever know because the rejected
papers never see the light of day, at least in that editor's journal. In the
eLife model, the reviewed preprints are posted alongside the reviews, with a
short assessment of their significance and quality of evidence. Editors' names
are publicly linked to the papers, so one could with time see trends in how
they perform.

This is not our first time publishing under a "post-publication review" model.
In 2022 we published a [paper](https://doi.org/10.24072/pcjournal.141)
(incidentally also on genetic codes) in Peer Community Journal, part of the
larger [Peer Community In](https://peercommunityin.org/) initiative, which has
a very similar approach. They only review publicly available preprints, editors
choose which submitted papers will be sent for review, and the reviews are
published alongside the manuscript. One point that may be different in their
process is that if reviews are negative, authors can decide not to proceed
further, and these will then not be published. I'm not sure if eLife has this
option, too.

More significantly, PCI is "diamond open access" - free for readers and also
free for authors to publish there. eLife charges a fee of USD 2000 (previously
USD 3000), although waivers are available. This is on the lower end compared to
most conventional journals. Prestige journals like Nature and Science don't
charge publication fees but are subscription only (not open access), but their
"companion" journals charge high fees for open access: USD 6790 at Nature
Communications, USD 2590 at Scientific Reports. Anything that pushes against
this inflationary trend is worth looking into.
