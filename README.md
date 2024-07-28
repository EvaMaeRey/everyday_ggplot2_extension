
<!-- README.md is generated from README.Rmd. Please edit that file -->

# everyday ggplot2 extension

<!-- badges: start -->
<!-- badges: end -->

Website? <https://www.youtube.com/watch?v=YN75YXaLFGM>,
<https://ivelasq.rbind.io/blog/other-geoms/>

‘everyday ggplot2 extension’ is a resource for people that want to get
into ggplot2 extension but might not be confident of how to do so. The
goal is to provide you education materials that will meet you where you
are and connect you to other folks interested in ggplot2 extension. In
short, this project seeks to support a new wave of extenders.[^1]

‘Everyday’ is meant in the sense of *ordinary* – your ggplot2 extension
doesn’t need to be flashy. You don’t need to have lots of people using
your extension. You don’t need the extension to be on CRAN or even to
write a package for your extension. You don’t even need a hex sticker!
What?!

It is nice if the extension does some work just for you or just makes
you happy. Package development know-how can be complementary to ggplot2
extension, but is NOT a prerequisite. Lack of package building knowledge
shouldn’t hold back the extension-curious! We especially explore ways of
using extension without packaging.

‘Everyday’ is also meant in the sense of *frequent* – practicing ggplot2
extension will probably make you better at extension - you’ll be in a
position to write that next handy extension once when you have more
experience under your belt.

And, you might think our title evokes, ‘The Design of Everyday Things’.
That’s correct. An aim is to design new avenues for bringing people into
ggplot2 extension.

And it’s to be expected that we’ll make poorly designed ggplot2
extensions along the way. And this is fine since mistakes can sometimes
be more instructive and memorable than doing things ‘the right way’ the
first time round. It’s hard to imagine Norman’s book selling as well
without the ill-conceived tea kettle gracing the cover. In fact the
‘Norman door’ is one whose design boggles door-users expectations.
Expecting mistakes is another reason to make ggplot2 extension a less
out-of-the-ordinary experience; past extensions feel less precious and
we can part ways with them if appropriate. A deprecated package or
abandoned function may have been of great service in getting you to a
place that’s more sensible.

<img src="design_of_everyday_things.jpg" width="145" />

# How do I know there’s an opportunity for extension?

The reason ggplot2 exists is explained by Hadley Wickham in an
interview:

> And, you know, I’d get a dataset. And, *in my head I could very
> clearly kind of picture*, I want to put this on the x-axis. Let’s put
> this on the y-axis, draw a line, put some points here, break it up by
> this variable. And then, like, getting that vision out of my head, and
> into reality, it’s just really, really hard. Just, like, felt harder
> than it should be. Like, there’s a lot of custom programming involved,
> where I just felt, like, to me, I just wanted to say, like, you know,
> *this is what I’m thinking, this is how I’m picturing this plot. Like
> you’re the computer ‘Go and do it’.* … and I’d also been reading about
> the Grammar of Graphics by Leland Wilkinson, I got to meet him a
> couple of times and … I was, like, this book has been, like, written
> for me. -
> <https://www.trifacta.com/podcast/tidy-data-with-hadley-wickham/>

To paraphrase, fact that ggplot2 is built on the grammar of graphics,
with its ‘logically decomposed bits’, should let you fly through plot
creation with ease. You can go from the plot you’ve already pictured in
your head into reality by describing it.

After a good amount of time using ggplot2, you get used to this flying
sensation. You’ve practiced and mastered the grammar. You are a composer
of ‘graphical poems’. You confidently speak plots into existence. Poetry
slam!

<div class="figure">

<img src="jules_leotard.jpeg" alt="*The 'daring young man on the flying trapeze', Jules Leotard, who 'flies through the air with the greatest of ease'*" width="220" />
<p class="caption">
*The ‘daring young man on the flying trapeze’, Jules Leotard, who ‘flies
through the air with the greatest of ease’*
</p>

</div>

But then one day you may find yourself with a loss for graphical words
within ggplot2. At some point ggplot2 will seem to *fail* to give you
the fluid ggplot2 experience. One day you will find yourself saying,
’Why aren’t I flying?” This might be a moment to double-check your
grammar prowess; or it might be a moment to turn to ggplot2 extension!

You may find what you need among existing extensions, checking the
[extensions gallery](https://exts.ggplot2.tidyverse.org/gallery/) and
the [Awesome `ggplot2`](https://github.com/erikgahner/awesome-ggplot2)
repository, you can’t find what you need to fly again, you might
consider creating your own extension.

To summarize, here are some situations that indicate there might be a
ggplot2 extension opportunity:

- I don’t feel like I’m flying; but usually I do
- My brain hurts because of the plot I’m trying to build; but usually
  it’s happy or
- ‘getting that vision out of my head, and into reality, it’s just
  really, really hard… harder than it should be.’
- my amygdala is activated when I think about making a certain plot

![](README_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

<!-- > Pooh began to feel a little more comfortable, because when you are a Bear of Very Little Brain, and you Think of Things, you find sometimes that a Thing which seemed very Thingish inside you is quite different when it gets out into the open and has other people looking at it. - A.A. Milne The House at Pooh Corner (1928) ch. 6 -->

# A new ‘easy recipes’ approach to creating and using new Stats: Taste, succeed, minimally modify

layer extension recipes take the form:

- Step 0. Get the job done with ‘base’ ggplot2. It’s a good idea to
  clarify what needs to happen without getting into the extension
  architecture

- Step 1. Write a computation function. Wrap the necessary computation
  into a function.

- Step 2. Define a ggproto object. ggproto objects allow your extension
  to work together with base ggplot2 functions! You’ll use the
  computation function from step 1 to help define it.

- Step 3. Write your geom/stat\_\* function! You’re ready to write your
  function. You will incorporate the ggproto from step 2.

- Step 4. Test/Enjoy! Take your new geom for a spin! Check out
  group-wise computation behavior!

- link to easy geom recipes: first taste

- cookbook

- {statexpress} package for concisely writing

- in-script extension examples

  - 
  - 

compute_group recipes and tutorial

# Communities of practice

Communities of practice can help motivate and sustain productivity of
projects.

- [ggplot2
  extenders](https://github.com/teunbrand/ggplot-extension-club) has met
  since

- [discussion](https://github.com/teunbrand/ggplot-extension-club/discussions)
  Extenders can share their good ideas which maybe they don’t have quite
  the skills or knowledge to execute on; or maybe they are just missing
  a comma! The
  [ggproto](https://stackoverflow.com/questions/tagged/ggproto) tag on
  StackOverflow is similar but might be dominated by more advanced
  users.)

- stalwarts; long-time ggplot2 extenders and developers

‘everyday ggplot2 extension’ would like to point you to new communities
of practice – places were you can share work and frustrations in the
ggplot2 world:

- warming up; \[<https://github.com/teunbrand/ggplot-extension-club>\]

I’m hopeful that an ‘absolute newcomers’ group may develop; this could
consist of ggplot2 super-users, no extension experience [tutorial
evaluation is underway and focus group may seed absolute newcomers
group](https://github.com/EvaMaeRey/easy-geom-recipes) and their
collaborators (is it cool and fun to explore the ggplot2 extension space
w/ absolute newcomers *to ggplot2 and R* - yes it is!). It might spin
off of the focus groups for the ‘easy geom recipes’ evaluation.

‘everyday ggplot2 extension’ promotes the ‘warming up’ group and aspires
to serve an ‘absolute newcomers’ group; and to promote cross pollination
between groups.

- [ggpuzzles](https://github.com/EvaMaeRey/ggpuzzles) is a place to demo
  minimal not-yet-working examples. Extenders can share their good ideas
  which maybe they don’t have quite the skills or knowledge to execute
  on; or maybe they are just missing a comma! The
  [ggproto](https://stackoverflow.com/questions/tagged/ggproto) tag on
  StackOverflow is similar but might be dominated by more advanced
  users.

## Read along packages

- ggcalendar

- gg

## By subject area of application

- stats101verse

  - \[ggxmean\]
  - \[ggols\]
  - \[ggsample\]
  - \[ma206data\]
  - \[ma206distributions\]
  - \[ma206equations\]

<!-- https://www.newyorker.com/books/page-turner/the-allure-of-the-map#:~:text=Stevenson%20writes%2C%20in%20an%20essay,predestined%2C%20I%20ticketed%20my%20performance%20'-->

### Spatial

<https://ivelasq.rbind.io/blog/leaidr2/> school district maps

> I am told there are people that don’t care for maps, and I find it
> hard to believe. - Robert Louis Stevenson

- \[ggamericas\] is an experiment in the geomSf-inheritance space,
  seeking to foster cross-package synergies, lessons learned, and
  emergence of best practices. The following packages are in the works
  and are proposed as early guides in this space:

  - [ggfips](https://github.com/EvaMaeRey/ggfips)

  - [ggnorthcarolina]()

  - [ggbrazil](https://github.com/EvaMaeRey/ggbrazil)

  - 

  <!-- -->

  - tidypivot
  - ggcirclepack

<!-- Shiny linkage... -->
<!--  - [codequoteforshiny] When you just want to talk about and manipulate the contents of a plot and not dig into the weeds of how to get there, shiny apps are great!  But if you are writing tools to make ggplot2 interfaces that make the code a closer match with how we think about the plot "getting the picture out of our heads", than you'll probably also want to quote the code!  Looking at the code shouldn't feel too "in the weeds" because of the grammar of graphic's conceptual mapping -- and your attention to conceptual mapping! -->

# 

## More resources

Any ‘everyday’ ggplot2 extender should also be aware of other invaluable
learning resources (compiled by Teun Van Der Brand):

- The [extending
  ggplot2](https://ggplot2.tidyverse.org/articles/extending-ggplot2.html)
  vignette

- The extending ggplot2 chapters of the [ggplot2
  book](https://ggplot2-book.org/):

  - Chapter 19: [Programming with
    ggplot2](https://ggplot2-book.org/programming.html)
  - Chapter 20: [ggplot2
    internals](https://ggplot2-book.org/internals.html)
  - Chapter 21: [Writing ggplot2
    extensions](https://ggplot2-book.org/extensions.html)
  - Chapter 22: [Case Study:
    Springs](https://ggplot2-book.org/spring1.html)

- The [ggproto](https://stackoverflow.com/questions/tagged/ggproto) tag
  on StackOverflow

- [Extending your ability to extend
  ggplot2](https://www.rstudio.com/resources/rstudioconf-2020/extending-your-ability-to-extend-ggplot2/)
  by Thomas Lin Pederson at rstudio::conf 2020

- [Cracking open ggplot internals with
  {ggtrace}](https://www.rstudio.com/resources/rstudioconf-2020/best-practices-for-programming-with-ggplot2/)
  by June Choe at rstudio::conf 2022

- [Best practises for programming with
  ggplot2](https://www.rstudio.com/resources/rstudioconf-2020/best-practices-for-programming-with-ggplot2/)
  by Dewey Dunnington at rstudio::conf 2020

# g.p.

## Contributors

Especially notably in willingness to have conversations about how to
make Stat extension more accessible is June Choe; he also has been very
open to technical discussion and has played an especially large role in
my fluency in using delayed aesthetic evaluation. Teun van den Brand has
also been helpful and open to discussion about about technical aspects
of particular extension questions.

I’m indebted to the [ggplot2 extenders
meet-up](https://github.com/teunbrand/ggplot-extension-club/blob/main/README.md)
presenters and participants, that have provided a wealth of insight
about extension experiences.

In the future anticipate Denver R-Ladies to be a resource for candid,
person-to-person feedback. We recently
[relaunched](https://www.meetup.com/rladies-denver/events/299879858/)
the group and I anticipate interest in the topic of ggplot2 extension,
and might help host proposed workshops that are part of this proposal.

[Andrew Heiss](https://www.andrewheiss.com/) has promised to help with a
workshop aimed at packaging new ggplot2 extension functionality which is
part of this proposal. Other expert package builders (especially in
ggplot2 extension) will be recruited.

## Consulted

I’m grateful to the ASA Colorado-Wyoming Chapter membership for helpful
feedback at the October 2023 meeting, after giving the talk: [Supporting
a new wave of ggplot2 extenders: New points of entry for ggplot2
super-users](https://bit.ly/ggextend-cowy).

I’ve also grateful to colleagues at West Point Math Department for their
feedback on my talk about creating and using new Stats objects:
[‘Unlocking ggplot2 as a computational engine by extending ggplot2
statistical
geometries’](https://evamaerey.github.io/mytidytuesday/2022-05-09-statistical-geometries/statistical_geometries.html#1)

Furthermore, I’ve gained feedback from participants evaluating a new
tutorial to Stat extension, [easy geom (Stat)
recipes](https://github.com/EvaMaeRey/easy-geom-recipes). A survey and
focus group was used to hear their reactions. In brief, I found that the
recruited ggplot2 super users (regular users with several years of
experience), either hadn’t tried to enter the Stat extension space, or
felt it was quite challenging. But there was a high success rates for
new Stat creation using the new tutorial’s recipes model. [Participant
characteristics and tutorial evaluation can be found
here](https://evamaerey.github.io/easy-geom-recipes/easy_geom_recipes_compute_group.html).
West Point Cadet Morgan Brown assisted in writing the tutorial.

# proposal

ggplot2 is notable among R package, sometimes even sighted as a key
reason for using the R language more broadly. Its elegance and
flexibility, and track-record of being well-maintained makes it a
attractive tool for analysts, journalists, educators and the like.

ggplot2 lets users ‘speak their plots into existence’. Users identify
requisite, orthogonal plot elements, name those elements and ggplot2
produces the described plot. The composition-based nature of ggplot2 is
key to its usability and in turn its popularity.

However, sorely under-utilized are ggplot2 extension mechanisms — and in
particular, the creation and use of new Stats. I believe providing
education for this mechanism that could take productivity and
statistical storytelling with ggplot2 to new heights.

Base ggplot2, of course, makes a lot of Stats available to users. Any
time we use `geom_histogram`, `geom_boxpot`, `geom_smooth`, etc,
mercifully much computation is happens under the hood for users. Compute
is defined in ggproto objects like `StatBin`, `StatBoxplot`,
`StatSmooth` which are used in these functions and computation is done
automatically.

When users create new Stats via extension, they access ggplot2’s
*general* capability as a computation engine. These users realize that
off-loading a computational task to a ggplot2 extension function will
save their future-selves or others from doing painstaking computational
tasks as a prep step. Having designated Stats means that computation is
enabled at the point-of-use: *within* the plot pipeline via a
descriptive function (e.g. geom_point_means() could be defined to plot a
point at the means of x and y), instead of requiring computation before
starting to plot (and in this case the creation of a derivitive
dataset). And that *scope* of the Stat computation can be modified
blazingly fast, via the addition of a group aesthetic or faceting
declaration.

> It may seem surprising, but creating new stats is one of the most
> useful ways to extend the capabilities of ggplot2. – ggplot2: Elegant
> Graphics for Data Analysis

Unfortunately, relatively few ggplot2 users have figured out how to use
this powerful mechanism. The reason for this is likely that dedicated
educational material is quite limited. The topic has been covered by
extension mechanism authors in works like [the ggplot2 extension
vignette](https://cran.r-project.org/web/packages/ggplot2/vignettes/extending-ggplot2.html)
and in [ggplot2: Elegant Graphics for Data Analysis, 3rd
Edition](https://ggplot2-book.org/extensions), but because they are a
small part of a much larger topic. In helpful and notable [extend your
ability to extend
ggplot2](https://www.youtube.com/watch?reload=9&v=uj7A3i2fi54) talk by
Thomas Lin Pederson, it’s time that doesn’t allow for multiple examples
which could help users to start recognizing and differentiating patterns
for new Stat creation. I believe that more focused, sustained attention
is required of educational materials that want to help ggplot2 users get
into Stat creation.

<!-- and because there might be misconception about what is required to enter this space of creating and using new Stats -->

Of particular concern is that barriers to entry and a lack of education
is preventing people that could be be particularly prolific and
efficacious from making contributions in ggplot2 extension. People with
heavy teaching or analytic reporting loads, for example, might not think
they have the time-resources to dedicate to figuring out Stat extension
since educational materials have been relatively sparse. But extension
by such people could be game-changing for their own teaching or analytic
work – and could have further impacts should they share more broadly.

Educator, XXX, who recently attended the ggplot2 extenders meet-up and
who is XXXX specializing in data visualization commented over email
about her work with that uses ggplot2. Quoting her with permission:

> ““.

She further this general prevalence of this inelegance:

> “”

This comment speaks to the need for greater education in ggplot2
extension mechanisms.

I have fleshed out a plan for doing this and preliminary work on this
with emphasis on Stats creation. After hearing XXX reflections, I
decided she might be interested in this new work. Her response, used
with permission, is encouraging.

> ’’

Further development of these resources and broad dissemination is the
goal of this proposal. By supporting this proposal, I think the XXX
grant will help ggplot2 and in turn R shine even brighter!

[^1]: [support a new wave of ggplot2
    extenders](https://bit.ly/ggextend-cowy).
