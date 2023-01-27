These are instructions for preparing papers for the new website.
Information regarding the papers will be organized in the /bib/pracsys.bib bibtex file with a few extra tags:

img this is the file name of a 250x100px image or gif placed in the /img/papers/ folder in the github repository. Be sure to include the file extension.
projecturl (optional) this is a link to the projects webpage or github
keywords this is a set of keywords used to sort papers. Please capitalize and use the preferred keywords for consistency
abstract this one's self-explanatory, but make sure to use braces instead of quotes and remove all newlines to avoid breaking bibtex
posterlink (optional) link to pdf of poster 
videolink (optional)

preferred keywords:
Planning, Perception, Learning, Manipulation, Navigation, HRI, Tensegrity, Simulation, Estimation, Dynamics, Rearrangement, Multi-Robot

Example:
@article{a_unique_identifier,
title = {Premature Speculation on the Importance of Neural Networks},
author = {A Uthor and E Tal},
url = {https://arxiv.org/},
year  = {2022},
date = {2022-05-24},
journal = {Journal of Irreproducible Results},
img = {a_unique_identifier.gif},
projecturl = {https://github.com},
keywords = {Learning, Estimation},
abstract = {Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin fringilla condimentum leo sit amet sagittis. Nullam hendrerit, turpis at varius vestibulum, nisi arcu gravida libero, et suscipit metus magna sit amet orci.}
}

To summarize, for each of the papers assigned to you, you must:
create a 250px wide and 100px tall image or gif and upload to the /img/papers/ folder.
Add (and populate) the new tags to your bibtex entry
(optional) test compile in latex
append your entry to the /bib/pracsys.bib
Thank you!
