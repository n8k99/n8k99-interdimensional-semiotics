---
title: "Lee - Introduction to Topological Manifolds"
type: "[[reading-comment]]"
icon: "📖"
domain: "[[The Commons]]"
author: "John M. Lee"
tags: [interdimensional-semiotics]
---




To Pm,
sine qua non

Preface
This book is an introduction to manifolds at the beginning graduate level.
It contains the essential topological ideas that are needed for the further
study of manifolds, particularly in the context of diﬀerential geometry,
algebraic topology, and related ﬁelds. Its guiding philosophy is to develop
these ideas rigorously but economically, with minimal prerequisites and
plenty of geometric intuition. Here at the University of Washington, for
example, this text is used for the ﬁrst third of a year-long course on the
geometry and topology of manifolds; the remaining two-thirds focuses on
smooth manifolds.
There are many superb texts on general and algebraic topology available.
Why add another one to the catalog? The answer lies in my particular
vision of graduate education—it is my (admittedly biased) belief that every
serious student of mathematics needs to know manifolds intimately, in the
same way that most students come to know the integers, the real numbers,
Euclidean spaces, groups, rings, and ﬁelds. Manifolds play a role in nearly
every major branch of mathematics (as I illustrate in Chapter 1), and
specialists in many ﬁelds ﬁnd themselves using concepts and terminology
from topology and manifold theory on a daily basis. Manifolds are thus part
of the basic vocabulary of mathematics, and need to be part of the basic
graduate education. The ﬁrst steps must be topological, and are embodied
in this book; in most cases, they should be complemented by material on
smooth manifolds, vector ﬁelds, diﬀerential forms, and the like. (After all,
few of the really interesting applications of manifold theory are possible
without using tools from calculus.)

viii
Preface
Of course, it is not realistic to expect all graduate students to take full-
year courses in general topology, algebraic topology, and diﬀerential geome-
try. Thus, although this book touches on a generous portion of the material
that is typically included in much longer courses, the coverage is selective
and relatively concise, so that most of the book can be covered in a single
quarter or semester, leaving time in a year-long course for further study in
whatever direction best suits the instructor and the students. At U.W. we
follow it with a two-quarter sequence on smooth manifold theory; but it
could equally well lead into a full-blown course on algebraic topology.
It is easy to describe what this book is not. It is not a course on general
topology—many of the topics that are standard in such a course are ignored
here, such as metrization theorems; inﬁnite products and the Tychonoﬀ
theorem; countability and separation axioms and the relationships among
them (other than second countability and the Hausdorﬀaxiom, which are
part of the deﬁnition of manifolds); and function spaces. Nor is it a course
in algebraic topology—although I treat the fundamental group in detail,
there is barely a mention of the higher [[Homotopy|homotopy]] groups, and the treatment
of homology theory is extremely brief, meant mainly to give the ﬂavor of
the theory and to lay some groundwork for the later introduction of de
Rham cohomology. It is certainly not a comprehensive course on topological
manifolds, which would have to include such topics as PL structures and
maps, transversality, intersection theory, cobordism, bundles, characteristic
classes, and low-dimensional geometric topology. Finally, it is not intended
as a reference book, because few of the results are presented in their most
general or most complete form.
Perhaps the best way to summarize what this book is would be to say
that it represents, to a good approximation, my conception of the ideal
amount of topological knowledge that should be possessed by beginning
graduate students who are planning to go on to study smooth manifolds
and diﬀerential geometry. Experienced mathematicians will probably ob-
serve that my choices of material and approach have been inﬂuenced by the
fact that I am a diﬀerential geometer and analyst by training and predilec-
tion, not a topologist. Thus I give special emphasis to topics that will be
of importance later in the study of smooth manifolds, such as group ac-
tions, orientations, and degree theory. (A few topological ideas that are
important for manifold theory, such as paracompactness and embedding
theorems, are omitted because they are better treated in the context of
smooth manifolds.) But despite my prejudices, I have tried to make the
book useful as a precursor to algebraic topology courses as well, and it
could easily serve as a prerequisite to a more extensive course in homology
and homotopy theory.
Prerequisites. The prerequisite for studying this book is, brieﬂy stated,
a solid undergraduate degree in mathematics; but this probably deserves
some elaboration. Traditionally, “algebraic topology” has been seen as a

Preface
ix
separate subject from “general topology,” and most courses in the former
begin with the assumption that the students have already completed a
course in the latter. However, the sad fact is that for a variety of reasons,
many undergraduate mathematics majors in the U.S. never take a course
in general topology. For that reason I have written this book without as-
suming that the reader has had any exposure to topological spaces. On the
other hand, I do assume several essential prerequisites beyond calculus and
linear algebra: basic logic and set theory such as what one would encounter
in any rigorous undergraduate analysis or algebra course; real analysis at
the level of Rudin’s Principles of Mathematical Analysis [Rud76], includ-
ing, in particular, a thorough understanding of metric spaces and their
continuous functions and compact subsets; and group theory at the level
of Hungerford’s Abstract Algebra: An Introduction [Hun90] or Herstein’s
Topics in Algebra [Her75]. Because it is vitally important that the reader
be comfortable with this prerequisite material, I have collected in the Ap-
pendix a summary of the main points that are used throughout the book,
together with a representative collection of exercises. These exercises, which
should be relatively straightforward for anyone who has had the prerequi-
site courses, can be used by the student to refresh his or her knowledge, or
can be assigned by the instructor at the beginning of the course to make
sure that everyone starts with the same background.
Organization. The book is divided into thirteen chapters, which can be
grouped into an introduction and ﬁve major substantive sections.
The introduction (Chapter 1) is meant to whet the student’s appetite
and create a “big picture” into which the many details can later ﬁt.
The ﬁrst major section, Chapters 2 through 4, is a brief and highly selec-
tive introduction to the ideas of general topology: topological spaces; their
subspaces, products, and quotients; and [[Connectedness|connectedness]] and compactness.
Of course, manifolds are the main examples and are emphasized through-
out. These chapters emphasize the ways in which topological spaces diﬀer
from the more familiar Euclidean and metric spaces, and carefully develop
the machinery that will be needed later, such as quotient maps, local path
connectedness, and locally compact Hausdorﬀspaces.
The second major section, comprising Chapters 5 and 6, explores in de-
tail the main examples that motivate the rest of the theory: simplicial com-
plexes, 1-manifolds, and 2-manifolds. Chapter 5 introduces simplicial com-
plexes in two ways—ﬁrst concretely, as locally ﬁnite collections of simplices
in Euclidean space that intersect nicely; and then abstractly, as collections
of ﬁnite vertex sets. Both approaches are useful: The concrete deﬁnition
helps students develop their geometric intuition, while the abstract point
of view emphasizes the fact that all statements about simplicial complexes
can be reduced to combinatorics. There are several reasons for introducing
simplicial complexes at this stage: They furnish a rich source of examples;
they give a very concrete way of thinking about orientations and the Euler

x
Preface
characteristic; they provide the concept of triangulability needed for the
classiﬁcations of 1-manifolds and 2-manifolds; and they set the stage for
the treatment of homology later. Chapter 6 begins by proving a classiﬁca-
tion theorem for 1-manifolds using the triangulability theorem proved in
the preceding chapter. The rest of the chapter is devoted to a detailed study
of 2-manifolds. After exploring the basic examples of surfaces—the sphere,
the torus, the projective plane, and their connected sums—I give a com-
plete proof of the classiﬁcation theorem for compact surfaces, essentially
following the treatment in [Mas89].
The third major section, Chapters 7 through 10, is the core of the book.
In it, I give a fairly complete and traditional treatment of the fundamental
group. Chapter 7 introduces the deﬁnitions and proves the topological and
homotopy invariance of the fundamental group. At the end of the chapter
I insert a brief introduction to category theory. Categories are not used in
a central way anywhere in the book, but it is natural to introduce them
after having proved the topological invariance of the fundamental group,
and it is useful for students to begin thinking in categorical terms early.
Chapter 8 gives a detailed proof that the fundamental group of the circle
is inﬁnite cyclic. Because the techniques used here are the precursor and
motivation for the entire theory of covering spaces, I introduce some of
the terminology of the latter subject—evenly covered neighborhoods, local
sections, lifting—in the special case of the circle, and the proofs here form
a model for the proofs of more general theorems involving covering spaces
to come in a later chapter. Chapter 9 is a brief digression into group theory.
Although a basic acquaintance with group theory is an essential prerequi-
site, most undergraduate algebra courses do not treat free products, free
groups, presentations of groups, or free abelian groups, so I develop these
subjects from scratch. (The material on free abelian groups is included pri-
marily for use in the treatment of homology in Chapter 13, but some of the
results play a role also in classifying the coverings of the torus in Chapter
12.) The last chapter of this section gives the statement and proof of the
Seifert–Van Kampen theorem, which expresses the fundamental group of a
space in terms of the fundamental groups of its subsets, and describes sev-
eral applications of the theorem including computation of the fundamental
groups of graphs and of all the compact surfaces.
The fourth major section consists of two chapters on covering spaces.
Chapter 11 deﬁnes covering spaces, gives a few examples, and develops the
theory of the covering group. Much of the development goes rapidly here,
because it is parallel to what was done earlier in the concrete case of the cir-
cle. The ostensible goal of Chapter 12 is to prove the classiﬁcation theorem
for coverings—that there is a one-to-one correspondence between isomor-
phism classes of coverings of X and conjugacy classes of subgroups of the
fundamental group of X—but along the way two other ideas are developed
that are of central importance in their own right. The ﬁrst is the notion of
the universal covering space, together with proofs that every manifold has a

Preface
xi
universal covering and that the universal covering space covers every other
covering space. The second is the fact that the quotient of a manifold by
a free, proper action of a discrete group yields a manifold. These ideas are
applied to a number of important examples, including classifying coverings
of the torus and the lens spaces, and proving that surfaces of higher genus
are covered by the hyperbolic disk.
The ﬁfth major section of the book consists of one chapter only, Chap-
ter 13, on homology theory. In order to cover some of the most important
applications of homology to manifolds in a reasonable time, I have chosen
a “low-tech” approach to the subject. I focus mainly on singular homology
because it is the most straightforward generalization of the fundamental
group. After deﬁning the homology groups, I prove a few essential proper-
ties, including homotopy invariance and the Mayer–Vietoris theorem, with
a minimum of homological machinery. I could not resist including a (terri-
bly brief) introduction to simplicial homology, just because it immediately
yields the topological invariance of the Euler characteristic. The last sec-
tion of the chapter is a brief introduction to cohomology, mainly with ﬁeld
coeﬃcients, to serve as background for a treatment of de Rham theory in
a later course. In keeping with the overall philosophy of focusing only on
what is necessary for a basic understanding of manifolds, I do not even
mention relative homology, homology with arbitrary coeﬃcients, simplicial
approximation, or the axioms for a homology theory.
Although this book grew out of notes designed for a one-quarter graduate
course, there is clearly too much material here to cover adequately in ten
weeks. It should be possible to cover all or most of it in a semester with
well prepared students. The book could even be used for a full-year course,
allowing the instructor to adopt a much more leisurely pace and to work
out some of the problems as examples in class.
Each instructor will have his or her own ideas about what to leave out
in order to ﬁt the material into a short course. At the University of Wash-
ington, we typically do not cover the chapter on homology at all, and give
short shrift to some of the simplicial theory and some of the more involved
examples of covering maps. Others may wish to leave out some or all of
the material on covering spaces, or the classiﬁcation of surfaces. With stu-
dents who have had a solid topology course, the ﬁrst four chapters could
be skipped or assigned as outside reading.
Exercises and Problems. As is the case with any new mathematical mate-
rial, and perhaps even more than usual with material like this that is so
diﬀerent from the mathematics most students have seen as undergraduates,
it is impossible to learn the subject without getting one’s hands dirty and
working out a large number of examples and problems. I have tried to give
the reader ample opportunity to do so throughout the book. In every chap-
ter, and especially in the early ones, there are “exercises” woven into the
text. Do not ignore them; without their solutions, the text is incomplete.

xii
Preface
The reader should take each exercise as a signal to stop reading, pull out a
pencil and paper, and work out the answer before proceeding further. The
exercises are usually relatively easy, and typically involve proving minor
results or working out examples that are essential to the ﬂow of the expo-
sition. Some require techniques that the student probably already knows
from prior courses; others ask the student to practice techniques or apply
results that have recently been introduced in the text. A few are straight-
forward but rather long arguments that are more enlightening to work
through on one’s own than to read. In the later chapters, fewer things are
singled out as exercises, but there are still plenty of omitted details in the
text that the student should work out before going on; it is my hope that
by the time the student reaches the last few chapters he or she will have
developed the habit of stopping and working through most of the details
that are not spelled out without having to be told.
At the end of each chapter is a selection of “problems.” These are, with
a few exceptions, harder and/or longer than the exercises, and give the
student a chance to grapple with more signiﬁcant issues. The results of a
number of the problems are used later in the text. There are more problems
than most students could do in a quarter or a semester, so the instructor will
want to decide which ones are most germane and assign those as homework.
Acknowledgments. Those of my colleagues at the University of Washington
with whom I have discussed this material—Tom Duchamp, Judith Arms,
Steve Mitchell, Scott Osborne, and Ethan Devinatz—have provided invalu-
able help in sorting out what should go into this book and how it should
be presented. Each has had a strong inﬂuence on the way the book has
come out, for which I am deeply grateful. (On the other hand, it is likely
that none of them would wholeheartedly endorse all my choices regarding
which topics to treat and how to treat them, so they are not to be blamed
for any awkwardnesses that remain.) I would like to thank Ethan Devinatz
in particular for having had the courage to use the book as a course text
when it was still in an inchoate state, and for having the grace and patience
to wait while I prepared chapters at the last minute for his course.
Thanks are due also to Mary Sheetz, who did an excellent job producing
some of the illustrations under the pressures of time and a ﬁnicky author.
My debt to the authors of several other textbooks will be obvious to
anyone who knows those books: William Massey’s Algebraic Topology:
An Introduction [Mas89], Allan Sieradski’s An Introduction to Topology
and [[Homotopy]] [Sie92], Glen Bredon’s Topology and Geometry, and James
Munkres’s Topology: A First Course [Mun75] and Elements of Algebraic
Topology [Mun84] are foremost among them.
Finally, I would like to thank my wife, Pm, for her forbearance and
unﬂagging support while I was spending far too much time with this book

Preface
xiii
and far too little with the family; without her help I unquestionably could
not have done it.
John M. Lee
Seattle

Contents
Preface
vii
1
Introduction
1
What Are Manifolds?
. . . . . . . . . . . . . . . . . . . . . . . .
1
Why Study Manifolds? . . . . . . . . . . . . . . . . . . . . . . . .
4
2
Topological Spaces
17
Topologies . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
17
Bases
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
27
Manifolds . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
30
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
36
3
New Spaces from Old
39
Subspaces . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
39
Product Spaces . . . . . . . . . . . . . . . . . . . . . . . . . . . .
48
Quotient Spaces
. . . . . . . . . . . . . . . . . . . . . . . . . . .
52
Group Actions
. . . . . . . . . . . . . . . . . . . . . . . . . . . .
58
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
62
4
[[Connectedness]] and Compactness
65
[[Connectedness]]
. . . . . . . . . . . . . . . . . . . . . . . . . . . .
65
Compactness . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
73
Locally Compact HausdorﬀSpaces . . . . . . . . . . . . . . . . .
81
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
88

xvi
Contents
5
Simplicial Complexes
91
Euclidean Simplicial Complexes . . . . . . . . . . . . . . . . . . .
92
Abstract Simplicial Complexes
. . . . . . . . . . . . . . . . . . .
96
Triangulation Theorems . . . . . . . . . . . . . . . . . . . . . . .
102
Orientations . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
105
Combinatorial Invariants . . . . . . . . . . . . . . . . . . . . . . .
109
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
114
6
Curves and Surfaces
117
Classiﬁcation of Curves
. . . . . . . . . . . . . . . . . . . . . . .
118
Surfaces . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
119
Connected Sums
. . . . . . . . . . . . . . . . . . . . . . . . . . .
126
Polygonal Presentations of Surfaces . . . . . . . . . . . . . . . . .
129
Classiﬁcation of Surface Presentations . . . . . . . . . . . . . . .
137
Combinatorial Invariants . . . . . . . . . . . . . . . . . . . . . . .
142
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
146
7
[[Homotopy]] and the Fundamental Group
147
[[Homotopy]] . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
148
The Fundamental Group . . . . . . . . . . . . . . . . . . . . . . .
150
Homomorphisms Induced by Continuous Maps
. . . . . . . . . .
158
[[Homotopy]] Equivalence . . . . . . . . . . . . . . . . . . . . . . . .
161
Higher [[Homotopy]] Groups . . . . . . . . . . . . . . . . . . . . . .
169
Categories and Functors . . . . . . . . . . . . . . . . . . . . . . .
170
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
176
8
Circles and Spheres
179
The Fundamental Group of the Circle . . . . . . . . . . . . . . .
180
Proofs of the Lifting Lemmas . . . . . . . . . . . . . . . . . . . .
183
Fundamental Groups of Spheres . . . . . . . . . . . . . . . . . . .
187
Fundamental Groups of Product Spaces . . . . . . . . . . . . . .
188
Fundamental Groups of Manifolds
. . . . . . . . . . . . . . . . .
189
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
191
9
Some Group Theory
193
Free Products . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
193
Free Groups . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
199
Presentations of Groups . . . . . . . . . . . . . . . . . . . . . . .
201
Free Abelian Groups . . . . . . . . . . . . . . . . . . . . . . . . .
203
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
208
10 The Seifert–Van Kampen Theorem
209
Statement of the Theorem . . . . . . . . . . . . . . . . . . . . . .
210
Applications . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
212
Proof of the Theorem
. . . . . . . . . . . . . . . . . . . . . . . .
221

Contents
xvii
Distinguishing Manifolds . . . . . . . . . . . . . . . . . . . . . . .
227
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
230
11 Covering Spaces
233
Deﬁnitions and Basic Properties
. . . . . . . . . . . . . . . . . .
234
Covering Maps and the Fundamental Group . . . . . . . . . . . .
239
The Covering Group . . . . . . . . . . . . . . . . . . . . . . . . .
247
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
253
12 Classiﬁcation of Coverings
257
Covering Homomorphisms . . . . . . . . . . . . . . . . . . . . . .
258
The Universal Covering Space . . . . . . . . . . . . . . . . . . . .
261
Proper Group Actions . . . . . . . . . . . . . . . . . . . . . . . .
266
The Classiﬁcation Theorem . . . . . . . . . . . . . . . . . . . . .
283
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
289
13 Homology
291
Singular Homology Groups
. . . . . . . . . . . . . . . . . . . . .
292
[[Homotopy]] Invariance . . . . . . . . . . . . . . . . . . . . . . . . .
300
Homology and the Fundamental Group
. . . . . . . . . . . . . .
304
The Mayer–Vietoris Theorem . . . . . . . . . . . . . . . . . . . .
308
Applications . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
318
The Homology of a Simplicial Complex
. . . . . . . . . . . . . .
323
Cohomology . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
329
Problems
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
334
Appendix: Review of Prerequisites
337
Set Theory
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
337
Metric Spaces . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
347
Group Theory . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
352
References
359
Index
362

1
Introduction
A course on manifolds diﬀers from most other introductory graduate math-
ematics courses in that the subject matter is often completely unfamiliar.
Most beginning graduate students have had undergraduate courses in alge-
bra and analysis, so that graduate courses in those areas are continuations
of subjects they have already begun to study. But it is possible to get
through an entire undergraduate mathematics education, at least in the
United States, without ever hearing the word “manifold.”
One reason for this anomaly is that even the deﬁnition of manifolds in-
volves rather a large number of technical details—for example, in this book
the formal deﬁnition will not come until the end of Chapter 2. Since it is
disconcerting to embark on such an adventure without even knowing what
it is about, we devote this introductory chapter to a nonrigorous deﬁnition
of manifolds, an informal exploration of some examples, and a consideration
of where and why they arise in various branches of mathematics.
What Are Manifolds?
Let us begin by describing informally how one should think about mani-
folds. The underlying idea is that manifolds are like curves and surfaces,
except, perhaps, that they might be of higher dimension. Every manifold
has a dimension, which is, roughly speaking, the number of independent
numbers (or “parameters”) needed to specify a point. The prototype of

2
1. Introduction
FIGURE 1.1. Plane curves.
FIGURE 1.2. Space curve.
an n-dimensional manifold is n-dimensional Euclidean space Rn, in which
each point is an n-tuple of real numbers.
An n-dimensional manifold is an object modeled locally on Rn; this means
that it takes exactly n numbers to specify a point, at least if we do not
stray too far from a given starting point. A physicist would say that an
n-dimensional manifold is an object with n “degrees of freedom.”
Manifolds of dimension 1 are commonly called curves (although they
need not be “curved” in the ordinary sense of the word). The simplest
example is the real line; other examples are provided by familiar plane
curves such as circles, parabolas, or the graph of any continuous function of
the form y = f(x) (Figure 1.1). Still other familiar 1-dimensional manifolds
are space curves, which are often described parametrically by equations
such as (x, y, z) = (f(t), g(t), h(t)) for some continuous functions f, g, h
(Figure 1.2).
In each of these examples, a point on the curve can be unambiguously
speciﬁed by a single real number. For example, a point on the real line is
a real number. We might specify a point on the circle by its angle, a point
on a graph by its x coordinate, and a point on a parametrized curve by
its parameter t. Note that although a parameter value determines a point,
diﬀerent parameter values may correspond to the same point, as in the
case of angles on the circle. But in every case, as long as we stay close
to some initial point, there is a one-to-one correspondence between nearby
real numbers and nearby points on the curve.

What Are Manifolds?
3
FIGURE 1.3. Doughnut surface.
Manifolds of dimension 2 are surfaces. The two most common exam-
ples are planes and spheres. (When mathematicians speak of a sphere, we
invariably mean a spherical surface, which is 2-dimensional, not a solid
ball, which is 3-dimensional.) Other familiar surfaces include cylinders, el-
lipsoids, paraboloids, and the doughnut-shaped surface in R3 obtained by
revolving a circle around the z-axis (Figure 1.3). (This doughnut-shaped
surface is often called a torus, but we will reserve that name for a slightly
diﬀerent but closely related object, to be introduced in the next chapter.)
In these cases two coordinates are needed to determine a point. For ex-
ample, on the plane we typically use Cartesian or polar coordinates; on the
sphere we might use latitude and longitude; while on the doughnut surface
we might use two angles. As in the 1-dimensional case, the correspondence
between points and pairs of numbers is in general only local.
The only higher-dimensional manifold that we can visualize is Euclidean
3-space. But it is not hard to construct subsets of higher-dimensional Eu-
clidean spaces that might reasonably be called manifolds. First, any open
subset of Rn is an n-manifold for obvious reasons. More interesting ex-
amples are obtained by using one or more equations to “cut out” lower-
dimensional subsets. For example, the set of points (x1, x2, x3, x4) in R4
satisfying the equation
(x1)2 + (x2)2 + (x3)2 + (x4)2 = 1
(1.1)
is called the (unit) 3-sphere. It is a 3-dimensional manifold because in
a neighborhood of any given point it takes exactly three coordinates to
specify a nearby point: Starting at, say, the “north pole” (0, 0, 0, 1), we
can solve equation (1.1) for x4, and then each nearby point is uniquely
determined by choosing appropriate (small) (x1, x2, x3) coordinates and
setting x4 = (1−(x1)2 −(x2)2 −(x3)2)1/2. Near other points, we may need
to solve for diﬀerent variables; but in each case three coordinates suﬃce.

4
1. Introduction
The key feature of these examples is that an n-dimensional manifold
“looks like” Rn locally. To make sense of the intuitive notion of “looks
like,” we will say that two subsets of Euclidean spaces U ⊂Rk, V ⊂Rn
are topologically equivalent or homeomorphic (Greek for “same form”) if
there exists a one-to-one correspondence ϕ: U →V such that both ϕ and
its inverse are continuous maps. (Such a correspondence is called a home-
omorphism.) A subset M of some Euclidean space Rk is locally Euclidean
of dimension n if every point of M has a neighborhood in M that is topo-
logically equivalent to a ball in Rn.
Now we can give a preliminary deﬁnition of manifolds. An n-dimensional
manifold (n-manifold for short) is a subset of some Euclidean space Rk that
is locally Euclidean of dimension n. Later, after we have developed more
machinery, we will give a considerably more general deﬁnition; but this one
will get us started.
Why Study Manifolds?
What follows is an incomplete survey of some of the ﬁelds of mathematics
in which manifolds play an important role.
Topology
Roughly speaking, topology is the branch of mathematics that is concerned
with properties of sets that are unchanged by “continuous deformations.”
More accurately, a topological property is one that is preserved by home-
omorphisms.
The subject in its modern form was invented a century ago by the French
mathematician Henri Poincar´e, as an outgrowth of his attempts to classify
geometric objects that appear in analysis. In a seminal 1895 paper titled
Analysis Situs (the old name for topology, Latin for “analysis of position”)
and a series of companion papers in 1899–1905, Poincar´e laid out the main
problems of topology and introduced an astonishing array of new ideas for
solving them. As you read this book, you will see that his name is written all
over the subject. In the intervening century, topology has taken on the role
of providing the foundations for just about every branch of mathematics
that has any use for a concept of “space.” (An excellent historical account
of the ﬁrst six decades of the subject can be found in [Die89].)
Here is a simple but telling example of the kind of problem that topology
was invented to solve. Consider two surfaces in space: a sphere and a cube.
It should not be hard to convince yourself that the cube can be continuously
deformed into the sphere without tearing or collapsing it. It is not much
harder to come up with an explicit formula for a [[Homeomorphism|homeomorphism]] between
them (we will do so in Chapter 2). Similarly, with a little more work, you

Why Study Manifolds?
5
FIGURE 1.4. Deforming a doughnut into a coﬀee cup.
should be able to see how a doughnut surface can be continuously deformed
into the surface of a one-handled coﬀee cup, by stretching out one-half of
the doughnut to become the cup, and shrinking the other half to become
the handle (Figure 1.4). Once you decide on an explicit set of equations to
deﬁne a “coﬀee-cup surface” in R3, you could in principle come up with a
set of formulas to describe a homeomorphism between it and the doughnut
surface. On the other hand, a little reﬂection will probably convince you
that there is no homeomorphism from the sphere to the doughnut surface:
Any such map would have to tear open a “hole” in the sphere, and thus
could not be continuous.
It is usually relatively straightforward (though not always easy!) to prove
that two manifolds are topologically equivalent once you have convinced
yourself intuitively that they are: Just write down an explicit homeomor-
phism between them. What is much harder is to prove that two manifolds
are not homeomorphic—even when it seems “obvious” that they are not
as in the case of the sphere and the doughnut—because you would need to
show that no one, no matter how clever, could ﬁnd such a map.
History abounds with examples of operations that mathematicians long
believed to be impossible, only to be proved wrong. Here is an example from
topology. Imagine a spherical surface colored white on the outside and gray
on the inside, and imagine that it can move freely in space, including passing
freely through itself. Under these conditions you could turn the sphere
inside out by continuously deforming it, so that the gray side ends up facing
out, but it seems obvious that in so doing you would have to introduce a
crease somewhere. (There are precise mathematical deﬁnitions of the terms
“continuously deforming” and “creases,” but you do not need to know them
to get the general idea.) The simplest way to proceed would be to push
the northern hemisphere down and the southern hemisphere up, allowing
them to pass through each other, until the two hemispheres had switched
places (Figure 1.5); but this would introduce a crease along the equator.
The topologist Stephen Smale stunned the mathematical community in
1958 [Sma58] when he proved it was possible to turn the sphere inside out
without introducing any creases. Several ways to do this are beautifully
illustrated in video recordings [Max77, LMM94, SFL98].

6
1. Introduction
FIGURE 1.5. Turning a sphere inside out (with a crease).
The usual way to prove that two manifolds are not topologically equiv-
alent is by ﬁnding [[Topological Invariant|topological invariants]]: properties (which could be num-
bers or other mathematical objects such as groups, matrices, polynomials,
or vector spaces) that are preserved by homeomorphisms. If two manifolds
have diﬀerent invariants, they cannot be homeomorphic.
It is evident from the examples above that geometric properties such as
circumference and area are not topological invariants, because they are not
generally preserved by homeomorphisms. Intuitively, the property that dis-
tinguishes the sphere from the doughnut surface is the fact that the latter
has a “hole,” while the former does not. But it turns out that giving a
precise deﬁnition of what is meant by a hole takes rather a lot of work.
One invariant that is commonly used to count holes in a manifold is called
the fundamental group of the manifold, which is a group (in the algebraic
sense) attached to each manifold in such a way that homeomorphic man-
ifolds have isomorphic groups. Then the “size” of the fundamental group
is a measure of the number of holes possessed by the manifold. The study
of the fundamental group will occupy a major portion of this book. It is
the starting point for algebraic topology, which is the subject that studies
topological properties of manifolds (or other geometric objects) by attach-
ing algebraic structures such as groups and rings to them in a topologically
invariant way.
One of the most important problems of topology is the problem of clas-
sifying manifolds. Ideally, one would like to produce a list of n-dimensional
manifolds, and a theorem that says every n-dimensional manifold is home-
omorphic to exactly one on the list, together with a list of computable
topological invariants that could be used to decide where on the list any
given manifold belongs. Precisely such a theorem is known for surfaces:
It says that every compact surface is homeomorphic to a sphere, or to a
doughnut surface with a ﬁnite number of holes, or to a connected sum of
projective planes. (We will deﬁne these terms and prove the theorem in
Chapter 6.)
For higher-dimensional manifolds, the situation is much more compli-
cated. For example, Poincar´e conjectured around 1900 that any compact 3-

Why Study Manifolds?
7
manifold whose fundamental group is the trivial (one-element) group must
be homeomorphic to the 3-sphere. For a long time, topologists thought of
this as the simplest ﬁrst step in a potential classiﬁcation of 3-manifolds.
But although analogous conjectures have been made for higher-dimensional
manifolds and were proved in the intervening years (for 5-manifolds and
higher by Stephen Smale in 1961 [Sma61], and for 4-manifolds by Michael
Freedman in 1982 [Fre82]), the original Poincar´e conjecture remains as of
this writing a preeminent unsolved problem in topology. The best hope for
a classiﬁcation of 3-manifolds is the geometrization conjecture made in the
1970s by William Thurston (see [Sco83, Thu97] for an explanation), which
says, roughly, that every compact 3-manifold can be cut into ﬁnitely many
pieces each of which admits one of eight (mostly non-Euclidean) geometric
structures. Since the manifolds with geometric structures are much better
understood, a proof of this conjecture would go a long way toward provid-
ing a complete classiﬁcation of 3-manifolds; in particular, it would imply
that the Poincar´e conjecture is true.
In dimensions 4 and higher, on the other hand, there is no hope for a com-
plete classiﬁcation: It was proved in 1958 by A. A. Markov that there is no
algorithm for classifying manifolds of dimension greater than 3 (see [Sti93]).
Nonetheless, there is much that can be said using sophisticated combina-
tions of techniques from algebraic topology, diﬀerential geometry, partial
diﬀerential equations, and algebraic geometry, and spectacular progress was
made in the last half of the twentieth century in understanding the vari-
ety of manifolds that exist. The topology of 4-manifolds, in particular, is
currently a highly active ﬁeld of research.
Geometry
The principal objects of study in Euclidean plane geometry, as you encoun-
tered it in secondary school, are ﬁgures constructed from portions of lines,
circles, and other curves—in other words, 1-manifolds. Similarly, solid ge-
ometry is concerned with ﬁgures made from portions of planes, spheres,
and other 2-manifolds. The properties that are of interest are those that
are invariant under rigid motions. These include simple properties such as
lengths, angles, areas, and volumes, as well as more sophisticated properties
derived from them such as curvature. The curvature of a curve or surface is
a quantitative measure of how it bends and in what directions; for example,
a positively curved surface is “bowl-shaped,” while a negatively curved one
is “saddle-shaped.”
Geometric theorems involving curves and surfaces range from the trivial
to the very deep. A typical theorem you have undoubtedly seen before is the
angle-sum theorem: The sum of the interior angles of any Euclidean triangle
is π radians. This seemingly trivial result has profound generalizations to
the study of curved surfaces, where angles may add up to more or less than
π depending on the curvature of the surface. The high point of surface

8
1. Introduction
theory is the Gauss–Bonnet theorem: For a closed, bounded surface in R3,
this theorem expresses the relationship between the total curvature (i.e., the
integral of curvature with respect to area) and the number of holes it has.
If the surface is topologically equivalent to an n-holed doughnut surface,
the theorem says that the total curvature is exactly equal to 4π −4πn.
In the case n = 1 this implies that no matter how a one-holed doughnut
surface is bent or stretched, the regions of positive and negative curvature
will always precisely cancel each other out so that the total curvature is
zero.
The introduction of manifolds has allowed the study of geometry to be
carried into higher dimensions. The appropriate setting for studying geo-
metric properties in arbitrary dimensions is that of Riemannian manifolds,
which are manifolds on which there is a rule for measuring distances and
angles, subject to certain natural restrictions to ensure that these quantities
behave analogously to their Euclidean counterparts. The properties of in-
terest are those that are invariant under isometries, or distance-preserving
transformations. For example, one can study the relationship between the
curvature of an n-dimensional Riemannian manifold (a local property) and
its global topological type. A typical theorem is that a complete Riemann-
ian n-manifold whose curvature is everywhere larger than some ﬁxed posi-
tive number must be compact and have a ﬁnite fundamental group (not too
many holes). The search for such relationships is one of the principal ac-
tivities in Riemannian geometry, a thriving ﬁeld of contemporary research.
See Chapter 1 of [Lee97] for an informal introduction to the subject.
Complex Analysis
Complex analysis is the study of holomorphic (i.e., complex analytic) func-
tions. Some such functions are naturally “multiple-valued.” A typical ex-
ample is the complex square root. Except for zero, every complex number
has two distinct square roots. But unlike the case of positive real numbers,
where we can always unambiguously choose the positive square root to
denote by the symbol √x, it is not possible to deﬁne a global continuous
square root function on the complex plane. To see why, write z in polar
coordinates as z = reiθ. Then the two square roots of z can be written
√r eiθ/2 and √r ei(θ/2+π). As θ increases from 0 to 2π, the ﬁrst square root
goes from the positive real axis through the upper half-plane to the neg-
ative real axis, while the second goes from the negative real axis through
the lower half-plane to the positive real axis. Thus whichever continuous
square root function we start with on the positive real axis, we are forced
to choose the other after having made one circuit around the origin.
Even though a “two-valued function” is properly considered as a relation
and not really a function at all, we can deﬁne the graph of such a relation
in an unambiguous way. To warm up with a simpler example, consider the
two-valued square root “function” on the nonnegative real axis. Its graph

Why Study Manifolds?
9
u
x
u2 = x
FIGURE 1.6. Graph of the two branches of the real square root.
is deﬁned to be the set of pairs (x, u) ∈R × R such that u = ±√x, or
equivalently u2 = x. This is a parabola opening in the positive x direction
(Figure 1.6), which we can think of as the two “branches” of the square
root.
Similarly, the graph of the two-valued complex square root “function”
is the set of pairs (z, w) ∈C × C such that w2 = z. Over each small disk
U ⊂C that does not contain 0, this graph has two branches or “sheets,”
corresponding to the two possible continuous choices of square root function
on U (Figure 1.7). If you start on one sheet above the positive real axis
and pass once around the origin in the counterclockwise direction, you end
up on the other sheet. Going around once more brings you back to the ﬁrst
sheet.
It turns out that this graph in C2 is a 2-dimensional manifold, of a special
type called a [[Riemann Surface]]—this is essentially a 2-manifold on which
there is some way to deﬁne holomorphic functions. Riemann surfaces are
of great importance in complex analysis, since any holomorphic function
gives rise to a Riemann surface by a procedure analogous to the one we
sketched above. The surface we constructed turns out to be topologically
equivalent to a plane, but more complicated functions can give rise to
more complicated surfaces. For example, the two-valued “function” f(z) =
±
√
z3 −z yields a Riemann surface that is homeomorphic to a plane with
one “handle” attached.
One of the fundamental tasks of complex analysis is to understand the
topological type (number of “holes” or “handles”) of the Riemann surface

10
1. Introduction
w = √reiθ/2
w
x
y
U
w = √rei(θ/2+π)
FIGURE 1.7. Two branches of the complex square root.
of a given function, and how it relates to the analytic properties of the
function.
Algebra
One of the most important objects studied in abstract algebra is the general
linear group GL(n, R), which is the group of n × n invertible real matrices.
As a set, it can be identiﬁed with a subset of n2-dimensional Euclidean
space, simply by stringing all the matrix entries out in a row. Since a
matrix is invertible if and only if its determinant is nonzero, GL(n, R) is an
open subset of Rn2, and is therefore an n2-dimensional manifold. Similarly,
the complex general linear group GL(n, C) is the group of n × n invertible
complex matrices; it is a 2n2-manifold, because we can identify Cn2 with
R2n2.
A Lie group is a group (in the algebraic sense) that is also a manifold,
together with some technical conditions to ensure that the group structure
and the manifold structure are compatible with each other. They play a
central role in diﬀerential geometry, representation theory, and mathemat-
ical physics, among many other ﬁelds. The most important Lie groups are
subgroups of the real and complex general linear groups. Some commonly

Why Study Manifolds?
11
FIGURE 1.8. A plane curve with disconnected pieces.
encountered examples are the special linear group SL(n, R) ⊂GL(n, R),
consisting of matrices with determinant 1; the orthogonal group O(n) ⊂
GL(n, R), consisting of matrices whose columns are orthonormal; the special
orthogonal group SO(n) = O(n) ∩SL(n, R); and their complex analogues,
the complex special linear group SL(n, C) ⊂GL(n, C), the unitary group
U(n) ⊂GL(n, C), and the special unitary group SU(n) = U(n) ∩SL(n, C).
It is important to understand the topological structure of a Lie group and
how its topological structure relates to its algebraic structure. For example,
it can be shown that SO(2) is topologically equivalent to a circle, SU(2)
is topologically equivalent to the 3-sphere, and any connected abelian Lie
group is topologically equivalent to a Cartesian product of circles and lines.
Lie groups provide a rich source of examples of manifolds in all dimensions.
Algebraic Geometry
Algebraic geometers study the geometric properties of solution sets to sys-
tems of polynomial equations. Many of the basic questions of algebraic
geometry can be posed very naturally in the elementary context of plane
curves deﬁned by polynomial equations. For example: How many intersec-
tion points can one expect between two plane curves deﬁned by polyno-
mials of degrees k and l? (Not more than kl, but sometimes fewer.) How
many disconnected “pieces” does the solution set to a particular polyno-
mial equation have (Figure 1.8)? Does a plane curve have any self crossings
(Figure 1.9) or “cusps” (points where the tangent vector does not vary
continuously—Figure 1.10)?
But the real power of algebraic geometry becomes evident only when one
focuses on polynomials with coeﬃcients in an algebraically closed ﬁeld (one
in which every polynomial decomposes into a product of linear factors),
since polynomial equations always have the expected number of solutions
(counted with multiplicity) in that case. The most deeply studied case is
the complex ﬁeld; in this context the solution set to a system of complex

12
1. Introduction
FIGURE 1.9. A self crossing.
FIGURE 1.10. A cusp.
polynomials in n variables is a certain geometric object in Cn called an
algebraic variety, which (except for a small subset where there might be
self crossings, cusps, or more complicated kinds of behavior) is a manifold.
The subject becomes even more interesting if one enlarges Cn by adding
“ideal points at inﬁnity” where parallel lines or asymptotic curves can be
thought of as meeting; the resulting space is called complex projective space,
and is an extremely important manifold in its own right.
The properties of interest are those that are invariant under projective
transformations (the natural changes of coordinates on projective space).
One can ask such questions as these: Is a given variety a manifold or does
it have singular points (points where it fails to be a manifold)? If it is
a manifold, what is its topological type? If it is not a manifold, what is
the geometric structure of its singular set, and how does that set change
when one varies the coeﬃcients of the polynomials slightly? If two varieties
are homeomorphic, are they equivalent under a projective transformation?
How many times and in what way do two or more varieties intersect?
Algebraic geometry has contributed a prodigious supply of examples of
manifolds. In particular, much of the recent progress in understanding 4-
dimensional manifolds has been driven by the wealth of examples that arise
as algebraic varieties.
Classical Mechanics
Classical mechanics is the study of systems that obey Newton’s laws of
motion. The positions of all the objects in the system at any given time
can be described by a set of numbers, or coordinates; typically, these are
not independent of each other but instead must satisfy some relations.
The relations can usually be interpreted as deﬁning a manifold in some
Euclidean space.

Why Study Manifolds?
13
dP Q
Q
R
θ
P
FIGURE 1.11. A rigid body in space.
For example, consider a rigid body moving through space under the
inﬂuence of gravity. If we choose three noncollinear points P, Q, and R on
the body (Figure 1.11), the position of the body is completely speciﬁed once
we know the coordinates of these three points, which correspond to a point
in R9. However, the positions of the three points cannot all be speciﬁed
arbitrarily: Because the body is rigid, they are subject to the constraint
that the distances between pairs of points are ﬁxed. Thus, to determine
the position of the body, we can arbitrarily specify the coordinates of P
in space (three parameters), and then we can specify the position of Q
by giving, say, its latitude and longitude on the sphere of radius dP Q, the
ﬁxed distance between P and Q (two more parameters). Finally, having
determined the position of the two points P and Q, the only remaining
freedom is to rotate R around the line PQ; so we can specify the position
of R by giving the angle θ that the plane PQR makes with some reference
plane (one more parameter). Thus the set of possible positions of the body
is a certain 6-dimensional manifold M ⊂R9.
Newton’s second law of motion expresses the acceleration of the object—
that is, the second derivatives of the coordinates of P, Q, R—in terms of
the force of gravity, which is a certain function of the object’s position.
This can be interpreted as a system of second-order ordinary diﬀerential
equations for the position coordinates, whose solutions are all the possible
paths the rigid body can take on the manifold M.
The study of classical mechanics can thus be interpreted as the study of
ordinary diﬀerential equations on manifolds, also known as smooth dynam-
ical systems. A wealth of interesting questions arise in this subject: How

14
1. Introduction
do solutions behave over the long term? Are there any equilibrium points
or periodic trajectories? If so, are they stable, that is, do nearby trajecto-
ries stay nearby? A good understanding of manifolds is necessary to fully
answer these questions.
General Relativity
Manifolds play a decisive role in Einstein’s general theory of relativity,
which describes the interactions among matter, energy, and gravitational
forces. The central assertion of the theory is that spacetime (the collec-
tion of all points in space at all times in history) can be modeled by a
4-dimensional manifold that carries a certain kind of geometric structure
called a Lorentz metric; and this metric satisﬁes a system of partial diﬀer-
ential equations called the Einstein ﬁeld equations. Gravitational eﬀects are
then interpreted as manifestations of the curvature of the Lorentz metric.
In order to describe the global structure of the universe, its history, and
its possible futures, it is important to understand ﬁrst of all what kinds
of 4-manifolds exist and what kinds of Lorentz metrics they can carry.
There are especially interesting relationships between the local geometry
of spacetime (as reﬂected in the local distribution of matter and energy)
and the global topological structure of the universe; these relationships
are similar to those described above for Riemannian manifolds, but are
more complicated because of the introduction of forces and motion into the
picture. In particular, if we assume that on a cosmic scale the universe looks
approximately the same at all points and in all directions (such a spacetime
is said to be homogeneous and isotropic), then it turns out there is a critical
value for the average density of matter and energy in the universe: Above
this density, the universe closes up on itself spatially and will collapse to a
point singularity in a ﬁnite time (the “big crunch”); below it, the universe
extends inﬁnitely far in all directions and will expand forever. Interestingly,
physicists’ best current estimates place the average density rather near the
critical value, and they have so far been unable to determine whether it
is above or below it, so they do not know whether the universe will go on
existing forever or not.
Quantum Field Theory
The theory of elementary particle interactions, called quantum ﬁeld theory,
has become increasingly geometric in recent decades. In particular, the
latest attempts to unify quantum theory and gravitation have led to ever
more interesting and exotic geometric structures. The approach to quantum
gravity that is currently considered most promising by many physicists is
string theory, in which manifolds appear in several diﬀerent starring roles.
First, in order to obtain a consistent theory, it seems to be necessary to
assume that spacetime has more than four dimensions. We experience only

Why Study Manifolds?
15
four of them directly, because the dimensions beyond four are so tightly
“curled up” that they are not visible on a macroscopic scale, much as a long
but microscopically narrow cylinder would appear to be one-dimensional
when viewed from far enough away. The topological properties of the man-
ifold that appears as the “cross section” of the curled-up dimensions have
such a profound eﬀect on the observable dynamics of the resulting quan-
tum ﬁeld theory that it is possible to rule out most cross sections a priori.
It currently appears that a consistent theory can be constructed only if
the cross section is a certain kind of 6-dimensional manifold known as a
Calabi–Yau manifold. These developments in physics have stimulated pro-
found developments in the mathematical understanding of 6-manifolds in
general and Calabi-Yau manifolds in particular.
Another role that manifolds play in string theory is in describing the his-
tory of an elementary particle. One of the central tenets of string theory is
that particles should be represented not as points, but as tiny 1-dimensional
objects (“strings”) moving through spacetime. As a particle moves, it traces
out a 2-dimensional manifold called its world sheet. Physical phenomena
arise from the interactions among these diﬀerent topological and geometric
structures: the world sheet, the Calabi-Yau cross section, and the macro-
scopic four-dimensional spacetime that we see.
Manifolds are used in many more areas of mathematics than the ones
listed here, but this brief survey should be enough to show you that mani-
folds have a rich assortment of applications. It is time to get to work.

2
Topological Spaces
In this chapter we begin our study in earnest. The ﬁrst order of business
is to build up enough machinery to give a proper deﬁnition of manifolds.
The chief problem with the preliminary deﬁnition given in Chapter 1 is
that it depends on having an “ambient Euclidean space” in which our n-
manifold lives. This introduces a great deal of extraneous structure that is
irrelevant to our purposes. Instead, we would like to view a manifold as a
mathematical object in its own right, not as a subset of some larger space.
The key concept that makes this possible is that of a “topological space,”
which is the main topic of this chapter.
We begin by deﬁning topological spaces, motivated by the open set crite-
rion for continuity in metric spaces. After the deﬁnition we introduce some
of the important elementary notions associated with topological spaces such
as convergence, continuity, homeomorphisms, closures, interiors, and exte-
riors, and then explore how to construct topologies from bases. At the end
of the chapter we give the oﬃcial deﬁnition of a manifold as a topological
space with special properties.
Topologies
One of the most useful tools in analysis is the concept of a metric space.
(See the Appendix for a brief review of metric space theory.) The most
important examples, of course, are (subsets of) Euclidean spaces with the

18
2. Topological Spaces
Euclidean metric, but many others, such as function spaces, arise frequently
in analysis.
Our goal in this book is to study manifolds and those of their properties
that are preserved by homeomorphisms (continuous maps with continuous
inverses). To accomplish this, we could choose to view our manifolds as
metric spaces. However, a metric still contains extraneous information. It
is obvious that a homeomorphism between metric spaces need not preserve
distances (just think of the obvious homeomorphism between two spheres
of diﬀerent radii). So we will push the process of abstraction a step further,
and come up with a kind of “space” without distances in which continuous
functions still make sense.
The key motivation behind the deﬁnition of this new kind of space is
the open set criterion for continuity (Lemma A.5 in the Appendix), which
shows that continuous functions between metric spaces can be detected
knowing only the open sets. Motivated by this observation, we make the
following deﬁnition. A topology on a set X is a collection T of subsets of X,
called open sets, satisfying the following properties:
(i) X and ∅are elements of T.
(ii) T is closed under ﬁnite intersections: If U1, . . . , Un ∈T, then their
intersection U1 ∩· · · ∩Un is in T.
(iii) T is closed under arbitrary unions: If {Uα}α∈A is any (ﬁnite or in-
ﬁnite) collection of elements of T, then their union 
α∈A Uα is in
T.
A pair (X, T) consisting of a set X and a topology T on X is called a
topological space. The elements of a topological space are usually called
its points. Since we will rarely have occasion to discuss any other type
of space in this book, we will sometimes follow the common practice of
calling a topological space simply a space. As is common in mathematics in
discussing a set endowed with a particular kind of structure, if the topology
is understood from the context, we will typically omit it from the notation
and simply say “X is a topological space” or “X is a space.”
Aside from the simplicity of the open set criterion for continuity, the other
reason for choosing open sets as the primary objects in the deﬁnition of a
topological space is that they give us a qualitative way to detect “nearness”
to a point without necessarily having a quantitative measure of nearness
as we would in a metric space. If X is a topological space and q ∈X,
a neighborhood of q is just an open set containing q. More generally, a
neighborhood of a subset K ⊂X is an open set containing K. (In some
books, the word neighborhood is used in the more general sense of a set
containing an open set containing q; but for us neighborhoods will always
be open.) We think of something being true “near q” if it is true in some
(or every, depending on the context) neighborhood of q.
The following exercises give some simple examples of topological spaces.

Topologies
19
{{1}, {2, 3}, {1, 2, 3}, ∅}
Discrete topology
Trivial topology
FIGURE 2.1. Topologies on {1, 2, 3}.
Exercise 2.1.
Show that each of the following is a topological space. (See
Figure 2.1.)
(a) Let X denote the set {1, 2, 3}, and declare the open sets to be {1},
{2, 3}, {1, 2, 3}, and the empty set.
(b) Any set X whatsoever, with T = {all subsets of X}. This is called the
discrete topology on X, and (X, T) is called a discrete space.
(c) Any set X, with T = {∅, X}. This is called the trivial topology on X.
(d) Any metric space (M, d), with T equal to the collection of all subsets
of M that are open in the metric space sense. This topology is called
the metric topology on M.
Metric spaces provide a rich source of examples of topological spaces. In
fact, a large percentage of the topological spaces we will need to consider are
actually subsets of Euclidean spaces Rn, with the metric topology induced
by the Euclidean metric (which we call the Euclidean topology). Unless we
specify otherwise, subsets of Rn will always be considered as topological
spaces with this topology. Thus our intuition regarding topological spaces
will rely heavily on our understanding of subsets of Euclidean space.
Another important class of examples of topological spaces is obtained
by taking open subsets of other spaces. If X is a topological space, and
Y is any open subset of X, then we can deﬁne a topology on Y just by
declaring the open sets of Y to be those open sets of X that are contained
in Y . It is trivial to check that the three deﬁning properties of a topology
are satisﬁed. (In the next chapter, we will show how to put a topology on
any subset of a topological space.)
Convergence and Continuity
The primary reason topological spaces were invented was that they provide
the most general setting for studying the notions of convergence and con-
tinuity. For this reason, it is appropriate to introduce these concepts next.
We begin with convergence.
The deﬁnition of convergence of a sequence of points in a metric space
(see the Appendix) is really just a fancy way of saying that as we go far

20
2. Topological Spaces
enough out in the sequence, the points of the sequence become “arbitrarily
close” to q.
In topological spaces, we use neighborhoods to encode the notion of “ar-
bitrarily close.” Thus, if X is a topological space and {qi} is any sequence
of points in X, we say that the sequence converges to q ∈X, and q is the
limit of the sequence, if for every neighborhood U of q there exists N such
that qi ∈U for all i ≥N. Symbolically, this is denoted by either qi →q or
limi→∞qi = q.
Exercise 2.2.
Show that in a metric space, this topological deﬁnition of
convergence is equivalent to the metric space deﬁnition.
For the types of topological spaces we will be chieﬂy interested in (mostly
manifolds), convergent sequences behave very much the same way we are
used to from our experience with Euclidean space. Nevertheless, it is good
to be aware that for some of the stranger examples of topological spaces,
convergence can sometimes have an unintuitive meaning, as the following
exercises show.
Exercise 2.3.
(a) Let X be a discrete topological space. Show that the only convergent
sequences in X are the ones that are “eventually constant,” that is,
sequences {qi} such that qi = q for all i greater than some N.
(b) Let Y be a trivial topological space (that is, a set with the trivial
topology {∅, Y }). Show that every sequence in Y converges to every
point of Y .
At the end of this chapter we will describe a restricted class of topological
spaces (Hausdorﬀspaces) for which the pathological behavior of (b) cannot
occur.
Next we address the most important topological concept of all: continu-
ous maps. If X and Y are topological spaces, a map f : X →Y is said to
be continuous if for every open set U ⊂Y , f −1(U) is open in X.
The open set criterion (Lemma A.5) for continuity in metric spaces says
precisely that a map between metric spaces is continuous in this sense if and
only if it is continuous in the usual ε-δ sense. Therefore, all the maps that
you know to be continuous from metric space theory are also continuous as
maps of topological spaces. Examples include polynomial functions from R
to R, linear transformations from Rn to Rk, and, more generally, any map
from a subset of Rn to Rk whose component functions are continuous in
the ordinary sense, such as polynomial, exponential, rational, logarithmic,
absolute value, and trigonometric functions (where they are deﬁned), and
functions built up from these by composition.
The next lemma gives some elementary but important properties of con-
tinuous maps. The ease with which properties like this can be proved is
one of the virtues of deﬁning continuity in terms of open sets.

Topologies
21
Lemma 2.1. Let X, Y , and Z be topological spaces.
(a) Any constant map f : X →Y is continuous.
(b) The identity map Id: X →X is continuous.
(c) If f : X →Y is continuous, so is the restriction of f to any open
subset of X.
(d) If f : X →Y and g: Y →Z are continuous, so is their composition
g ◦f : X →Z.
Proof. We will prove (d) and leave the other parts as exercises. We have
to show that if U is any open subset of Z, then (g ◦f)−1(U) is an open
subset of X. By elementary set-theoretic considerations, (g ◦f)−1(U) =
f −1(g−1(U)). Applying the deﬁnition of continuity to g, g−1(U) is open;
and then doing the same for f shows that f −1(g−1(U)) is open.
Exercise 2.4.
Prove parts (a)–(c) of Lemma 2.1.
In metric spaces it makes sense to talk about a map being “continuous at
a point” (f : M1 →M2 is continuous at x ∈M1 if for all ε > 0, there exists
δ > 0 such that for each y ∈M1, d1(y, x) < δ implies d2(f(y), f(x)) < ε),
and a map is continuous if and only if it is continuous at every point. In
topological spaces, continuity at a point is generally not a very useful con-
cept. However, it is an important fact that continuity is a “local” property,
in the sense that a map is continuous if and only if it is continuous in a
neighborhood of every point. The precise statement is given in the following
important lemma.
Lemma 2.2 (Local Criterion for Continuity). A map f : X →Y be-
tween topological spaces is continuous if and only if each point of X has a
neighborhood on which (the restriction of ) f is continuous.
Proof. If f is continuous, we may simply take each neighborhood to be X
itself. Conversely, suppose f is continuous in a neighborhood of each point,
and let U ⊂Y be any open set; we have to show that f −1(U) is open. Any
point x ∈f −1(U) has a neighborhood Vx on which f is continuous (Figure
2.2). Continuity of f|Vx implies, in particular, that (f|Vx)−1(U) is open in
Vx, and therefore also open in X. Unwinding the deﬁnitions, we see that
(f|Vx)−1(U) = {x ∈Vx : f(x) ∈U} = f −1(U) ∩Vx,
which contains x and is contained in f −1(U). Since f −1(U) is the union of
all such open sets as x ranges over f −1(U), it follows that f −1(U) is open,
as desired.

22
2. Topological Spaces
X
Y
x
f
Vx
U
f −1(U)
FIGURE 2.2. Local criterion for continuity.
If X and Y are topological spaces, a homeomorphism from X to Y is
deﬁned to be a continuous bijective map ϕ: X →Y with continuous in-
verse. If there exists a homeomorphism between X and Y , we say that
X and Y are homeomorphic or topologically equivalent. Sometimes this is
abbreviated X ≈Y .
Exercise 2.5.
Show that “homeomorphic” is an equivalence relation.
The homeomorphism relation is the most fundamental relation in topol-
ogy. In fact, as we mentioned in Chapter 1, “topological properties” are
exactly those that are preserved by homeomorphisms.
Here are a few explicit examples of homeomorphisms that you should
keep in mind.
Example 2.3. Any open ball in Rn is homeomorphic to any other open
ball; the homeomorphism can easily be constructed as a composition of
translations x 
→x + x0 and dilations x 
→cx. Similarly, all spheres in Rn
are homeomorphic to each other. These examples illustrate that “size” is
not a topological property.
Example 2.4. Let Bn denote the open unit ball B1(0) ⊂Rn, and deﬁne
a map F : Bn →Rn by
y = F(x) =
x
1 −|x|2 .
Note that |F(x)| = |x|/(1 −|x|2) →∞as |x| →1. It is straightforward to
check that the inverse of F is given by
x = F −1(y) =
2y
1 +

1 + 4|y|2 .
Thus F is a homeomorphism, so Rn is homeomorphic to Bn. This shows
that “boundedness” is not a topological property.
Example 2.5. Another illustrative example is the homeomorphism be-
tween a cube and a sphere alluded to in Chapter 1. Let S2 = {x ∈

Topologies
23
FIGURE 2.3. Deforming a cube into a sphere.
R3 : |x| = 1} denote the unit sphere in R3, and set C = {(x, y, z) :
max(|x|, |y|, |z|) = 1}, which is the cubical surface of side 2 centered at
the origin. Let ϕ: C →S2 be the map that projects each point on C radi-
ally inward to the sphere (Figure 2.3). More precisely, given a point q ∈C,
ϕ(q) is the unit vector in the direction of q. Thus ϕ is given by the formula
ϕ(x, y, z) =
(x, y, z)

x2 + y2 + z2 ,
which is continuous by the usual arguments of elementary analysis. The
next exercise shows that ϕ is a homeomorphism. This example demon-
strates that “corners” are not topological properties.
Exercise 2.6.
Show that the map ϕ: C →S2 is a homeomorphism by
showing that its inverse can be written
ϕ−1(x, y, z) =
(x, y, z)
max (|x|, |y|, |z|).
In the deﬁnition of a homeomorphism, it is important to note that al-
though the assumption that ϕ is bijective guarantees that the inverse map
ϕ−1 exists for set-theoretic reasons, continuity of ϕ−1 is not automatic.
The next exercise gives an example of a continuous bijection whose inverse
is not continuous.
Exercise 2.7.
Let X denote the half-open interval [0, 1) ⊂R, and let S1
denote the unit circle in R2 (both with the Euclidean metric topologies, of
course). Deﬁne a map a: X →S1 by a(t) = (cos 2πt, sin 2πt) (Figure 2.4).
Show that a is continuous and bijective but not a homeomorphism.

24
2. Topological Spaces
a
FIGURE 2.4. A map that is bijective but not a homeomorphism.
A map f : X →Y (continuous or not) is said to be an open map if for
any open set U ⊂X, the image set f(U) is open in Y . A map can be open
but not continuous, continuous but not open, both, or neither.
There is a generalization of homeomorphisms that is often useful. We
say that a continuous map f : X →Y between topological spaces is a local
homeomorphism if every point x ∈X has a neighborhood U ⊂X such that
f(U) is an open subset of Y and f|U : U →f(U) is a homeomorphism.
Exercise 2.8.
(a) Show that every local homeomorphism is an open map.
(b) Show that every homeomorphism is a local homeomorphism.
(c) Show that a bijective continuous open map is a homeomorphism.
(d) Show that a bijective local homeomorphism is a homeomorphism.
Closed Sets
Because of the importance of neighborhoods in understanding a topological
space and its continuous maps and convergent sequences, the deﬁnition of
a topological space takes open sets as the primary objects. There is also a
complementary notion that is nearly as important.
A subset F of a topological space X is said to be closed if its complement
X ∖F is open. From the deﬁnition of topological spaces, several properties
follow immediately:
(i) X and ∅are closed.
(ii) Finite unions of closed sets are closed.
(iii) Arbitrary intersections of closed sets are closed.
A topology on a set X can be deﬁned by describing the collection of closed
sets, as long as they satisfy these three properties; the open sets are then
just those sets whose complements are closed.
Here are some examples of closed subsets of familiar topological spaces.

Topologies
25
Example 2.6 (Closed Sets).
(a) Any closed interval [a, b] ⊂R is a closed set, as are the half-inﬁnite
closed intervals [a, ∞) and (−∞, b].
(b) Any closed ball in a metric space is a closed set (Exercise A.11(b) in
the Appendix).
(c) Every subset of a discrete space is closed.
It is important to be aware that just as in metric spaces, “closed” is not
the same as “not open”—sets can be both open and closed, or neither open
nor closed. For example, in any topological space X, the sets X and ∅are
both open and closed. On the other hand, the half-open interval [0, 1) is
neither open nor closed in R.
Continuity can be detected by closed sets as well as open ones.
Lemma 2.7. A map between topological spaces is continuous if and only
if the inverse image of every closed set is closed.
Exercise 2.9.
Prove Lemma 2.7.
Given any set A ⊂X, we deﬁne several related sets as follows. The
closure of A in X, denoted by A, is the set
A =

{B ⊂X : B ⊃A and B is closed in X}.
The interior of A, written Int A, is
Int A =

{C ⊂X : C ⊂A and C is open in X}.
It is obvious from the properties of open and closed sets that A is closed
and Int A is open. In words, A is “the smallest closed set containing A,”
and Int A is “the largest open set contained in A.”
We also deﬁne the exterior of A, written Ext A, as
Ext A = X ∖A,
and the boundary of A, written ∂A, as
∂A = X ∖(Int A ∪Ext A).
It follows immediately from the deﬁnitions that for any subset A ⊂X,
the whole space X is equal to the disjoint union of Int A, Ext A, and ∂A.
The set A always contains all of its interior points and none of its exterior
points, and may contain all, some, or none of its boundary points.
For many purposes, it is useful to have alternative characterizations of
open and closed sets, and of the interior, exterior, closure, and boundary
of a given set. The following lemma gives such characterizations. Some of
these are probably familiar to you from your study of Euclidean and metric
spaces. See Figure 2.5 for illustrations of some of these characterizations.

26
2. Topological Spaces
Ext A
Int A
∂A
A
FIGURE 2.5. Interior, exterior, and boundary points.
Lemma 2.8. Let X be a topological space and A ⊂X any subset.
(a) A point q is in the interior of A if and only if q has a neighborhood
contained in A.
(b) A point q is in the exterior of A if and only if q has a neighborhood
contained in X ∖A.
(c) A point q is in the boundary of A if and only if every neighborhood
of q contains both a point of A and a point of X ∖A.
(d) Int A and Ext A are open in X, while ∂A is closed in X.
(e) A is open if and only if A = Int A.
(f ) A is closed if and only if it contains all its boundary points, which is
true if and only if A = Int A ∪∂A.
(g) A = A ∪∂A = Int A ∪∂A.
Exercise 2.10.
Prove Lemma 2.8.
Given a topological space X and a set A ⊂X, we say that a point
q ∈X is a limit point of A if every neighborhood of q contains a point of
A other than q (which might or might not itself be in A). Limit points are
also sometimes called accumulation points or cluster points. For example,
if X = R and A = (0, 1), then every point in [0, 1] is a limit point of A. If
we let B = {1/n}∞
n=1 ⊂R, then 0 is the only limit point of B.
Exercise 2.11.
Show that a set A in a topological space is closed if and
only if it contains all of its limit points.
A subset A of a topological space X is said to be dense in X if A = X.

Bases
27
Exercise 2.12.
Show that a subset A ⊂X is dense if and only if every
nonempty open set in X contains a point of A.
Exercise 2.13.
Show that Rn has a countable dense subset.
Analogous to open maps are closed maps: A map f : X →Y is said to
be closed if it takes closed sets in X to closed sets in Y .
Exercise 2.14.
Show that a bijective continuous map is a homeomor-
phism if and only if it is open if and only if it is closed.
Bases
To deﬁne a topology on a given set, it is often convenient to single out
some “special” open sets and use them to deﬁne the rest of the open sets.
For example, the metric topology is deﬁned by ﬁrst deﬁning balls and then
declaring a set to be open if it contains a ball around each of its points.
This idea can be generalized easily to arbitrary topological spaces, as in
the next deﬁnition.
Suppose X is any set. A basis in X is a collection B of subsets of X
satisfying the following conditions:
(i) Every element of X is in some element of B; in other words, X =

B∈B B.
(ii) If B1, B2 ∈B and x ∈B1 ∩B2, there exists an element B3 ∈B such
that x ∈B3 ⊂B1 ∩B2.
Proposition 2.9. Let B be a basis in a set X, and let T be the collection
of all unions of elements of B. Then T is a topology on X.
This topology T is called the topology generated by B. Before we prove
the proposition, it will be useful to have an alternative characterization of
T, analogous to the deﬁnition of open sets in a metric space in terms of
balls. Given X and a collection B of subsets of X, we say that a subset
U ⊂X satisﬁes the basis criterion with respect to B if for every x ∈U,
there exists B ∈B such that x ∈B ⊂U.
Lemma 2.10. Suppose B is a basis in X. Then the collection T deﬁned in
Proposition 2.9 is precisely the set of all subsets of X that satisfy the basis
criterion with respect to B.
Proof. Let U ⊂X, and suppose ﬁrst that U satisﬁes the basis criterion.
Let
V =

{B ∈B : B ⊂U}.

28
2. Topological Spaces
U1
U2
B1
B2
B3
x
FIGURE 2.6. Proof that U1 ∩U2 satisﬁes the basis criterion.
Obviously, V ∈T, since V is by deﬁnition a union of basis sets. Thus if we
can show that U = V , it will follow that U ∈T. Clearly, V ⊂U, because
V is a union of subsets of U. To show that U ⊂V , let x ∈U be arbitrary;
since U satisﬁes the basis criterion, there must exist a basis set B ∈B such
that x ∈B ⊂U. It follows immediately that x ∈V , so we are done.
Conversely, suppose that U ∈T. This means that U is a union of elements
of B, i.e., for some subset A ⊂B, U = 
B∈A B. In other words, x ∈U if
and only if x ∈B for some B ∈A. In particular, x ∈B ⊂U, so U satisﬁes
the basis criterion.
Proof of Proposition 2.9. We need to show that T satisﬁes the three deﬁn-
ing conditions for a topology. First, the fact that X = 
B∈B B means that
X ∈T. The empty set is also in T trivially. (It is the “union of no elements
of B”!) A union of elements of T is a union of unions of elements of B, and
therefore is itself a union of elements of B; thus T is closed under arbitrary
unions.
Finally, to show that T is closed under ﬁnite intersections, suppose ﬁrst
that U1, U2 ∈T. Then, for any x ∈U1 ∩U2, the basis criterion says that
there exist basis elements B1, B2 ∈B such that x ∈B1 ⊂U1 and x ∈B2 ⊂
U2 (Figure 2.6). But then part (ii) of the deﬁnition of basis guarantees that
there exists B3 ∈B such that x ∈B3 ⊂B1 ∩B2 ⊂U1 ∩U2. Thus U1 ∩U2
satisﬁes the basis criterion, so it is again in T. This shows that T is closed
under pairwise intersections, and closure under ﬁnite intersections follows
easily by induction.
It often happens that we are given a particular topological space X
together with a collection B of open subsets of X, and we would like to
know whether B forms a basis for the topology of X. On the face of it,
this would require showing ﬁrst that B satisﬁes the two conditions in the

Bases
29
deﬁnition of a basis, and then that each open subset of X is a union of
elements of B (or alternatively satisﬁes the basis criterion). But as the
following lemma shows, once we know that the sets in B are open subsets
with respect to some topology, showing that they actually are a basis for
that topology is much easier.
Lemma 2.11. Suppose X is a topological space, and B is a collection of
open subsets of X. If every open subset of X satisﬁes the basis criterion
with respect to B, then B is a basis for the topology of X.
Proof. By Lemma 2.10, all we need to show is that B satisﬁes the two
deﬁning conditions for a basis.
For the ﬁrst condition, since X itself is an open subset, the basis criterion
tells us that any point x ∈X is in some element B ∈B; thus the union of
all the elements of B is X.
For the second condition, suppose B1 and B2 are elements of B and
x ∈B1∩B2. The basis criterion applied to B1∩B2 (which is the intersection
of two open subsets of X and therefore open) guarantees the existence of
B3 ∈B such that x ∈B3 ⊂B1 ∩B2.
The next exercise describes bases for the topologies of Exercise 2.1. The
preceding lemma makes the job of showing that they are indeed bases quite
straightforward.
Exercise 2.15.
In each of the following cases, prove that the given set B
is a basis for the given topology.
(a) M is a metric space with the metric topology, and B is the collection
of all open balls in M.
(b) X is a set with the discrete topology, and B is the collection of all
one-point subsets of X.
(c) X is a set with the trivial topology, and B = {X}.
Exercise 2.16.
Show that each of the following collections Bi is a basis
for the Euclidean topology on Rn.
(a) B1 = {Cs(x) : x ∈Rn and s > 0}, where Cs(x) is the open cube of
side s around x:
Cs(x) = {y = (y1, . . . , yn) : |xi −yi| < s/2, i = 1, . . . , n}.
(b) B2 = {Br(x) : r is rational and x has rational coordinates}.
When we have a basis for a topology on Y , it is suﬃcient (and often
much easier) to check continuity of maps into Y using only basis open sets,
as the following lemma shows.

30
2. Topological Spaces
Lemma 2.12. Let X and Y be topological spaces and let B be a basis for
Y . A map f : X →Y is continuous if and only if for every basis open set
B ∈B, f −1(B) is open in X.
Proof. Clearly, if f is continuous, the inverse image of every basis open set
is open. Conversely, suppose f −1(B) is open for every B ∈B. Let U ⊂Y
be open, and let x ∈f −1(U). By the basis criterion, there is a basis set B
such that f(x) ∈B ⊂U. This implies that x ∈f −1(B) ⊂f −1(U), which
means that x has a neighborhood contained in f −1(U). Since this is true
for every x ∈U, U is the union of all these neighborhoods as x ranges over
points of U, and therefore is open.
Manifolds
We are almost ready to give the oﬃcial deﬁnition of manifolds. We need
just a few more preliminary deﬁnitions. The ﬁrst one is easy, and captures
very precisely the intuitive idea that a manifold should look “locally” like
Euclidean space. Let X be a topological space. A topological space M
is said to be locally Euclidean of dimension n if every point q ∈M has
a neighborhood that is homeomorphic to an open subset of Rn. Such a
neighborhood is called a Euclidean neighborhood of q.
For some purposes, it is useful to be more speciﬁc about the kind of open
subset we use to characterize locally Euclidean spaces. The next lemma
shows that we could have replaced “open subset” by open ball or by Rn
itself.
Lemma 2.13. A topological space M is locally Euclidean of dimension n
if and only if either of the following properties holds:
(a) Every point of M has a neighborhood homeomorphic to an open ball
in Rn.
(b) Every point of M has a neighborhood homeomorphic to Rn.
Proof. It is immediate that any space with property (a) or (b) is locally
Euclidean of dimension n. Conversely, suppose M is locally Euclidean of
dimension n. Because any open ball in Rn is homeomorphic to Rn itself
(Example 2.4), properties (a) and (b) are equivalent, so we need only prove
(a).
Given any point q ∈M, let U be a neighborhood of q that admits a
homeomorphism ϕ: U →V , where V is an open subset of Rn. The fact
that V is open means that there is some open ball B around ϕ(q) that is
contained in V , and then ϕ−1(B) is a neighborhood of q homeomorphic to
an open ball.

Manifolds
31
If M is locally Euclidean of dimension n, a homeomorphism from an open
subset U ⊂M to an open subset of Rn is called a coordinate chart (or just
a chart) on U. We will call any open subset of M that is homeomorphic
to a ball in Rn a Euclidean ball in M. (When M has dimension 2, we will
sometimes use the term Euclidean disk.) The preceding lemma shows that
every point in a locally Euclidean space has a Euclidean ball neighborhood.
The deﬁnition of locally Euclidean spaces makes sense even when n = 0.
Since R0 is by convention a single point, Lemma 2.13(b) implies that a
space is locally Euclidean of dimension 0 if and only if each point has a
neighborhood homeomorphic to a one-point space, or in other words if and
only if the space is discrete.
There are two other properties that we will include in the deﬁnition of
manifolds, to rule out “pathological” spaces that might otherwise pass as
manifolds.
HausdorﬀSpaces
The ﬁrst property we want to introduce ensures that there are “enough”
open sets, so that neighborhoods behave more or less the way our intuition
derived from Euclidean and metric spaces leads us to expect. For example,
in a metric space, a one-point set {q} is always closed, because around every
point other than q there is a ball that does not include q. More generally, any
two points in a metric space always have disjoint neighborhoods. However,
these properties do not always hold in topological spaces. Consider the set
{1, 2, 3} with the topology {∅, {1}, {2, 3}, {1, 2, 3}} (Figure 2.1). In this
case 2 and 3 do not have disjoint neighborhoods, since every open set that
contains one also contains the other. Moreover, the set {2} is not closed,
because its complement is not open.
The problem with this example is that there are too few open sets, so
neighborhoods do not have the same intuitive meaning they have in metric
spaces. In our study of manifolds, we will want to rule out such “patholog-
ical” spaces, so we make the following deﬁnition. A topological space X is
said to be a Hausdorﬀspace if given any pair of distinct points q1, q2 ∈X,
there exist neighborhoods U1 of q1 and U2 of q2 with U1 ∩U2 = ∅. This
property is often summarized by saying “open sets separate points.”
Any metric space is Hausdorﬀ. (If d(q1, q2) = r, then the open balls of
radius r/2 around q1 and q2 are disjoint by the triangle inequality.) More
generally, any open subset of a Hausdorﬀspace is Hausdorﬀ: If V ⊂X is
open in the Hausdorﬀspace X, and q1, q2 are distinct points in V , then in
X there are open sets U1, U2 separating q1 and q2, and the sets U1 ∩V and
U2 ∩V are open in V , disjoint, and contain q1 and q2, respectively.
Hausdorﬀspaces have many of the properties that we expect of metric
spaces, such as those expressed in the following lemma.
Lemma 2.14. Let X be a Hausdorﬀspace.

32
2. Topological Spaces
(a) Every one-point set in X is closed.
(b) If a sequence {xi} in X converges to a limit x ∈X, the limit is
unique.
Proof. For part (a), choose any q0 ∈X. Given p ̸= q0, the Hausdorﬀ
property says that there exist disjoint neighborhoods Up of q0 and Vp of p.
This means that the complement of {q0} is equal to the union of the open
sets Vp as p ranges over X ∖{q0}, which is open, so {q0} is closed.
To prove that limits are unique, suppose that x and x′ are two distinct
limits of the sequence {xi}. By the Hausdorﬀproperty, there exist disjoint
neighborhoods U of x and U ′ of x′. By deﬁnition of convergence, there exist
N, N ′ such that i ≥N implies xi ∈U and i ≥N ′ implies xi ∈U ′. But since
U and U ′ are disjoint, this is a contradiction when i ≥max(N, N ′).
Exercise 2.17.
Show that the only Hausdorﬀtopology on a ﬁnite set is
the discrete topology.
The non-Hausdorﬀexample above involving {1, 2, 3} is obviously con-
trived, and has little relevance to our study of manifolds. But in Problem
3-8 at the end of the next chapter you will see a space that would be a
manifold except for the fact that it fails to be Hausdorﬀ.
Second Countability
Whereas the Hausdorﬀproperty ensures that there are enough open sets,
the next property we will introduce ensures that there are not too many.
We say that a topological space is second countable if it admits a countable
basis.
As the “second” in the name second countable suggests, there is also
another weaker notion of countability. It relies on the following deﬁnition:
If X is a space and q ∈X, a collection Bq of neighborhoods of q is called a
neighborhood basis at q if every neighborhood of q contains some B ∈Bq.
X is said to be ﬁrst countable if there exists a countable neighborhood
basis at each point. Second countability implies ﬁrst countability: Given a
countable basis for X, the collection of basis open sets containing q is easily
seen to be a countable neighborhood basis at q.
One of the ways in which second countability is often used is in reducing
the number of open sets one needs to “cover” a space. If X is any topological
space, a collection U of subsets of X is said to cover X, or to be a cover of
X, if every point in X is in one of the sets of U. An open cover of X is a
collection of open sets that covers X. Given any cover U, a subcover of U
is a subset of U that is still a cover.
Lemma 2.15. If X is a second countable space, every open cover of X
has a countable subcover.

Manifolds
33
Proof. Let B be a countable basis for X, and let U be an arbitrary open
cover of X. Let B′ denote the subset of B consisting of those basis sets
that are entirely contained in some element of U. Because any subset of a
countable set is countable, B′ is a countable set.
Now, for each element B ∈B′, choose an element UB ∈U such that
B ⊂UB (this is possible by the way we deﬁned B′). The collection U′ =
{UB : B ∈B′} is a countable subset of U; the lemma will be proved if we
can show that it still covers X.
If x ∈X is arbitrary, then x ∈U0 for some open set U0 ∈U. By the basis
criterion for U0, there is some B ∈B such that x ∈B ⊂U0. This means,
in particular, that B ∈B′, and therefore there is a set UB ∈U′ such that
x ∈B ⊂UB. This shows that U′ is a cover and completes the proof.
Most “reasonable” spaces are second countable. For example, it follows
from Exercise 2.16(b) above that Rn is second countable. Moreover, any
open subset U of a second countable space X is second countable: Starting
with a countable basis for X, just throw away all the elements of the basis
that do not lie in U; then it is easy to check that the remaining basis sets
form a countable basis for the topology of U.
In Problems 3-7 and 4-6 we will see examples of spaces that would be
manifolds except for the failure of second countability.
Deﬁnition of Manifolds
We come now to the culmination of this chapter: the oﬃcial deﬁnition of
manifolds.
An n-dimensional topological manifold is a second countable Hausdorﬀ
space that is locally Euclidean of dimension n. Since the only kind of man-
ifolds we will be considering in this book are topological manifolds, we
will usually simply call them n-dimensional manifolds, or n-manifolds, or
even just manifolds if the dimension is understood or irrelevant. (The term
“topological manifold” is usually used only to emphasize that the kind
of manifold under consideration is the kind we have deﬁned here, which
is a topological space with special properties, rather than other kinds of
manifolds that can be deﬁned, such as “smooth manifolds” or “complex
manifolds.” We will not treat any of these other kinds of manifolds in this
book.)
A shorthand notation that is in common use is to write “let M n be a
manifold” to mean “let M be a manifold of dimension n.” The superscript n
is not part of the name of the manifold, and is usually dropped after the ﬁrst
time the manifold is introduced. One must be a bit careful to distinguish
this notation from the n-fold Cartesian product M n = M × · · · × M, but
it is usually clear from the context which is meant. We will not use this
shorthand in this book, but you should be aware of it because you will
encounter it in your reading.

34
2. Topological Spaces
FIGURE 2.7. A manifold with boundary.
The most obvious example of an n-manifold is Rn itself. More gener-
ally, any open subset of Rn—or in fact of any n-manifold—is again an
n-manifold, as the next lemma shows.
Lemma 2.16. Any open subset of an n-manifold is an n-manifold.
Proof. Let M be an n-manifold, and let V be an open subset of M. Any
q ∈V has a neighborhood (in M) that is homeomorphic to an open subset
of Rn; the intersection of that neighborhood with V is still open, still home-
omorphic to an open subset of Rn, and lies in V , so V is locally Euclidean.
We remarked above that any open subset of a Hausdorﬀspace is Haus-
dorﬀand any open subset of a second countable space is second countable.
Therefore V is an n-manifold.
In the next few chapters we will develop many more examples of mani-
folds.
Manifolds with Boundary
For some purposes it is useful also to have the following more general notion.
An n-dimensional manifold with boundary is a second countable Hausdorﬀ
space in which every point has a neighborhood homeomorphic to an open
subset of the n-dimensional upper half space Hn = {(x1, . . . , xn) ∈Rn :
xn ≥0}. Just as in the case of manifolds, we will call any homeomorphism
from an open subset U of M to an open subset of Hn a chart on U.
Example 2.17 (Manifolds with Boundary). The upper half space Hn
itself is obviously a manifold with boundary, as is any closed interval in R,
any closed disk in R2, or in fact a closed ball in any Euclidean space (see
Figure 2.7). (This is not hard to see intuitively. You can probably construct
appropriate charts yourself, or you can wait until Chapter 3 and use the
ones suggested in Problem 3-4.)
The boundary of Hn in Rn is the set of points where xn = 0. If M is a
manifold with boundary, a point that is in the inverse image of ∂Hn under
some chart is called a boundary point of M, and a point that is in the
inverse image of Int Hn is called an interior point. The boundary of M (the

Manifolds
35
set of all its boundary points) is denoted by ∂M; similarly, its interior is
denoted by Int M.
Note that this use of the terms “boundary” and “interior” is distinct
from their use earlier in this chapter in reference to subsets of topological
spaces: If M is a manifold with boundary, its boundary as a subset of itself
is always empty, even though its boundary as a manifold with boundary
may not be. Usually the distinction will be clear from the context, but if
necessary we can always distinguish the two meanings by referring to the
topological boundary or the manifold boundary as appropriate.
There is a subtlety about this deﬁnition that might not be immediately
evident. Although the interior and boundary of a manifold with boundary
M are well-deﬁned subsets, and it might seem intuitively rather obvious
that they are disjoint sets, we have no way of proving at this stage that
a point of M cannot be simultaneously both a boundary point and an
interior point. After we have developed some more machinery, you will be
asked to prove this fact (for the 1-dimensional case in Problem 4-14, the
2-dimensional case in Problem 8-6, and the general case in Problem 13-9).
Nonetheless, we will go ahead and assume it when convenient.
Since any open ball in Rn is homeomorphic to an open subset of Hn,
an n-manifold is automatically an n-manifold with boundary (with empty
boundary). But the converse is not true: For example, an endpoint of a
closed interval has no Euclidean neighborhood. Assuming the (as yet un-
proved) fact that a boundary point cannot be an interior point, it follows
that a manifold with boundary is a manifold if and only if its boundary is
empty.

36
2. Topological Spaces
Problems
2-1. Let (X1, T1) and (X2, T2) be topological spaces and let f : X1 →X2
be a bijective map. Show that f is a homeomorphism if and only
if f(T1) = T2 in the sense that U ∈T1 if and only if f(U) ∈T2.
[This shows, roughly speaking, that the topology is precisely the in-
formation preserved by homeomorphisms, and justiﬁes the deﬁnition
of topological spaces as the right setting for studying properties pre-
served by homeomorphisms.]
2-2. Suppose X is a set, and B is any collection of subsets of X whose
union equals X. Let T be the collection of all unions of ﬁnite inter-
sections of elements of B. (Note that the empty set is the union of
the empty collection of sets.)
(a) Show that T is a topology. (It is called the topology generated by
B, and B is called a subbasis for T.)
(b) Show that T is the “smallest” topology for which all the sets in
B are open; more precisely, show that T is the intersection of all
topologies containing B.
2-3. Let X be an inﬁnite set. Consider the following collections of subsets
of X:
T1 = {U ⊂X : X ∖U is ﬁnite or is all of X};
T2 = {U ⊂X : X ∖U is inﬁnite or is empty};
T3 = {U ⊂X : X ∖U is countable or is all of X}.
For each collection, determine whether it is a topology.
2-4. Let X = {1, 2, 3}. Give a list of topologies on X such that any topol-
ogy on X is homeomorphic to exactly one on your list.
2-5. Let X = R2 as a set, but with the topology determined by the fol-
lowing basis:
B = {sets of the form {(c, y) : a < y < b}, for ﬁxed a, b, c ∈R}.
Determine which (if either) of the identity maps X →R2, R2 →X
is continuous.
2-6. Let X be a discrete space, Y be a space with the trivial topology,
and Z be any topological space. Show that any maps f : X →Z
and g: Z →Y are continuous. If Z is Hausdorﬀ, show that the only
continuous maps h: Y →Z are constant maps.
2-7. Give examples of maps between subsets of the plane (with the Eu-
clidean topology) that are

Problems
37
(a) open but not closed or continuous;
(b) closed but not open or continuous;
(c) continuous but neither open nor closed;
(d) continuous and open but not closed;
(e) continuous and closed but not open;
(f) open and closed but not continuous.
2-8. Let f : X →Y be a continuous map between topological spaces, and
let B be a basis for the topology of X. Let f(B) denote the collection
{f(B) : B ∈B} of subsets of Y . If f is surjective and open, show
that f(B) is a basis for the topology of Y .
2-9. Suppose we are given an indexed collection of nonempty topological
spaces {Xα}α∈A. Declare a subset of the disjoint union 
α∈A Xα to
be open if and only if its intersection with each Xα is open.
(a) Show that this is a topology on 
α∈A Xα, called the disjoint
union topology.
(b) Show that a subset of the disjoint union is closed if and only if
its intersection with each Xα is closed.
(c) If each Xα is an n-manifold, show that the disjoint union

α∈A Xα is an n-manifold if and only if the index set A is
countable.
2-10. Suppose X is locally Euclidean of dimension n, and f : X →Y is
a surjective local homeomorphism. Show that Y is also locally Eu-
clidean of dimension n.
2-11. Show that a topological space is a 0-manifold if and only if it is a
countable discrete space.
2-12. Let X be a totally ordered set (see the Appendix), and assume that X
has at least two elements. For any a ∈X, deﬁne sets L(a), R(a) ⊂X
by
L(a) = {c ∈X : c < a},
R(a) = {c ∈X : c > a}.
Give X the topology generated by the subbasis {L(a), R(a) : a ∈X},
called the order topology.
(a) Show that each set of the form (a, b) is open in X and each set
of the form [a, b] is closed (where (a, b) and [a, b] are deﬁned just
as in R).
(b) Show that X is Hausdorﬀ.

38
2. Topological Spaces
(c) Show that for any a, b ∈X, (a, b) ⊂[a, b]. Under what conditions
does equality hold?
2-13. Let X be a second countable topological space. Show that every col-
lection of disjoint open subsets of X is countable.
2-14. Show that locally Euclidean spaces and metric spaces are ﬁrst count-
able.
2-15.
(a) Show that every second countable space has a countable dense
subset.
(b) Show that a metric space is second countable if and only if it
has a countable dense subset.
2-16. Let X be a ﬁrst countable space.
(a) For any set A ⊂X and any point p ∈X, show that p ∈A if and
only if there is a sequence {pn}∞
n=1 in A such that pn →p.
(b) Show that for any space Y , a map f : X →Y is continuous
if and only if f takes convergent sequences in X to convergent
sequences in Y .
2-17. Show that any manifold has a basis of Euclidean balls.
2-18. Suppose M is an n-dimensional manifold with boundary. Show that
Int M is an n-manifold and ∂M is an (n−1)-manifold (without bound-
ary).

3
New Spaces from Old
In this chapter we introduce three standard ways of constructing new topo-
logical spaces from given ones: subspaces, product spaces, and quotient
spaces. We will explore how various topological properties are aﬀected by
these constructions, and we will show how each topology is characterized
by which maps it makes continuous. At the end of the chapter we will
explore in some detail the quotient spaces that arise from group actions.
Throughout the chapter we will use these tools to build new examples of
manifolds.
Subspaces
We have seen a number of examples of topological spaces that are subsets
of Rn, with the topology induced by the Euclidean metric. We have also
seen that open subsets of a topological space inherit a topology from the
containing space. It turns out that arbitrary subsets of topological spaces
can also be viewed as topological spaces in their own right.
Let X be a space, and let A ⊂X be any subset. We deﬁne a topology
TA on A by
TA = {U ⊂A : U = A ∩V for some open set V ⊂X}.
In other words, the open sets of TA are the intersections with A of the open
sets of X (Figure 3.1).
Exercise 3.1.
Prove that TA is a topology on A.

40
3. New Spaces from Old
X
V
A
U
FIGURE 3.1. An open set in the subspace A.
0
1
1
2
3
0 . . . 1
5
1
3
1
2
1
4
B
C
FIGURE 3.2. Subspaces of R.
The topology TA is called the subspace topology (or sometimes the relative
topology) on A. A subset of a topological space X is called a subspace of
X if it is endowed with the subspace topology. Henceforth, whenever we
mention a subset of a topological space, we will always consider it as a
topological space with the subspace topology unless otherwise speciﬁed.
Exercise 3.2.
Let M be a metric space, and let A ⊂M be any subset.
Show that the subspace topology on A is the same as the metric topology
obtained by restricting the metric of M to points in A.
Example 3.1. Consider the subspaces B
= [0, 1] ∪(2, 3) and C
=
{1/n}∞
n=1 of R (Figure 3.2). Notice that the set [0, 1] is not open in R.
But it is an open subset of B, because [0, 1] is the intersection with B
of the open interval (−1, 2). In C, the one-point sets {1/n} are all open
(why?), so the subspace topology on B is discrete.
These examples illustrate that openness and closedness are not properties
of a set by itself, but rather of a set in relation to a particular topological
space.
An injective continuous map that is a homeomorphism onto its image
(in the subspace topology) is called a topological embedding. If f : A →X
is such a map, we can think of the image set f(A) as a homeomorphic copy
of A embedded in X.

Subspaces
41
Example 3.2. Let a: [0, 1) →R2 be the map a(s) = (cos 2πs, sin 2πs). In
Exercise 2.7, you showed that a is not a homeomorphism onto its image
in the subspace topology (which is the same as the metric topology by
Exercise 3.2), so it is an example of a map that is continuous and injective
but not an embedding. However, the restriction of a to any interval [0, b)
for 0 < b < 1 is an embedding.
The ﬁrst property we will prove about the subspace topology is so fun-
damental that, in a sense we will explain later, it completely characterizes
the subspace topology among all the possible topologies on a subset. For
any subset A ⊂X, ιA : A 	→X denotes the inclusion map of A into X (see
the Appendix).
Theorem 3.3 (Characteristic Property of Subspace Topologies).
Suppose A ⊂X is a subspace. For any topological space Y , a map f : Y →A
is continuous if and only if the following composite map from Y to X is
continuous:
Y
f
−→A
ιA
	→X.
Proof. Directly from the deﬁnitions of continuity and the subspace topol-
ogy,
f : Y →A is continuous
⇐⇒for all U ⊂
openA, f −1(U) ⊂
openY
⇐⇒for all V ⊂
openX, f −1(V ∩A) ⊂
openY
⇐⇒for all V ⊂
openX, (ιA ◦f)−1(V ) ⊂
openY
⇐⇒ιA ◦f : Y →X is continuous.
Proposition 3.4 (Other Properties of the Subspace Topology).
Suppose A is a subspace of the topological space X.
(a) The inclusion map ιA : A 	→X is continuous, and in fact is a topo-
logical embedding.
(b) If f : X →Y is continuous, then its restriction to A is continuous.
(c) If f : X →Y is continuous, then f : X →f(X) is continuous.
(d) The closed subsets of A are precisely the intersections of A with closed
subsets of X.
(e) If B ⊂A is a subspace of A, then B is a subspace of X; in other
words, the subspace topologies that B inherits from A and from X
agree.

42
3. New Spaces from Old
X
B
A
V
U
W
FIGURE 3.3. A subspace of a subspace.
(f ) If B ⊂A ⊂X, B is open in A, and A is open in X, then B is open
in X.
(g) If B is a basis for the topology of X, then
BA = {B ∩A : B ∈B}
is a basis for the topology of A.
(h) Any subspace of a Hausdorﬀspace is Hausdorﬀ.
(i) Any subspace of a second countable space is second countable.
Proof. Part (a) follows immediately from the characteristic property, just
by taking Y to be equal to A and f to be the identity map. Then (b)
follows from (a), since f|A = f ◦ιA. Part (c) follows from the characteristic
property because the hypothesis says that ιf(X) ◦f : X →Y is continuous,
where ιf(X) is the inclusion of f(X) into Y .
For part (e), let U ⊂B be any subset. For the purposes of this proof, we
say U is open in B relative to A if U is open in the subspace topology that
B inherits from A; U is open in B relative to X is deﬁned similarly. Then
we argue as follows (Figure 3.3):

Subspaces
43
X
q
A
V
U
B
FIGURE 3.4. A basis open set for a subspace.
U is open in B relative to A
⇐⇒U = B ∩V for some V ⊂
openA
⇐⇒U = B ∩V, where V = A ∩W, W ⊂
openX
⇐⇒U = B ∩A ∩W for some W ⊂
openX
⇐⇒U = B ∩W for some W ⊂
openX (since B ⊂A)
⇐⇒U is open in B relative to X.
To prove (g), we have to show that every open subset of A satisﬁes the
basis criterion with respect to BA. Let U be an open subset of A, and let
q ∈U. Then by deﬁnition U = A ∩V for some open subset V ⊂X. By
the basis criterion for V , there is an element B ∈B such that q ∈B ⊂V
(Figure 3.4). It then follows that q ∈B ∩A ⊂U with B ∩A ∈BA.
Parts (d), (f), (h), and (i) are left as an exercise.
Exercise 3.3.
Complete the proof of Proposition 3.4.
We can now produce many examples of manifolds as subspaces of Eu-
clidean spaces. In particular, since the Hausdorﬀproperty and second
countability are hereditary by parts (h) and (i) of the preceding propo-
sition, to show that a subspace of Rn is a manifold we need only verify the
locally Euclidean condition.
We begin with a very general construction.
Example 3.5. If U ⊂Rn is an open set and f : U →Rk is any continuous
map, the graph of f (Figure 3.5) is the set

44
3. New Spaces from Old
x2, . . . , xn
x1
y1, . . . , yk
U
Γ(f)
FIGURE 3.5. The graph of a continuous function.
Γ(f) = {(x, y) = (x1, . . . , xn, y1, . . . , yk) ∈Rn+k : x ∈U and y = f(x)}.
To verify that Γ(f) is locally Euclidean, we construct an explicit homeo-
morphism between U and Γ(f). Let Φf : U →Γ(f) be the map
Φf(x) = (x, f(x)).
It is continuous because f is, and it is easily seen that its inverse is the
restriction to Γ(f) of the map π(x, y) = x (the projection onto the ﬁrst
n coordinates), which is continuous by Proposition 3.4(b). Thus Φf is a
topological embedding. In particular, Γ(f) is (globally) homeomorphic to
the open set U ⊂Rn, so it is an n-manifold.
Example 3.6. Our next examples are arguably the most important man-
ifolds of all, so it is worth taking some time to understand them well. The
(unit) n-sphere is the set
Sn = {x ∈Rn+1 : |x| = 1}.

Subspaces
45
In low dimensions, spheres are easy to visualize: S0 is the two-point discrete
space {±1} ⊂R; S1 is the unit circle in the plane; and S2 is the familiar
spherical surface of radius 1 in R3. In the case of the circle, it is often more
convenient to identify the plane R2 with the set C of complex numbers by
the correspondence (x, y) ↔x + iy, and think of the circle as the set of
complex numbers with unit modulus:
S1 = {z ∈C : |z| = 1}.
To see that Sn is a manifold, we need to show that each point has a
Euclidean neighborhood. The most straightforward way is to show that
each point has a neighborhood in which Sn is the graph of a continuous
function. For each i = 1, . . . , n + 1, let U +
i
denote the subset of Rn+1
where xi > 0, and U −
i
the set where xi < 0. If x is any point in Sn, some
coordinate xi must be nonzero there, so the sets U ±
1 , . . . , U ±
n+1 cover a
neighborhood of Sn. On U ±
i , we can solve the equation |x| = 1 for xi and
ﬁnd that x ∈Sn ∩U ±
i
if and only if
xi = ±

1 −(x1)2 −· · · −(xi−1)2 −(xi+1)2 −· · · −(xn+1)2.
In other words, the portion of Sn in U ±
i
is the graph of a continuous
function, and is therefore locally Euclidean. This proves that Sn is an n-
manifold.
Here is another useful way to show that Sn is a manifold. Consider both
Rn and Sn as subsets of Rn+1 (identifying Rn with the set of points whose
xn+1 coordinate is zero), and let N = (0, . . . , 0, 1) denote the “north pole.”
Deﬁne stereographic projection σ : Sn ∖{N} →Rn to be the map given by
σ(x1, . . . , xn+1) = (x1, . . . , xn)
1 −xn+1
.
Geometrically, it sends a point x ∈Sn ∖{N} to the point u ∈Rn where
the line from N to x intersects Rn (Figure 3.6), as you can easily check. It
is a homeomorphism, because it has an inverse given by
σ−1(u1, . . . , un) = (2u1, . . . , 2un, |u|2 −1)
|u|2 + 1
.
Thus Sn ∖{N} is homeomorphic to Rn. In particular, this provides a Eu-
clidean neighborhood of every point of Sn except N, and the analogous
projection from the south pole works in a neighborhood of N.
Example 3.7. Finally, consider the doughnut surface D, which is the sur-
face of revolution in R3 deﬁned by revolving the circle (y −2)2 + z2 = 1
(called the generating circle) around the z-axis (Figure 3.7). It is character-
ized by the equation (r −2)2 + z2 = 1, where r =

x2 + y2. This surface
can be parametrized by two angles θ (measured around the z axis from the

46
3. New Spaces from Old
N
x
u = σ(x)
FIGURE 3.6. Stereographic projection.
xz-plane) and ϕ (measured around the generating circle from the horizon-
tally outward direction). It is more convenient for calculations to make the
substitutions ϕ = 2πu and θ = 2πv, and deﬁne a map F : R2 →D by
F(u, v) = ((2 + cos 2πu) cos 2πv, (2 + cos 2πu) sin 2πv, sin 2πu).
(3.1)
This maps the plane onto D. It is not one-to-one, since F(u + k, v + l) =
F(u, v) for any pair of integers (k, l). However, F is injective if it is restricted
to a small enough neighborhood of any point (u0, v0), and a straightforward
calculation shows that a local inverse in a neighborhood of (u0, v0) can be
constructed from the formulas
u = 1
2π tan−1
z
r −2 + k;
v = 1
2π tan−1 y
x + l;
u = 1
2π cot−1 r −2
z
+ k;
v = 1
2π cot−1 x
y + l
for suitable choices of k, l. Thus D is a 2-manifold.
The next lemma is similar to the local criterion for continuity of Lemma
2.2, in that it asserts the global continuity of a map that is known to be
continuous on certain subsets. In this case, however, the subsets must be
closed, and there can be only ﬁnitely many of them. This lemma will turn
out to be extremely useful in our investigations of surfaces.
Lemma 3.8 (Gluing Lemma).
Let X be a topological space, and sup-
pose X = A1 ∪· · · ∪Ak, where each Ai is closed in X. For each i, let

Subspaces
47
θ
ϕ
x
y
z
FIGURE 3.7. A doughnut surface of revolution.
fi : Ai →Y be a continuous map such that fi|Ai∩Aj = fj|Ai∩Aj. There
exists a unique continuous map f : X →Y such that f|Ai = fi for each i.
Exercise 3.4.
Prove Lemma 3.8.
In choosing a topology for a subset A ⊂X, there are two competing
priorities: We would like the inclusion map A 	→X to be continuous (from
which it follows by composition that the restriction to A of any continuous
map f : X →Y is continuous); and we would also like continuous maps
into X whose images happen to lie in A also to be continuous as maps into
A. For the ﬁrst requirement, A needs to have enough open sets, while for
the second it should not have too many. The subspace topology is chosen
as the optimal compromise between these requirements.
As we will see several times in this chapter, natural topologies like the
subspace topology can usually be characterized in terms of which maps are
continuous with respect to them. This is why the “characteristic property”
of the subspace topology (Theorem 3.3) is so named. The next lemma
makes this precise.
Theorem 3.9 (Uniqueness of the Subspace Topology).
Suppose A
is a subset of a topological space X. The subspace topology on A is the
unique topology for which the characteristic property holds.

48
3. New Spaces from Old
Proof. Suppose we are given an arbitrary topology on A that is known to
satisfy the characteristic property. For this proof, let Ag denote A with
the given topology, and let As denote A with the subspace topology. To
show that the given topology is equal to the subspace topology, it suﬃces
to show that the identity map of A is a homeomorphism between Ag and
As, by Problem 2-1.
First we note that the inclusion map from Ag into X is continuous, as
follows: Since the identity map of any space is continuous, the characteristic
property applied to the composition
Ag
Id
−→Ag 	→X
implies that this composite map is continuous; but this composition is just
the inclusion Ag 	→X itself. Of course, the inclusion map As 	→X is
also continuous, because it is the inclusion map of a subspace (Proposition
3.4(a)).
Now consider the two composite maps
As
Idsg
−→Ag
ιg
	→X,
Ag
Idgs
−→As
ιs
	→X.
Here both Idgs and Idsg represent the identity map of A, and ιs and ιg
represent inclusion of A into X; we decorate them with subscripts only for
the purpose of discussing their continuity.
Note that ιg ◦Idsg = ιs, and ιs ◦Idgs = ιg, both of which we have just
shown to be continuous. Thus, applying the characteristic property to each
of the compositions above, we conclude that both Idsg and its inverse Idgs
are continuous. Therefore, Idsg is a homeomorphism.
Product Spaces
Suppose X1, . . . , Xn are topological spaces. We deﬁne a basis in their Carte-
sian product X1 × · · · × Xn by
B = {U1 × · · · × Un : Ui is open in Xi, i = 1, . . . , n}.
Exercise 3.5.
Prove that B is a basis.
The topology generated by B is called the product topology, and the space
X1×· · ·×Xn with the product topology is called a product space. The basis
open sets of the form U1 × · · · × Un are called product open sets.
For example, in the plane R2 = R×R, the product topology is generated
by sets of the form I × J, where I and J are open sets in R. A typical such
set is an open rectangle.

Product Spaces
49
Exercise 3.6.
Show that the product topology on Rn = R × · · · × R is the
same as the metric topology induced by the Euclidean distance function.
The product topology can also be deﬁned in the more general setting of
inﬁnite products, with a slightly more complicated deﬁnition. We will not
need to use inﬁnite products in this book, but the general deﬁnition of the
product topology is given in Problem 7-12. For more information, consult
[Sie92] or [Mun75].
The characteristic property relates continuity of a map into a product
space to continuity of its component functions. In the special case of a map
from Rn to Rm, this reduces to a familiar result from advanced calculus.
Theorem 3.10 (Characteristic Property of Product Topologies).
Let X1 × · · · × Xn be a product space. For any topological space B, a map
f : B →X1 × · · · × Xn is continuous if and only if each of its component
functions fi = πi ◦f is continuous:
B
Xi.
-
fi
f




X1 × · · · × Xn
?
πi
Proof. Since it suﬃces to check continuity on basis open sets,
f is continuous
⇐⇒f −1(U1 × · · · × Un) ⊂
openB for all Ui ⊂
openXi
⇐⇒f −1
1 (U1) ∩· · · ∩f −1
n (Un) ⊂
openB for all Ui ⊂
openXi.
If each fi is continuous, the set in the last line above is the intersection of
ﬁnitely many open sets and is therefore open in B, which shows that f is
continuous. Conversely, if f is continuous, choose j between 1 and n and
take Ui = Xi for all i except i = j. Then f −1
i
(Ui) = B when i ̸= j, so the
argument above shows that f −1
j
(Uj) is open in B whenever Uj is open in
Xj, or in other words, fj is continuous.
It follows from the characteristic property that if f1, f2 : X →C are
complex-valued continuous functions, then their sum (f1+f2)(x) = f1(x)+
f2(x) is continuous, because it is the composition of the maps f : X →C2
given by f(x) = (f1(x), f2(x)) and s: C2 →C given by s(w, z) = w + z. A
similar remark applies to the product (f1f2)(x) = f1(x)f2(x).
Just as in the case of the subspace topology, the product topology is
uniquely determined by its characteristic property.
Theorem 3.11 (Uniqueness of the Product Topology).
Let
X1,
. . . , Xn be topological spaces. The product topology on X1 ×· · ·×Xn is the
unique topology that satisﬁes the characteristic property.

50
3. New Spaces from Old
Proof. Suppose that X1 × · · · × Xn is endowed with some topology that
satisﬁes the characteristic property. First we note that the projection maps
πi are continuous (in either topology) by the characteristic property applied
to the identity map of X1 × · · · × Xn. Now inserting X1 × · · · × Xn with
the product topology in place of B shows that the identity map from the
product topology to the given topology is continuous, and reversing roles
shows that its inverse is also continuous. Thus the two topologies are equal.
Proposition 3.12 (Other Properties of the Product Topology).
Let X1, . . . , Xn be topological spaces.
(a) The projection maps πi : X1 × · · · × Xn →Xi are all continuous.
(b) The product topology is “associative” in the sense that the three prod-
uct topologies X1 × X2 × X3, (X1 × X2) × X3, and X1 × (X2 × X3)
on the set X1 × X2 × X3 are all equal.
(c) For any i and any points xj ∈Xj, j ̸= i, the map fi : Xi →X1 ×
· · · × Xn given by
fi(x) = (x1, . . . , xi−1, x, xi+1, . . . , xn)
is a topological embedding of Xi into the product space.
(d) If for each i, Bi is a basis for the topology of Xi, then the set
{B1 × · · · × Bn : Bi ∈Bi}
is a basis for the product topology on X1 × · · · × Xn.
(e) If Ai is a subspace of Xi for i = 1, . . . , n, the product topology and
the subspace topology on A1 × · · · × An ⊂X1 × · · · × Xn are equal.
(f ) If each Xi is Hausdorﬀ, so is X1 × · · · × Xn.
(g) If each Xi is second countable, so is X1 × · · · × Xn.
Exercise 3.7.
Prove Proposition 3.12.
If fi : Xi →Yi are maps (continuous or not) for i = 1, . . . , k, their product
map is
f1 × · · · × fk : X1 × · · · × Xk →Y1 × · · · × Yk
given by
f1 × · · · × fk(x1, . . . , xk) = (f1(x1), . . . , fk(xk)).

Product Spaces
51
Proposition 3.13. A product of continuous maps is continuous, and a
product of homeomorphisms is a homeomorphism.
Proof. Because it suﬃces to check that the inverse images of basis open sets
are open, the ﬁrst claim follows from the fact that (f1×· · ·×fk)−1(U1×· · ·×
Uk) is just the product of the open sets f1(U1), . . . , fk(Uk). The second
claim follows from the ﬁrst, because the inverse of a bijective product map
is itself a product map.
Product spaces provide us with another rich source of examples of man-
ifolds. The key is the following proposition.
Proposition 3.14. If M1, . . . , Mk are manifolds of dimensions n1, . . . , nk,
respectively, the product space M1 × · · · × Mk is a manifold of dimension
n1 + · · · + nk.
Proof. Proposition 3.12 shows that the product is Hausdorﬀand second
countable, so only the locally Euclidean property needs to be checked.
Given any point q = (q1, . . . , qk) ∈M1 × · · · × Mk, for each i there exists
a neighborhood Ui of qi and a homeomorphism ϕi from Ui to an open
subset of Rni. By the preceding lemma, the product map ϕ1 × · · · × ϕk is a
homeomorphism from a neighborhood of q to an open set in Rn1+···+nk.
A particularly important example is the product manifold Tn = S1×· · ·×
S1, which is an n-dimensional manifold called the n-torus. In particular,
the 2-torus is usually just called the torus. Because S1 is a subspace of
R2, T2 can be considered as a subspace of R4 by Proposition 3.12(e): It
is just the set of points (x1, x2, x3, x4) ∈R4 such that (x1)2 + (x2)2 = 1
and (x3)2 + (x4)2 = 1. As the next lemma shows, T2 is homeomorphic to
a familiar surface.
Lemma 3.15. The torus T2 is homeomorphic to the doughnut surface D
of Example 3.7.
Proof. The key idea is that both surfaces are parametrized by two angles.
For D, the angles are ϕ = 2πu and θ = 2πv as in (3.1); for T2, they are
the angles in the two circles. Although one must be careful using angle
functions because they cannot be deﬁned continuously on a whole circle,
with some care we can eliminate the angles altogether and come up with
formulas that are manifestly continuous.
With this in mind, we write x1 = cos θ, x2 = sin θ, x3 = cos ϕ, x4 = sin ϕ.
Substituting into (3.1) suggests deﬁning a map G: T2 →D by
G(x1, x2, x3, x4) = ((2 + x3)x1, (2 + x3)x2, x4).
This is obviously continuous, and a little algebra shows that G maps T2
into D. To see that it is a homeomorphism, just check that its inverse is

52
3. New Spaces from Old
given by
G−1(x, y, z) = (x/r, y/r, r −2, z),
where r =

x2 + y2 as in Example 3.7.
Quotient Spaces
Our third technique for constructing new topological spaces from old ones
is somewhat more involved than the preceding two. It is a way to identify
some points in a given topological space with each other, to obtain a new,
smaller space.
Let X be a topological space, Y be any set, and π: X →Y be a surjective
map. Deﬁne a topology on Y by declaring a subset U ⊂Y to be open if and
only if π−1(U) is open in X. This is called the quotient topology induced
by the map π.
Exercise 3.8.
Show that the quotient topology is indeed a topology.
More generally, if X and Y are topological spaces, a map π: X →Y
is called a quotient map if it is surjective and continuous and Y has the
quotient topology induced by π. If π is known to be surjective, this is the
same as saying that U is open in Y if and only if π−1(U) is open in X.
An easy example to keep in mind is the map π: Rn+k →Rn given
by projection onto the ﬁrst n coordinates. It is straightforward to check
directly from the deﬁnition that it is a quotient map.
The most common source of quotient maps is the following construction.
Let ∼be an equivalence relation on a topological space X (see the Ap-
pendix). For each q ∈X let [q] denote the equivalence class of q, and let
X/∼denote the set of equivalence classes: This is a partition of X, which
is a decomposition of X into a collection of disjoint subsets whose union
is X. Let π: X →X/∼be the natural projection sending each element of
X to its equivalence class. Then X/∼together with the quotient topology
determined by π is called the quotient space (or sometimes identiﬁcation
space) of X by the given equivalence relation. The quotient map π is called
the projection.
Alternatively, a quotient space can be deﬁned by explicitly giving a par-
tition of X. Whether a given quotient space is deﬁned in terms of an equiv-
alence relation or a partition is a matter of convenience.
If π: X →Y is a quotient map, a subset U ⊂X is said to be saturated
(with respect to π) if U = π−1(V ) for some subset V ⊂Y . (In fact, you
can check that U is saturated if and only if U = π−1(π(U)).) If Y is a
quotient space determined by an equivalence relation, the saturated sets
are those that are unions of equivalence classes. More generally, for any

Quotient Spaces
53
quotient map π: X →Y , a subset π−1(y) ⊂X for y ∈Y is called a ﬁber
of π; a saturated set is one that is a union of ﬁbers.
Although quotient maps do not always take open sets to open sets, there
is a useful alternative characterization of quotient maps in terms of satu-
rated open sets.
Lemma 3.16. A continuous surjective map π: X →Y is a quotient map
if and only if it takes saturated open sets to open sets, or saturated closed
sets to closed sets.
Exercise 3.9.
Prove Lemma 3.16.
Lemma 3.17. Suppose f : X →Y is a quotient map. The restriction of f
to any saturated open or closed set is a quotient map.
Exercise 3.10.
Prove Lemma 3.17.
It is not always a trivial matter to check that a continuous surjective map
is a quotient map—it may well not be, as the following example shows.
Example 3.18. Consider the map a: [0, 1) →S1 deﬁned (in complex no-
tation) by a(s) = e2πis. It is surjective and continuous, but not a quotient
map, because [0, 1
2) is a saturated open subset of [0, 1) whose image is not
open in S1.
The following lemma gives two very useful suﬃcient conditions for a
surjective continuous map to be a quotient map.
Lemma 3.19. If π: X →Y is a surjective continuous map that is also an
open or closed map, then it is a quotient map.
Proof. If π is open, it takes saturated open sets to open sets (because it
takes all open sets to open sets). If π is closed, it takes saturated closed
sets to closed sets. In either case, it is a quotient map by Lemma 3.16.
One simple property of quotient maps is that they behave well with
respect to composition.
Lemma 3.20 (Composition Property of Quotient Maps).
Sup-
pose π1 : X
→Y
and π2 : Y
→Z are quotient maps. Then their
composition π2 ◦π1 : X →Z is also a quotient map.
Proof. Just note that U ⊂Z is open if and only if π−1
2 (U) is open in Y ,
which is true if and only if π−1
1 (π−1
2 (U)) = (π2 ◦π1)−1(U) is open in X.
As it happens, quotient spaces do not generally behave well with respect
to products, subspaces, bases, or topological properties such as locally Eu-
clidean, Hausdorﬀ, or second countable. In particular, quotient spaces of
manifolds are generally not manifolds. In fact, it is not diﬃcult to construct

54
3. New Spaces from Old
FIGURE 3.8. A quotient of B2.
FIGURE 3.9. A quotient of I × I.
a quotient space of a manifold that satisﬁes all the deﬁnitions of a manifold
except that it is not Hausdorﬀ(see Problem 3-8). Thus if we wish to prove
that a given quotient space is a manifold, we have to prove at least the
locally Euclidean and Hausdorﬀproperties directly.
The following lemma shows that in many cases this is suﬃcient. In par-
ticular, it shows that a quotient of a manifold is again a manifold, provided
that it is locally Euclidean and Hausdorﬀ.
Lemma 3.21. Suppose P is a second countable space and π: P →M is a
quotient map. If M is locally Euclidean, it is second countable.
Proof. Let U be a covering of M by Euclidean balls. The collection
{π−1(U) : U ∈U} is an open cover of P, which has a countable sub-
cover by Lemma 2.15. If we let U′ ⊂U denote a countable subset of U such
that {π−1(U) : U ∈U′} covers P, then U′ is a countable cover of M by
Euclidean balls. Each such ball has a countable basis, and the union of all
these bases is a countable basis for M.
Because quotient spaces are probably less familiar to you than subspaces
or products, we will introduce a number of examples before going any
farther.
Example 3.22. The map α: [0, 1] →S1 given by α(s) = e2πis is a closed
map and therefore a quotient map.
Example 3.23. Let B2 denote the closed unit disk in R2. Let ∼be the
equivalence relation on B2 generated by (x, y) ∼(−x, y) for all (x, y) ∈∂B2
(Figure 3.8). (You can think of this space as being obtained from B2 by
“pasting” the left half of the boundary to the right half.) We will see in
Chapter 6 that B2/∼is homeomorphic to S2.
Example 3.24. Let I = [0, 1] denote the closed unit interval in the real
line; we will generally just call this the unit interval. Deﬁne an equivalence
relation on the square I × I by setting (x, 0) ∼(x, 1) for all x ∈I, and
(0, y) ∼(1, y) for all y ∈I (Figure 3.9). This can be visualized as the
space obtained by gluing the top boundary segment of the square to the

Quotient Spaces
55
FIGURE 3.10. Wedge of two lines.
FIGURE 3.11. Wedge of two circles.
bottom to form a cylinder, and then gluing the left-hand boundary circle
of the resulting cylinder to the right-hand one. Later we will see that the
resulting quotient space is homeomorphic to the torus.
Example 3.25. Let X1, . . . , Xk be topological spaces, and let qi ∈Xi.
The wedge of X1, . . . , Xk (also called their one-point union), written X1 ∨
· · · ∨Xk, is the quotient space obtained from X1 ⨿· · · ⨿Xk by identifying
q1 ∼· · · ∼qk. In other words, we glue the spaces together by identifying
all their distinguished points together. For example, the wedge R ∨R is
homeomorphic to the union of the x-axis and the y-axis in the plane (Figure
3.10), and the wedge S1 ∨S1 is homeomorphic to the ﬁgure eight space E
consisting of the union of the two circles of radius 1 centered at (0, 1) and
(0, −1) in the plane (Figure 3.11). A wedge of ﬁnitely many copies of S1 is
sometimes called a bouquet of circles.
Example 3.26. Deﬁne an equivalence relation on R by declaring x ∼y if
x and y diﬀer by an integer. We will see below that the resulting quotient
space is homeomorphic to the circle.
Example 3.27. Consider the map q: Rn+1 ∖{0} →Sn deﬁned by q(x) =
x/|x|. Observe that q is continuous and surjective, and the ﬁbers of q are
rays in Rn+1 ∖{0}. Thus the saturated sets are the unions of rays, and it is
easy to check that q takes saturated open sets to open sets and is therefore
a quotient map.
Example 3.28. Deﬁne Pn, the real projective space of dimension n, to be
the set of 1-dimensional linear subspaces (lines through the origin) in Rn+1.
There is a natural map π: Rn+1 ∖{0} →Pn deﬁned by sending a point
x to its span. We topologize Pn by giving it the quotient topology with
respect to this map.

56
3. New Spaces from Old
This space can also be viewed in another way. If we deﬁne an equivalence
relation on Rn+1∖{0} by declaring two points x, y to be equivalent if x = λy
for some nonzero real number λ, then there is an obvious identiﬁcation
between Pn and the set of equivalence classes. Under this identiﬁcation,
the map π deﬁned above is just the map sending a point to its equivalence
class.
The Characteristic Property of the Quotient Topology
The characteristic property of the quotient topology is even more important
than those of the subspace or product topologies.
Theorem 3.29 (Characteristic Property of Quotient Topologies).
Let π: X →Y be a quotient map. For any topological space B, a map
f : Y
→B is continuous if and only if the composite map f ◦π is
continuous:
Y
B.
-
f
f ◦π
@
@
@@
R
X
?
π
Proof. If f is continuous, f ◦π is continuous by composition. Conversely, if
f ◦π is continuous and U ⊂B is open, then π−1(f −1(U)) = (f ◦π)−1(U) is
open in X, which implies f −1(U) is open in Y by deﬁnition of the quotient
topology. Thus f is continuous.
The characteristic property has the following extremely important corol-
lary:
Corollary 3.30 (Passing to the Quotient).
Suppose π: X →Y is a
quotient map, B is a topological space, and f : X →B is any continuous
map that is constant on the ﬁbers of π (i.e., if π(p) = π(q), then f(p) =
f(q)). Then there exists a unique continuous map f : Y →B such that
f = f ◦π:
Y
B.
-
f
f
@
@
@@
R
X
?
π
Proof. The existence and uniqueness of f follow from elementary set the-
ory: Given q ∈Y , there is some p ∈X such that π(p) = q, and we can set
f(q) = f(p) for any such p. The hypothesis on f guarantees that f is unique

Quotient Spaces
57
and well-deﬁned. Continuity of f is then immediate from the characteristic
property.
In the situation of the preceding corollary, we say that the map f passes
to the quotient or descends to the quotient.
In the case of quotient spaces, there are two slightly diﬀerent ways of
phrasing the uniqueness associated with the characteristic property. The
ﬁrst one says that the characteristic property uniquely characterizes quo-
tient maps.
Theorem 3.31 (Characterization of Quotient Maps). Let X and Y
be topological spaces, and let π: X →Y be any surjective map. Then π is
a quotient map if and only if the characteristic property holds.
Proof. If π is a quotient map, the characteristic property holds by Theorem
3.29. Conversely, suppose π has the characteristic property. Applying the
characteristic property to the diagram
Y
Y
-
Id
π
@
@
@@
R
X
?
π
shows that π is continuous because the identity is. To show that π is a
quotient map, we will show that Y with the given topology is homeomorphic
to Y with the quotient topology. As before, let Yg and Yq denote Y with
the given and quotient topologies, respectively, and let Idgq, Idqg, πq, and
πg have the obvious meanings. Then the characteristic property applied to
the two diagrams
Yg
Yq
-
Idgq
πq
@
@
@@
R
X
?
πg
Yq
Yg
-
Idqg
πg
@
@
@@
R
X
?
πq
shows that Idqg and Idgq are both continuous, from which the result follows.
The second uniqueness result says that quotient spaces are uniquely de-
termined up to homeomorphism by the identiﬁcations made by their quo-
tient maps.
Corollary 3.32 (Uniqueness of Quotient Spaces).
Suppose
π1 : X
→
Y1 and π2 : X
→
Y2 are quotient maps that make the
same identiﬁcations (i.e., π1(p) = π1(q) if and only if π2(p) = π2(q)).
Then there is a unique homeomorphism ϕ: Y1 →Y2 such that ϕ ◦π1 = π2.

58
3. New Spaces from Old
Proof. By Corollary 3.30, both π1 and π2 pass uniquely to the quotient as
in the following diagrams:
Y1
Y2
-

π2
π2
@
@
@@
R
X
?
π1
Y2
Y1.
-

π1
π1
@
@
@@
R
X
?
π2
Since both diagrams above commute, it follows that 
π1◦(
π2◦π1) = 
π1◦π2 =
π1. Consider another diagram:
Y1
Y1.
-
π1
@
@
@@
R
X
?
π1
If the bottom arrow is interpreted as either 
π1 ◦
π2 or the identity map of
Y1, this diagram will commute; by the uniqueness part of Corollary 3.30,
these maps must be equal. Similarly, 
π2 ◦
π1 is the identity on Y2. Thus
ϕ = 
π2 is the required homeomorphism, and it is the unique such map by
the uniqueness statement of Corollary 3.30.
Group Actions
Our next construction is a far-reaching generalization of Examples 3.26 and
3.28. A topological group is a group G endowed with a topology such that
the maps μ: G × G →G and ι: G →G given by
μ(g1, g2) = g1g2,
ι(g) = g−1
are continuous, where the product and inverse are those of the group struc-
ture of G. A discrete group is a topological group that has the discrete
topology.
Example 3.33. Each of the following is a topological group.
• The real line R with its additive group structure and the Euclidean
topology.
• The set R∗= R ∖{0} of nonzero real numbers under multiplication,
with the subspace topology.
• The set C∗= C ∖{0} of nonzero complex numbers under complex
multiplication, with the subspace topology.

Group Actions
59
• The general linear group GL(n, R), which is the set of n×n invertible
real matrices under matrix multiplication, with the subspace topology
inherited from Rn2.
• Any group with the discrete topology.
Exercise 3.11.
Verify that each of the above examples is a topological
group.
Lemma 3.34. Any subgroup of a topological group is a topological group
with the subspace topology. Any ﬁnite product of topological groups is a
topological group with the direct product group structure and the product
topology.
Exercise 3.12.
Prove Lemma 3.34.
In view of Lemma 3.34, each of the following is a topological group:
• Euclidean space Rn as a group under vector addition.
• The circle S1 ⊂C∗under complex multiplication, with the subspace
topology.
• The n-torus Tn = S1 × · · · × S1 with the direct product group struc-
ture.
• The orthogonal group O(n), which is the subgroup of GL(n, R) con-
sisting of matrices A such that AAt is the identity.
If G is a topological group and g ∈G, the left translation map Lg : G →G
deﬁned by Lg(g′) = gg′ is continuous, because it is the restriction of the
multiplication map to {g} × G. Because Lg ◦Lg−1 = IdG, left translation
by any element of g is a homeomorphism of G. Similarly, right translation
Rg(g′) = g′g is also a homeomorphism.
Suppose G is a group and X is a topological space. A left action of G
on X is a map G × X →X, written (g, x) 
→g · x, with the following
properties:
(i) For any x ∈X and any g1, g2 ∈G, g1 · (g2 · x) = (g1g2) · x.
(ii) For all x ∈X, 1 · x = x.
Similarly, a right action is a map X × G →X, written (x, g) 
→x· g, with
the same properties except that composition works in reverse: (x·g1)·g2 =
x·(g1g2). Any right action determines a left action in a canonical way, and
vice versa, by the correspondence
g · x = x · g−1.

60
3. New Spaces from Old
Thus for many purposes, the choice of left or right action is a matter of
taste. We usually choose to focus on left actions because the composi-
tion law mimics composition of functions, and unless we specify otherwise,
groups will always be understood to act on the left. However, we will see
some situations in which an action appears naturally as a right action.
If G is a topological group, an action of G on a space X is said to be
continuous if the map G×X →X is continuous. This means, in particular,
that for each g ∈G the map x 
→g·x is continuous from X to itself, because
it is the restriction of the action to the subspace {g}×X ⊂G×X. In fact,
each such map is a homeomorphism, because the deﬁnition of a group
action guarantees that it has a continuous inverse x 
→g−1 · x. When G
is discrete, it is easy to check that the action is continuous if and only if
x 
→g · x is continuous for each g ∈G.
For any x ∈X, the set G · x = {g · x : g ∈G} is called the orbit of x.
The action is said to be transitive if for every pair of points x, y ∈X, there
is a group element g such that g · x = y or equivalently if the only orbit is
the entire space X. It is said to be free if the only element of G that has
any ﬁxed points is the identity, i.e., g · x = x for some x implies g = 1.
Example 3.35 (Continuous Group Actions).
(a) The general linear group GL(n, R) acts continuously on the left on Rn
by matrix multiplication, each vector in Rn considered as a column
matrix. Because any nonzero vector in Rn can be taken to any other
by a linear transformation, there are only two orbits: Rn ∖{0} and
{0}.
(b) The orthogonal group O(n) acts continuously on Rn by matrix mul-
tiplication as well; this is just the restriction of the action in part
(a) to O(n) × Rn ⊂GL(n, R) × Rn. Since orthogonal transformations
preserve lengths of vectors, and any vector can be taken to any other
of the same length by an orthogonal transformation, the orbits are
{0} and the spheres centered at 0.
(c) The restriction of the action of O(n) to the unit sphere in Rn yields
a transitive action on Sn−1.
(d) The group R∗acts on Rn ∖{0} by scalar multiplication. The action
is free, and the orbits are the lines through the origin (with the origin
removed).
(e) Any topological group G acts freely and transitively on itself on the
left by left translation: g · g′ = Lg(g′) = gg′. Similarly, G acts on
itself on the right by right translation.
Given an action of G on a space X, we deﬁne an equivalence relation on
X by setting x1 ∼x2 if there is an element g ∈G such that g · x1 = x2.

Group Actions
61
The equivalence classes are precisely the orbits of the group action. The
resulting quotient space is denoted by X/G, and is called the orbit space
of the action. If the action is transitive, the orbit space is a single point, so
only nontransitive actions yield interesting examples.
Exercise 3.13.
Verify that the real projective space Pn of Example 3.28
is the orbit space of the action of R∗on Rn+1 ∖{0} by scalar multiplication.
A particularly important special case arises when we consider a subgroup
Γ of a topological group G (with the subspace topology). Group multipli-
cation on the left or right deﬁnes a left or right action of Γ on G; it is just
the restriction of the action of G on itself to Γ × G or G × Γ. This action
is continuous and free, but in general not transitive. An orbit of the right
action of Γ on G is a set of the form {gγ : γ ∈Γ}, which is precisely the
left coset gΓ. Thus the orbit space of the right action of Γ on G is the set
G/Γ of left cosets with the quotient topology. This quotient space is called
the (left) coset space of G by Γ. (It is unfortunate but unavoidable that the
right action produces a left coset space and vice versa. If G is abelian, the
situation is simpler, because then the left action and right action of Γ are
equal to each other.)
Example 3.36. As an application, let us consider the coset space R/Z.
Because Z (with the discrete topology) is a subgroup of the topological
group R, there is a natural free continuous action of Z on R by translation:
n · x = n + x. (Because R is abelian, we might as well consider it as a
left action.) The orbits are exactly the equivalence classes of the relation
deﬁned in Example 3.26 above, x ∼y if and only if x −y ∈Z. Thus the
quotient space of that example is the same as the coset space R/Z.
Consider also the map ε: R →S1 deﬁned by
ε(s) = e2πis.
It is straightforward to check that this is a local homeomorphism and thus
an open map, so it is a quotient map. Because it makes the same identiﬁ-
cations as the quotient map R →R/Z, the uniqueness of quotient spaces
tells us that R/Z is homeomorphic to S1. (We will be returning to this map
ε, which we call the exponential quotient map, extensively in this book.)
More generally, the discrete subgroup Zn acts freely on Rn by translation.
By similar reasoning, the quotient space Rn/Zn is homeomorphic to the
n-torus Tn = S1 × · · · × S1.
We will see more examples of this technique in the next few chapters.

62
3. New Spaces from Old
Problems
3-1. Show that a ﬁnite product of open maps is open, and a ﬁnite product
of closed maps is closed.
3-2. By considering the space X = [0, 1] ⊂R, and the sets A0 = {0},
Ai = [1/(i + 1), 1/i] for i = 1, 2, . . . , show that the gluing lemma
(Lemma 3.8) is false if {A1, . . . , Ak} is replaced by an inﬁnite sequence
of closed sets.
3-3. Formulate a “characteristic property” for the disjoint union topology
(Problem 2-9) and prove that the disjoint union topology is uniquely
characterized by it.
3-4. Use stereographic projection to show that any closed ball in Rn is an
n-dimensional manifold with boundary.
3-5. Let X be a topological space. The diagonal of X × X is the subset
Δ = {(x, x) : x ∈X} ⊂X ×X. Show that X is Hausdorﬀif and only
if Δ is closed in X × X.
3-6. If X1, . . . , Xk are topological spaces, show that the projections
πi : X1 × · · · × Xk →Xi are quotient maps.
3-7. Let M = Rd × R, where Rd is the set R with the discrete topology.
(a) Show that M is homeomorphic to the space X of Problem 2-5.
(b) Show that M is locally Euclidean (of what dimension?) and
Hausdorﬀ, but not second countable.
3-8. Let X be the subset R × {0} ∪R × {1} of R2. Deﬁne an equivalence
relation on X by declaring (x, 0) ∼(x, 1) if x ̸= 0. Show that the
quotient space X/∼is locally Euclidean and second countable, but
not Hausdorﬀ. (This space is called the line with two origins.)
3-9. Lemma 3.17 showed that the restriction of a quotient map to a satu-
rated open set is still a quotient map. Show that the “saturated”
hypothesis is necessary, by giving an example of a quotient map
f : X →Y and an open subset U ⊂X such that f|U is surjective but
not a quotient map.
3-10. Show that real projective space Pn is an n-manifold. [Hint: Consider
the subsets Ui ⊂Rn+1 where xi = 1.]
3-11. Let CPn denote the set of all 1-dimensional complex subspaces of
Cn+1, called n-dimensional complex projective space. Topologize CPn
as the quotient Cn+1 ∖{0}/C∗, where C∗is the group of nonzero
complex numbers acting by scalar multiplication. Show that CPn is
a 2n-manifold. [Hint: Mimic what you did in Problem 3-10.]

Problems
63
3-12. Let G be a topological group and let H ⊂G be a subgroup. Show
that H is also a subgroup.
3-13. If G is a group that is also a topological space, show that G is a
topological group if and only if the map G×G →G given by (x, y) 
→
xy−1 is continuous.
3-14. Let G be a topological group and Γ ⊂G be a subgroup.
(a) For any g ∈G, show that left translation Lg : G →G passes
to the quotient G/Γ and deﬁnes a homeomorphism of G/Γ with
itself.
(b) A topological space X is said to be homogeneous if for any x, y ∈
X, there is a homeomorphism ϕ: X →X taking x to y. Show
that every coset space is homogeneous.
3-15. Let G be a topological group acting continuously on a topological
space X.
(a) Show that the quotient map π: X →X/G is open.
(b) Show that X/G is Hausdorﬀif and only if the orbit relation
{(x1, x2) ∈X × X : x2 = g · x1 for some g ∈G}
is closed in X × X.
3-16. If Γ is a normal subgroup of the topological group G, show that the
coset space G/Γ is a topological group. [Hint: It might be helpful to
use Problems 3-1 and 3-15(a).]

4
[[Connectedness]] and Compactness
In this chapter we treat two topological properties that will be of central
importance in our study of manifolds: connectedness and compactness.
The deﬁnition of connectedness is formulated so that connected spaces
will behave similarly to intervals in the real line, so, for example, a contin-
uous real-valued function on a connected space satisﬁes the intermediate
value theorem. Similarly, compactness is deﬁned so that compact spaces
will have many of the same properties enjoyed by closed and bounded sub-
sets of Euclidean spaces. In particular, continuous real-valued functions on
compact sets always achieve their maxima and minima.
[[Connectedness]]
One of the most important elementary facts about continuous functions is
the intermediate value theorem: If f is a continuous real-valued function
deﬁned on a closed bounded interval [a, b], then f takes on every value be-
tween f(a) and f(b). The key idea here is the “connectedness” of intervals.
In this section we generalize this concept to topological spaces.
Deﬁnitions and Basic Properties
If X is a topological space, a separation of X is a pair of nonempty, disjoint,
open subsets U, V ⊂X such that X = U ∪V . We say that X is disconnected
if there exists a separation of X, and connected otherwise.

66
4. [[Connectedness]] and Compactness
FIGURE 4.1. Union of two disks.
FIGURE 4.2. The x-axis minus 0.
By this deﬁnition, connectedness is a property of a space, not a property
of subsets like openness or closedness. We can also talk about connected
subsets of a topological space, by which we always mean connected in the
subspace topology. In this context we can also consider a separation of A
to be a pair of open subsets U, V ⊂X whose intersections with A are
nonempty and disjoint, and whose union contains A: This is equivalent to
the original deﬁnition because the open subsets of A are exactly the open
subsets of X intersected with A.
Example 4.1. Each of the following subspaces of the plane is discon-
nected.
(a) X is the union of the two disjoint closed disks B1(2, 0) and B1(−2, 0)
(Figure 4.1). Each of the disks is open in X, so the pair of disks is a
separation of X.
(b) Y is the x-axis minus the origin (Figure 4.2). The two sets {(x, 0) :
x > 0} and {(x, 0) : x < 0} separate Y .
(c) Z is the set of points with rational coordinates. A separation is given
by, say, {(x, y) : x < π} and {(x, y) : x > π}.
On the other hand, it is intuitively clear that the open and closed unit
disks, the circle, the whole plane, and the x-axis are all connected, at least
in the everyday sense of the word. Proving it, however, is not so easy,
because we would have to show that it is impossible to ﬁnd a separation.
We will soon come up with an easy technique for proving connectedness
that will work in most practical cases, including that of manifolds.
Here is a useful alternative characterization of connectedness.
Proposition 4.2. A space X is connected if and only if the only subsets
of X that are both open and closed in X are ∅and X itself.
Proof. Suppose ﬁrst that X is connected, and assume that U ⊂X is open
and closed. Then V = X ∖U is also open and closed. If both U and V were
nonempty, then {U, V } would be a separation of X; therefore, either V is
empty, which means that U = X, or U is empty.

[[Connectedness]]
67
Conversely, if X is disconnected, we can write X = U ∪V where U and
V are nonempty, open, and disjoint. This implies that U is open, closed,
not empty, and not equal to X.
The most important feature of connectedness is that continuous images
of connected sets are connected.
Theorem 4.3 (Main Theorem on [[Connectedness]]).
Let
X, Y
be
topological spaces and let f : X →Y be a continuous map. If X is con-
nected, then f(X) is connected.
Proof. Suppose f(X) is not connected. Then there exist open sets U, V ⊂
Y whose intersections with f(X) are nonempty and disjoint and whose
union contains f(X). It follows immediately that {f −1(U), f −1(V )} is a
separation of X, so X is not connected.
Proposition 4.4 (Properties of Connected Sets).
(a) Suppose X is any space and U, V are disjoint open subsets of X. If
A is a connected subset of X contained in U ∪V , then either A ⊂U
or A ⊂V .
(b) Suppose X is any space and A ⊂X is connected. Then A is connected.
(c) Let X be a space, and let {Bα}α∈A be any collection of connected
subspaces with a point in common. Then 
α∈A Bα is connected.
(d) Any product of ﬁnitely many connected spaces is connected.
(e) Any quotient space of a connected space is connected.
Proof. For part (a), if A contained points in both U and V , then {A ∩
U, A ∩V } would be a separation of A.
To prove part (b), suppose U and V are disjoint open subsets of X that
separate A. By (a), A is contained in one of the sets, say A ⊂U. Each
point of V has a neighborhood (namely V ) disjoint from A, so every point
of V is exterior to A. Therefore, A ⊂U, which means that A ∩V = ∅, a
contradiction.
For part (c), let q be a point contained in each Bα, and suppose {U, V }
is a separation of 
α∈A Bα. Suppose without loss of generality that q lies
in U. By part (a), each Bα must be entirely contained in U, and thus so is
their union.
For part (d), since X1×· · ·×Xk = (X1×· · ·×Xk−1)×Xk, by induction it
suﬃces to consider a product of two spaces. Thus let X and Y be connected,
and suppose {U, V } is a separation of X×Y . Choose any point (x0, y0) ∈U.
The set {x0} × Y is connected because it is homeomorphic to Y ; since it
contains the point (x0, y0) ∈U, it must be entirely contained in U by part
(a). For each y ∈Y , the set X × {y} is also connected and has a point

68
4. [[Connectedness]] and Compactness
U
V
a
b
c
FIGURE 4.3. Proof that an interval is connected.
(x0, y) ∈U, so it must also be contained in U. Since the sets X × {y}
exhaust X × Y , the result follows.
Finally, (e) follows from Theorem 4.3 and the fact that quotient maps
are surjective.
Although this proposition gives us a number of ways of building new
connected spaces out of given ones, so far we have no examples of spaces
to start with that are known to be connected (except a one-point space,
which does not carry us very far). The one example of a space that can
be shown to be connected by “brute force” is the one that enters into the
proof of the intermediate value theorem: an interval in the real line (see
the Appendix).
Proposition 4.5. A nonempty subset of R is connected if and only if it is
an interval.
Proof. First assume that J ⊂R is an interval. If it is not connected, there
are open subsets U, V ⊂R that separate J. Choose a ∈U ∩J, b ∈V ∩J,
and assume (interchanging U and V if necessary) that a < b (Figure 4.3).
Then [a, b] ⊂J because J is an interval. Since U and V are both open in
R, there exists ε > 0 such that [a, a + ε) ⊂U ∩J and (b −ε, b] ⊂V ∩J.
Let c = sup(U ∩[a, b]). By our choice of ε, a+ε ≤c ≤b−ε. In particular,
c is between a and b, so c ∈J ⊂U ∪V . But if c were in U, it would have
a neighborhood (c −δ, c + δ) ⊂U, which would contradict the deﬁnition of
c. Similarly, c ∈V leads to a contradiction. Therefore, J is connected.
Conversely, assume that J is not an interval. This means that there exist
a < c < b with a, b ∈J but c ̸∈J. Then the sets (−∞, c) and (c, ∞)
separate J, so J is not connected.
An immediate consequence of this proposition is the following generalized
intermediate value theorem.
Theorem 4.6 (Intermediate Value Theorem).
Suppose X is a con-
nected topological space, and f is a continuous real-valued function on X.
If p, q ∈X, then f takes on all values between f(p) and f(q).
Proof. The image set f(X) is connected, so it must be an interval.

[[Connectedness]]
69
Path [[Connectedness]]
Now we can give a simple but powerful suﬃcient condition for connected-
ness, based on the following deﬁnitions. Let X be a topological space and
p, q ∈X. A path in X from p to q is a continuous map f : [0, 1] →X such
that f(0) = p and f(1) = q. We say that X is path connected if for every
p, q ∈X, there is a path in X from p to q.
Theorem 4.7. Path connectedness implies connectedness.
Proof. Suppose that X is path connected but not connected, and let {U, V }
be a separation of X. We can choose p ∈U and q ∈V (since neither set is
empty), and ﬁnd a path f from p to q in X. Then f −1(U) and f −1(V ) are
disjoint open subsets of [0, 1] that cover [0, 1]; moreover, 0 ∈f −1(U) and
1 ∈f −1(V ), so neither set is empty. This implies that [0, 1] is disconnected,
which is a contradiction.
Example 4.8. The following spaces are all easily shown to be path con-
nected, and therefore they are connected.
(a) Rn.
(b) Any subset B ⊂Rn that is convex, which means that for any x, x′ ∈
B, the line segment from x to x′ lies entirely in B.
(c) Rn ∖{0} for n ≥2.
Example 4.9. The following spaces are also connected.
(a) Sn for n ≥1, because it is a quotient space of Rn+1 ∖{0} by Example
3.27.
(b) The n-torus Tn, because it is a product of connected spaces.
On the other hand, path connectedness is stronger in general than con-
nectedness. Here is an example of a space that is connected but not path
connected.
Example 4.10. Deﬁne subsets of the plane by
A = {(x, y) : x = 0 and y ∈[−1, 1]};
B = {(x, y) : y = sin(1/x) and x ∈(0, 1]}.
Let X = A ∪B (Figure 4.4). X is called the topologist’s sine curve. In
Problem 4-5 you will show that it is connected but not path connected.

70
4. [[Connectedness]] and Compactness
B
A
FIGURE 4.4. The topologists’s sine curve.
Components and Path Components
Look back at Example 4.1. Our ﬁrst example of a disconnected set, the
union of two disjoint closed disks, could be separated in only one way,
because any other separation would induce a separation of one of the closed
disks, which is path connected. The same reasoning applies to the second
example, the x-axis minus the origin. The set of rational points in the
plane, however, admits inﬁnitely many possible separations. Identifying the
possible separations of a space amounts to ﬁnding “maximal” connected
subsets, a concept we now explore more fully.
Let X be a topological space. Deﬁne a relation on X, called the connec-
tivity relation, by saying that p ∼q if there exists a connected subset of X
containing both p and q.
Lemma 4.11. The connectivity relation is an equivalence relation.
Proof. It is reﬂexive because {q} is a connected subset containing q, and
symmetric because p ∼q and q ∼p both mean that there is a connected
subset containing p and q. To prove transitivity, suppose p ∼q and q ∼r,
which means that there are connected subsets A containing {p, q} and B
containing {q, r}. Since A and B have the point q in common, A ∪B is
connected by Proposition 4.4(c). Thus A ∪B is a connected set containing
{p, r}, so p ∼r.
The equivalence classes in X under the connectivity relation are called
the components of X.

[[Connectedness]]
71
Lemma 4.12. The components of X are exactly the maximal connected
subsets of X, that is, connected sets that are not contained in any larger
connected set.
Proof. Given q ∈X, let A be the component of X containing q, and let B
be the union of all connected sets containing q. Then B itself is connected
by Proposition 4.4(c), and is thus a maximal connected subset. If p ∈B,
then p, q lie in the connected subset B, so p ∼q and thus p ∈A. Conversely,
if p ∈A, then p ∼q, so p lies in some connected subset containing q. Since
B is the union of all such subsets, p ∈B.
Example 4.13. Consider the disconnected subsets of Example 4.1.
(a) The components of X (the union of two disjoint closed disks) are the
two disks themselves.
(b) The components of Y (the x-axis minus the origin) are the positive
x-axis and the negative x-axis.
(c) In the set Z of points with rational coordinates, if p and q are distinct
points of Z, they must diﬀer in one of their coordinates, say their
x-coordinates. Choosing an irrational number α between the two x-
coordinates, the sets where x < α and x > α give a separation of Z
in which p and q lie in diﬀerent subsets. Therefore, p and q cannot
both be contained in any connected subset, so p is not equivalent to
q. Thus the components of Z are the one-point subsets.
Proposition 4.14 (Properties of Components).
Let X be any space.
(a) Each component of X is closed in X.
(b) Any connected subset of X is contained in a single component.
Proof. If B is any component of X, it follows from Proposition 4.4(b)
that B is a connected set containing B. Since components are maximal
connected sets, B = B, so B is closed.
Suppose A ⊂X is connected. Since the components cover X, A has a
point in common with some component B. By Proposition 4.4(c) A ∪B is
connected, so by maximality of B, it must be equal to B. This means that
A ⊂B.
Although components are always closed, they may not be open in general,
so they do not necessarily separate the space. Consider the set Z of rational
points in the plane, for example: Its components are single points, which
are not open sets.
We can also apply the construction used to deﬁne components with path
connectedness in place of connectedness. Deﬁne the path connectivity rela-
tion for points p, q in a space X by saying p ∼
p q if there is a path in X
from p to q.

72
4. [[Connectedness]] and Compactness
Exercise 4.1.
Show that ∼
p is an equivalence relation.
The equivalence classes under ∼
p are called the path components of X.
Proposition 4.15 (Properties of Path Components).
Let X be any
space.
(a) Each path component is contained in a single component, and each
component is a disjoint union of path components.
(b) If A ⊂X is path connected, then A is contained in a single path
component.
Exercise 4.2.
Prove Proposition 4.15.
We say that a space X is locally connected if it admits a basis of connected
open sets, and locally path connected if it admits a basis of path connected
open sets. To put it more concretely, for any p ∈X and any neighborhood
U of p, p has a (path) connected neighborhood contained in U. Clearly,
any locally path connected space is locally connected.
A space can be connected but not locally connected, as is, for example,
the topologist’s sine curve (see Problem 4-5); and it can be locally connected
but not connected, as is the disjoint union of two closed disks.
Lemma 4.16. Let X be any space.
(a) If X is locally connected, then each component of X is open.
(b) If X is locally path connected, then each path component of X is
open, its path components are the same as its components, and it is
connected if and only if it is path connected.
Proof. First assume that X is locally connected, and let A be a component
of X. If p ∈A, then p has a connected neighborhood U by local connect-
edness, and this neighborhood must lie entirely in A by Lemma 4.14(b).
Thus every point of A has a neighborhood in A; in other words, A is open.
Now assume that X is locally path connected. The same argument, with
“connected” replaced by “path connected,” shows that each path compo-
nent is open. Let q ∈X, and let A be the component containing q, and
B the path component. By Proposition 4.15(a), we know that B ⊂A and
A can be written as a disjoint union of path components, each of which is
open in X and thus in A. If B is not the only path component in A, then
the pair {B, A ∖B} is a separation of A, which is a contradiction because
A is connected. This proves that A = B. Finally, X being connected means
it has only one component, which by the above argument is the same as
having only one path component, which in turn is equivalent to being path
connected.

Compactness
73
Proposition 4.17. Every manifold is locally path connected.
Exercise 4.3.
Prove Proposition 4.17.
This proposition means that in our work with manifolds we can use
connectedness and path connectedness interchangeably. This will simplify
many arguments because path connectedness is so much easier to check.
Compactness
Another fundamental fact about continuous functions is the extreme value
theorem (Theorem A.10 in the Appendix): A continuous real-valued func-
tion on a closed, bounded subset of Rn attains its maximum and minimum
values.
This theorem, of course, fails in general for metric spaces, and “bounded”
does not even make sense in topological spaces. But the essential property of
closed and bounded subsets of Rn that makes the proof work, compactness,
makes sense in arbitrary topological spaces. This property is the subject of
the rest of this chapter.
Deﬁnitions and Basic Properties
Recall that an open cover of a space X is a collection U of open subsets of
X whose union is X, and a subcover of U is a subcollection of U that still
covers X. A topological space X is said to be compact if every open cover
of X has a ﬁnite subcover; or in other words, if given any open cover U of
X, there are ﬁnitely many sets U1, . . . , Uk ∈U such that X = U1 ∪· · ·∪Uk.
As in the case of connectedness, when we say that a subset A of a topo-
logical space X is compact, we always mean with respect to the subspace
topology unless otherwise speciﬁed. A subspace A ⊂X is compact if and
only if given any collection of open subsets of X whose union contains A
(which we also call an open cover of A), there is a ﬁnite subcover.
The most important fact about compact spaces is that continuous images
of compact spaces are compact.
Theorem 4.18 (Main Theorem on Compactness).
Let
X, Y
be
topological spaces and let f : X →Y be a continuous map. If X is compact,
then f(X) is compact.
Proof. Let U be an open cover of f(X). (As noted in the remark above,
we can take the elements of U either to be open subsets of f(X) in the
subspace topology, or to be open subsets of Y whose union contains f(X).)
For each U ∈U, f −1(U) is an open subset of X. Since U covers f(X), every
point of X is in some set f −1(U), so the collection {f −1(U) : U ∈U} is an
open cover of X. By compactness of X, some ﬁnite number of these, say

74
4. [[Connectedness]] and Compactness
Up1
Up2
q
Vp1
Vp2
p1
p2
A
V
U
FIGURE 4.5. The case B = {q}.
{f −1(U1), . . . , f −1(Uk)}, cover X. Then it follows that {U1, . . . , Uk} cover
f(X).
Proposition 4.19 (Properties of Compact Spaces).
(a) Every closed subset of a compact space is compact.
(b) In a Hausdorﬀspace X, compact sets can be separated by open sets.
That is, if A, B ⊂X are disjoint compact subsets, there exist disjoint
open sets U, V ⊂X such that A ⊂U and B ⊂V .
(c) Every compact subset of a Hausdorﬀspace is closed.
(d) Every ﬁnite product of compact spaces is compact.
(e) Every quotient of a compact space is compact.
Proof. For part (a), let U be a cover of A by open subsets of X.
Then U ∪{X ∖A} is an open cover of X, which has a ﬁnite subcover
{U1, . . . , Uk, X ∖A}. Therefore, A must be covered by the ﬁnite collection
{U1, . . . , Uk}.
To prove (b), ﬁrst consider the case in which B = {q} is a one-point
set. For each p ∈A, there exist disjoint open sets Up containing p and Vp
containing q by the Hausdorﬀproperty. The collection {Up : p ∈A} is an
open cover of A, so it has a ﬁnite subcover: Call it {Up1, . . . , Upk} (Figure
4.5). Let U = Up1 ∪· · · ∪Upk and V = Vp1 ∩· · · ∩Vpk. Then U and V are
disjoint open sets with A ⊂U and {q} ⊂V, so this case is proved.
Next consider the case of a general compact subset B. The argument
above shows that for each q ∈B there exist disjoint open subsets Uq, Vq ⊂
X such that A ⊂Uq and q ∈Vq. By compactness of B, ﬁnitely many of
these, say {Vq1, . . . , Vqm}, cover B. Then setting U = Uq1 ∩· · · ∩Uqm and
V = Vq1 ∪· · · ∪Vqm proves the result.

Compactness
75
x
U1
U2
U3
X
Y
FIGURE 4.6. Finding a ﬁnite cover of the strip Zx × Y .
For (c), suppose X is Hausdorﬀand A ⊂X is compact. For any point
q ∈X ∖A, by part (b) there exist disjoint open sets U containing A and
V containing q. In particular, V is a neighborhood of q disjoint from A, so
every such q is exterior to A. This means that A is closed.
To prove (d), it suﬃces by induction to consider a product X ×Y of two
compact spaces. Let U be an open cover of X × Y . Choose any x ∈X.
The “slice” {x} × Y is homeomorphic to Y , so ﬁnitely many of the sets
of U cover it, say U1, . . . , Uk (Figure 4.6). Because product open sets are
a basis for the product topology, for each y ∈Y there is a product open
set V × W ⊂X × Y such that (x, y) ∈V × W ⊂U1 ∪· · · ∪Uk. Finitely
many of these product sets cover {x} × Y , say V1 × W1, . . . , Vm × Wm. If
we set Zx = V1 ∩· · · ∩Vm, then it is evident that the whole “strip” Zx × Y
is actually contained in U1 ∪· · · ∪Uk.
Thus we have shown the following: For each x ∈X, there exists an open
subset Zx ⊂X such that Zx×Y is covered by ﬁnitely many of the sets in U.
The collection {Zx : x ∈X} is an open cover of X, which by compactness
has a ﬁnite subcover, say {Zx1, . . . , Zxk}. Since ﬁnitely many sets of U cover
each strip Zxi ×Y , and ﬁnitely many such strips cover X ×Y , we are done.
Finally, part (e) is immediate from Theorem 4.18, since a quotient of a
compact space is the image of a compact space by a continuous map.
Part (d) is actually true in the more general context of inﬁnite products
(see [Sie92] or [Mun75]); in its general form, it is known as Tychonoﬀ’s
theorem.

76
4. [[Connectedness]] and Compactness
Exercise 4.4.
Let X be a compact space, and suppose {Fn} is a countable
collection of nonempty closed subsets of X that are nested, which means that
Fn ⊃Fn+1 for each n. Show that 	
n Fn is nonempty.
One of the main applications of compactness is the following generaliza-
tion of the extreme value theorem of elementary calculus.
Theorem 4.20 (Extreme Value Theorem).
If X is a compact space
and f : X →R is continuous, then f is bounded and attains its maximum
and minimum values on X.
Proof. By the main theorem on compactness, f(X) is a compact subset of
R, so by Proposition A.6 it is closed and bounded. In particular, it contains
its supremum and inﬁmum.
The next lemma expresses an important property of compact metric
spaces, which we will use frequently later in the book. Recall that the di-
ameter of a set S in a metric space is deﬁned to be diam(S) = sup{d(x, y) :
x, y ∈S}. If U is an open cover of a metric space, a number δ > 0 is called
a Lebesgue number for the cover if any set whose diameter is less than δ is
contained in one of the sets U ∈U.
Lemma 4.21 (Lebesgue Number Lemma).
Any open cover of a
compact metric space has a Lebesgue number.
Proof. Let U be an open cover of the compact metric space M. Each point
x ∈M is in some set U ∈U. Since U is open, there is some r(x) > 0 such
that B2r(x)(x) ⊂U. The balls {Br(x)(x) : x ∈M} form an open cover of
M, so ﬁnitely many of them, say Br(x1)(x1), . . . , Br(xn)(xn), cover M.
We will show that δ = min{r(x1), . . . , r(xn)} is a Lebesgue number for U.
To see why, suppose S ⊂M is a nonempty set whose diameter is less than
δ. Let y be any point of S; then there is some xi such that y ∈Br(xi)(xi)
(Figure 4.7). It suﬃces to show that any other point of S is in B2r(xi)(xi),
since the latter set is by construction contained in some U ∈U. If z ∈S,
the triangle inequality gives
d(z, xi) ≤d(z, y) + d(y, xi) < δ + r(xi) ≤2r(xi),
which proves the claim.
Sequential and Limit Point Compactness
The deﬁnition of compactness in terms of open covers lends itself to sim-
ple proofs of some rather powerful theorems, but it does not convey much
intuitive content. There are two other properties that are equivalent to
compactness for manifolds and metric spaces (though not for arbitrary
topological spaces), and that give a more vivid picture of what compact-
ness really means. A space X is said to be limit point compact if every

Compactness
77
2r(xi)
r(xi)
xi
S
U
y
z
FIGURE 4.7. Proof of the Lebesgue number lemma.
inﬁnite subset of X has a limit point in X, and sequentially compact if
every sequence of points in X has a subsequence that converges to a point
in X.
Proposition 4.22. Compactness implies limit point compactness.
Proof. Suppose X is compact, and let S ⊂X be an inﬁnite subset. If S
has no limit point, then every point x ∈X has a neighborhood U such that
U ∩S is either empty or {x}. Finitely many of these neighborhoods cover
X. But since each such neighborhood contains at most one point of S, this
implies that S is ﬁnite, which is a contradiction.
Problem 4-7 shows that the converse of this proposition is not true in
general.
Lemma 4.23. For ﬁrst countable Hausdorﬀspaces, limit point compact-
ness implies sequential compactness.
Proof. Suppose X is ﬁrst countable, Hausdorﬀ, and limit point compact,
and let {pn} be any sequence of points in X. If the sequence takes on only
ﬁnitely many values, then it has a constant subsequence, which is certainly
convergent. So we may suppose it takes on inﬁnitely many values.
By hypothesis the set of values {pn} has a limit point q ∈X. If q is
actually equal to pn for inﬁnitely many values of n, again there is a constant
subsequence and we are done; so by discarding ﬁnitely many terms at the
beginning of the sequence if necessary we may assume pn ̸= q for all n. First
countability of X means that there is a countable neighborhood basis at q,
say {Bn : n = 1, 2, . . . }. By replacing Bn with B1 ∩· · · ∩Bn if necessary,
we may assume that the neighborhood basis is nested: B1 ⊃B2 ⊃· · · . For

78
4. [[Connectedness]] and Compactness
such a neighborhood basis, it is easy to see that any subsequence {pni}
such that pni ∈Bi converges to q.
Since q is a limit point, we can choose n1 such that pn1 ∈B1. Suppose
by induction that we have chosen n1 < n2 < · · · < nk with pni ∈Bi. By
the Hausdorﬀproperty, q has a neighborhood U disjoint from the ﬁnite set
{pn : 1 ≤n ≤nk}, and by deﬁnition of limit point there is some nk+1
(necessarily greater than nk) such that pnk+1 ∈U ∩Bk+1. This completes
the induction, and proves that there is a subsequence {pni} converging to
q.
The next result shows that for manifolds and most of the other spaces we
will be considering in this book, we can use all three notions of compactness
interchangeably.
Proposition 4.24. For metric spaces and second countable Hausdorﬀ
spaces, compactness, limit point compactness, and sequential compactness
are all equivalent.
Proof. We have shown that compactness implies limit point compactness
for all spaces, and limit point compactness implies sequential compactness
for ﬁrst countable Hausdorﬀspaces, which include both metric spaces and
second countable Hausdorﬀspaces. So it remains to show that a metric
space or second countable Hausdorﬀspace that is sequentially compact is
actually compact.
Suppose ﬁrst that X is second countable and sequentially compact. (For
this part we do not need the Hausdorﬀproperty.) Any open cover U of
X has a countable subcover {Un : n = 1, 2, . . . } by Lemma 2.15. Suppose
that no ﬁnite subcollection of Un’s covers X. This means that for each
n there exists qn ∈X such that qn ̸∈U1 ∪· · · ∪Un. By hypothesis, the
sequence {qn} has a convergent subsequence qnk →q. Now, q ∈Um for
some m because the Un’s cover X, and then convergence of the subsequence
means that there exists some N such that qnk ∈Um whenever k ≥N.
But by construction, qnk ̸∈U1 ∪· · · ∪Um as soon as nk ≥m, which
is a contradiction. This proves that ﬁnitely many of the Un’s cover X.
Therefore, second countable sequentially compact spaces are compact.
Finally, let M be a sequentially compact metric space. We will show
that M is second countable, which by the above argument implies that M
is compact. From Problem 2-15, it suﬃces to show that M has a countable
dense subset.
The key idea is to show ﬁrst that sequential compactness implies the
following weak form of compactness for metric spaces: For each ε > 0, the
open cover of M consisting of all ε-balls has a ﬁnite subcover. Suppose this
is not true for some ε. Construct a sequence as follows. Let q1 ∈M be
arbitrary. Since Bε(q1) ̸= M, there is a point q2 ̸∈Bε(q1). Similarly, since
Bε(q1) ∪Bε(q2) ̸= M, there is a point q3 in neither of the two preceding
ε-balls. Proceeding by induction, we construct a sequence {qn} such that

Compactness
79
for each n,
qn+1 ̸∈Bε(q1) ∪· · · ∪Bε(qn).
(4.1)
Replacing this sequence by a convergent subsequence (which still satisﬁes
(4.1)), we can assume qn →q ∈M. Since convergent sequences are Cauchy,
as soon as n is large enough we have d(qn+1, qn) < ε, which contradicts
(4.1).
Now, for each n let q(n)
1
, . . . , q(n)
kn be ﬁnitely many points such that the
balls of radius 1/n around these points cover M. The collection of points
{q(n)
i
} is countable, and is easily seen to be dense. This shows that M is
second countable and completes the proof.
Exercise 4.5.
Show that every compact metric space is complete.
The Closed Map Lemma
The next lemma, though simple, is among the most useful results in this
entire chapter.
Lemma 4.25 (Closed Map Lemma).
Suppose F is a continuous map
from a compact space to a Hausdorﬀspace.
(a) F is a closed map.
(b) If F is surjective, it is a quotient map.
(c) If F is injective, it is a topological embedding.
(d) If F is bijective, it is a homeomorphism.
Proof. Let F : X →Y be such a map. If A ⊂X is closed, it is com-
pact, since any closed subset of a compact space is compact (Proposition
4.19(a)). Therefore, F(A) is compact by the main theorem on compact-
ness, and closed in Y because compact subsets of Hausdorﬀspaces are
closed (Proposition 4.19(c)). This shows that F is a closed map. If in addi-
tion F is surjective, it is a quotient map by Lemma 3.19. If it is bijective,
the fact that it is closed implies that its inverse is continuous, so it is a
homeomorphism (Exercise 2.14). Finally, if F is injective, it is bijective
onto its image, so the fact that it is an embedding follows from (d).
Here are some immediate applications of the closed map lemma.
In Example 3.24 we constructed a quotient space of the square I × I
by gluing the side boundary segments together and the top and bottom
boundary segments together, and we claimed that it was homeomorphic to
the torus. Here is a proof. Construct another map q: I ×I →T2 by setting
q(u, v) = (cos 2πu, sin 2πu, cos 2πv, sin 2πv). By the closed map lemma, this
is a quotient map. Since it makes the same identiﬁcations as the quotient

80
4. [[Connectedness]] and Compactness
map we started with, the original quotient of I × I must be homeomorphic
to the torus by the uniqueness of quotient spaces.
In Lemma 3.15 we showed that the doughnut surface is homeomorphic to
the torus by a rather laborious explicit computation. Now that lemma can
be proved much more simply, as follows. Consider the map F : R2 →R3
deﬁned in Example 3.7. The restriction of this map to I × I is a quotient
map by the closed map lemma. Since it makes the same identiﬁcations
as the map q in the preceding paragraph, the two quotient spaces D and
S1 × S1 are homeomorphic. (The homeomorphism is the map that sends
q(u, v) to F(u, v).)
Another application of the closed map lemma is the following useful
result. You should notice how the closed map lemma, invoked twice in the
proof, allows us to avoid ever having to prove continuity directly by ε-δ
estimates.
Proposition 4.26. Let K
be a compact convex subset of Rn
with
nonempty interior. Then K is homeomorphic to the closed unit ball Bn,
by a homeomorphism that sends Sn−1 to ∂K.
Proof. Let q be an interior point of K. By replacing K with its image
under the translation x 
→x −q (which is a homeomorphism of Rn with
itself), we can assume 0 ∈Int K. Then there is some ε > 0 such that the
ball Bε(0) is contained in K; using the dilation x 
→x/ε, we can assume
Bn = B1(0) ⊂K.
The core of the proof is the following claim: Each ray starting at the origin
intersects ∂K in exactly one point. Since K is compact, its intersection with
each closed ray is compact; thus there is a point x0 in this intersection at
which the distance to the origin assumes its maximum. This point is easily
seen to lie in the boundary of K. To see that there can be only one such
point, we will show that the line segment from 0 to x0 consists entirely
of interior points of K, except for x0 itself. Since B1(0) ⊂K, every line
segment from x0 to a point y ∈B1(0) is contained in K. As y ranges over
B1(0), these line segments sweep out a set C shaped like an ice cream cone
(Figure 4.8). Around each point λx0 for 0 ≤λ < 1, it is easy to check that
there is a ball of radius 1 −λ contained in C and hence in K. Thus x0 is
the only boundary point of K on the ray.
Now we deﬁne a map f : ∂K →Sn−1 by
f(x) = x
|x|.
In words, f(x) is the point where the line segment from the origin to x
intersects the sphere. Since f is the restriction of a continuous map, it is
continuous, and the discussion in the preceding paragraph shows that it is
bijective. Since ∂K is compact, f is a homeomorphism by the closed map
lemma.

Locally Compact HausdorﬀSpaces
81
x0
λx0
0
K
C
FIGURE 4.8. Proof that there is only one boundary point on a ray.
Finally, deﬁne F : Bn →K by
F(x) = |x|f −1
 x
|x|

.
Then F is continuous because f −1 is. Geometrically, F takes each radial
line segment from 0 to a point ω ∈Sn linearly onto the radial segment
from 0 to the point f −1(ω) ∈∂K. By convexity, F takes its values in
K. The map F is injective, since points on distinct rays are mapped to
distinct rays, and each radial segment is mapped linearly to its image. It is
surjective because each point y ∈K is on some ray from 0. By the closed
map lemma, F is a homeomorphism.
Locally Compact HausdorﬀSpaces
Compact Hausdorﬀspaces have many of the familiar properties of sub-
sets of Euclidean spaces. However, while all manifolds are Hausdorﬀ, many
interesting manifolds are not compact. Nonetheless, many of the nice prop-
erties of compact Hausdorﬀspaces carry over to a more general class of
spaces, which we now deﬁne.
A topological space X is said to be locally compact if for every q ∈X there
is a compact subset of X containing a neighborhood of q. In this generality,
the deﬁnition is not particularly useful, and does not seem parallel to other

82
4. [[Connectedness]] and Compactness
deﬁnitions of what it means for a topological space to possess a property
“locally,” which usually entails the existence of a basis of open sets with a
particular property. But when combined with the Hausdorﬀproperty, local
compactness is much more useful. A subset A of a topological space X is
said to be precompact or relatively compact if A is compact.
Proposition 4.27. Let X be a Hausdorﬀspace. The following are equiv-
alent.
(a) X is locally compact.
(b) Each point of X has a precompact neighborhood.
(c) X has a basis of precompact open sets.
Proof. Clearly, (c) =⇒(b) =⇒(a), so all we have to prove is (a) =⇒
(c). It suﬃces to show that if X is locally compact Hausdorﬀ, then each
point x ∈X has a neighborhood basis of precompact open sets. Let K ⊂X
be a compact set containing a neighborhood U of x. The collection V of all
neighborhoods of x contained in U is clearly a neighborhood basis at x.
Because X is Hausdorﬀ, K is closed in X. If V ∈V, then V ⊂K (because
V ⊂U ⊂K and K is closed), and therefore V is compact (because a closed
subset of a compact set is compact). Thus V is the required neighborhood
basis.
Lemma 4.28 (Shrinking Lemma).
Let X be a locally compact Haus-
dorﬀspace. If x ∈X and U is any neighborhood of x, there exists a pre-
compact neighborhood V of x such that V ⊂U.
Proof. Suppose x ∈X and U is a neighborhood of x. If W is any precom-
pact neighborhood of x, then W ∖U is closed in W and therefore compact.
Because open sets separate compact sets in a Hausdorﬀspace, there are
disjoint open sets Y containing x and Y ′ containing W ∖U (Figure 4.9).
Let V = Y ∩W. Because V ⊂W, V is compact. Because V ⊂Y , which
is disjoint from Y ′, we have V ⊂W ∖Y ′. Now the fact that W ∖U ⊂Y ′
means that W ∖Y ′ ⊂U, so V ⊂U.
Lemma 4.29. Any open or closed subset of a locally compact Hausdorﬀ
space is locally compact Hausdorﬀ.
Proof. Let X be a locally compact Hausdorﬀspace. Note that any subspace
of X is Hausdorﬀ, so only local compactness needs to be checked. If Y ⊂X
is open, the shrinking lemma says that any point in Y has a neighborhood
whose closure is compact and contained in Y , so Y is locally compact.
Suppose Z ⊂X is closed. Any x ∈Z has a precompact neighborhood U
in X. Since U ∩Z = U ∩Z is a closed subset of the compact set U, it
is compact, so U ∩Z is a precompact neighborhood of x in Z. Thus Z is
locally compact.

Locally Compact HausdorﬀSpaces
83
x
Y
Y ′
W
U
FIGURE 4.9. Proof of the shrinking lemma.
Exercise 4.6.
Show that any ﬁnite product of locally compact Hausdorﬀ
spaces is locally compact Hausdorﬀ.
Example 4.30 (Locally Compact HausdorﬀSpaces).
(a) Euclidean space Rn is locally compact Hausdorﬀ, because any closed
ball Bε(x) is a precompact neighborhood of x. Thus every open or
closed subset of Rn is locally compact Hausdorﬀ.
(b) Let M be a manifold, and let U be a cover of M by Euclidean balls.
Each U ∈U has a basis of open sets that are precompact in U and
thus also in M, and the union of all such bases is a basis for M. Thus
any manifold is locally compact Hausdorﬀ.
The last example shows that every manifold has a basis of precompact
open sets. For later use, we will need the following reﬁnement of that fact.
Let M be an n-manifold. A Euclidean ball B ⊂M is called regular if it has
the following properties:
(i) There is a Euclidean ball B′ ⊂M containing B.
(ii) For some r > 0, there is a chart ϕ: B′ →B2r(0) ⊂Rn that sends B
onto Br(0).
Lemma 4.31. Every manifold has a countable basis of regular Euclidean
balls.
Proof. Let M be an n-manifold. Every point of M is contained in a Eu-
clidean neighborhood, and since M is second countable, a countable col-
lection U = {Ui : i ∈N} of such neighborhoods covers M by Lemma 2.15.
For each of these open sets Ui, choose a homeomorphism ϕi from Ui to an
open set Ui ⊂Rn.
Now let B be the collection of all open subsets of M of the form
ϕ−1
i (Br(x)), where x ∈Ui is a point with rational coordinates and r is

84
4. [[Connectedness]] and Compactness
ϕi
Ui
q
V
Ui
ϕi(q)
x
r 2r
3r
M
FIGURE 4.10. Showing that the collection B is a basis.
any positive rational number such that B2r(x) ⊂Ui. Since there are only
countably many such balls for each Ui, the collection B is countable. For
any such set B = ϕ−1
i (Br(x)) ∈B, let B′ = ϕ−1
i (B2r(x)). To show that B
is a regular ball, we need to show that B ⊂B′ and ϕi(B) = Br(x). We will
show, equivalently, that ϕ−1
i (Br(x)) = B. Now, ϕ−1
i (Br(x)) is compact and
therefore closed in M (because M is Hausdorﬀ), so B ⊂ϕ−1
i (Br(x)) ⊂B′.
This means that the closure of B in M is equal to its closure in B′, which
is ϕ−1
i (Br(x)), since ϕi is a homeomorphism.
To show that the collection B is a basis, it suﬃces to show that each
open subset of M satisﬁes the basis criterion with respect to it. Let V ⊂M
be any open subset and q ∈V . Then q ∈Ui for some i, and ϕi(V ∩Ui) is an
open subset of Ui containing ϕi(q) (Figure 4.10). Choose a rational number
r > 0 small enough that B3r(ϕi(q)) ⊂ϕi(V ∩Ui), and then choose a point
x ∈ϕi(V ∩Ui) with rational coordinates such that |x −ϕi(q)| < r. Then
ϕi(q) ∈Br(x), and it follows from the triangle inequality that B2r(x) ⊂
ϕi(V ∩Ui). Therefore, B = ϕ−1
i (Br(x)) is in B, contains q, and is contained
in V , thus completing the proof.
The closed map lemma is powerful, but it applies only when the domain
is compact. The following proposition provides a useful generalization of
the closed map lemma to noncompact spaces. A continuous map is said to
be proper if the inverse image of each compact subset of Y is compact.
Proposition 4.32. Suppose f : X →Y is a continuous map between lo-
cally compact Hausdorﬀspaces. If f is proper, it is a closed map.

Locally Compact HausdorﬀSpaces
85
Proof. Let K ⊂X be a closed set. We will show that f(K) contains all of
its boundary points, which means that it is closed in Y .
If y ∈Y is a boundary point of f(K), let U be a precompact neigh-
borhood of y. An easy veriﬁcation shows that y is also a boundary point
of f(K) ∩U. Because f is proper, f −1(U) is compact, which implies that
K ∩f −1(U) is compact. By continuity, f(K ∩f −1(U)) = f(K) ∩U is com-
pact and therefore closed in Y . In particular, y ∈f(K) ∩U ⊂f(K), so
f(K) is closed.
Theorem 4.33 (Baire Category Theorem).
In a locally compact
Hausdorﬀspace or a complete metric space, any countable collection of
dense open subsets has dense intersection.
Proof. Suppose {Vn}n∈N is a countable collection of dense open subsets of
such a space X. We need to show that if U ⊂X is a nonempty open subset,
the intersection of U with 	
n Vn is nonempty.
First consider the case in which X is locally compact Hausdorﬀ. Since V1
is dense, U ∩V1 is nonempty, so by the shrinking lemma there is a nonempty
precompact open set W1 such that W 1 ⊂U ∩V1. Similarly, there is a
nonempty precompact open set W2 such that W 2 ⊂W1 ∩V2 ⊂U ∩V1 ∩V2.
Continuing by induction, we obtain a sequence of nested nonempty compact
sets W 1 ⊃W 2 ⊃· · · ⊃W n ⊃· · · such that W n ⊂U ∩V1 ∩· · · ∩Vn. By
Exercise 4.4, there is a point x ∈	
n W n, which is clearly in U ∩	
n Vn as
well.
In the case that X is a complete metric space, we modify the above
proof as follows. At the inductive step, since Wn−1 ∩Vn is open and
nonempty, there is some ball Bεn(xn) contained in the intersection. Choos-
ing rn < min(εn, 1/n), we obtain a sequence of nested closed balls such
that Brn(xn) ⊂U ∩V1 ∩· · · ∩Vn. Because rn →0, the centers {xn} form
a Cauchy sequence, which converges to a point x ∈U ∩	
n Vn.
The Baire category theorem has a useful complementary reformulation.
A subset F of a topological space X is said to be nowhere dense if its
closure contains no nonempty open set.
Corollary 4.34. In a locally compact Hausdorﬀspace or a complete met-
ric space, any countable collection of nowhere dense sets has empty interior.
Proof. Let X be such a space, and let {Fn} be a countable collection of
nowhere dense subsets of X. Replacing each Fn by its closure, we may
assume that the sets are closed. Then their complements Un are open and
dense, so by the Baire category theorem 	
n Un is dense. It follows that

n Fn = X ∖	
n Un cannot contain any nonempty open set.
For example, it is easy to show that the solution set to any polynomial
equation in two variables is nowhere dense in R2. Since there are only

86
4. [[Connectedness]] and Compactness
countably many polynomials with rational coeﬃcients, this corollary im-
plies that there are points in the plane (a dense set of them, in fact) that
satisfy no rational polynomial equation.
The name of the theorem derives from the (astonishingly unedifying)
terminology used by Baire: He deﬁned a set of the ﬁrst category to be a
countable union of nowhere dense sets, and a set of the second category to
be any set that is not of the ﬁrst category. The theorem proved by Baire
was that for spaces satisfying the hypothesis, every open set is of the second
category. Although the category terminology is mostly ignored nowadays,
the name of the theorem has stuck.
As we mentioned in Chapter 3, quotient maps do not generally behave
well with respect to products. In particular, it is not always true that the
product of two quotient maps is again a quotient map. However, it turns
out that the product of a quotient map with the identity map of a locally
compact Hausdorﬀspace is indeed a quotient map, as the next lemma
shows. This will be used in Chapter 7; the proof is rather technical and can
safely be skipped on ﬁrst reading.
Lemma 4.35. Suppose π: X →Y is a quotient map and K is a locally
compact Hausdorﬀspace. The map π × Id: X × K →Y × K is a quotient
map.
Proof. We need to show that π × Id takes saturated open sets in X ×
K to open sets in Y × K. Let U ⊂X × K be a saturated open set.
Given (x0, k0) ∈U, we will show that (x0, k0) has a saturated product
neighborhood W ×J contained in U. It then follows that π(W)×J contains
(π(x0), k0), is contained in π ×Id(U), and is open (since π(W) is the image
of a saturated open set under the quotient map π). Thus π × Id(U) is open
in Y × K.
Now we proceed to prove the existence of the desired saturated prod-
uct neighborhood. For any subset W ⊂X, we deﬁne its saturation to be
Sat(W) = π−1(π(W)); it is the smallest saturated subset containing W.
By deﬁnition of the product topology, (x0, k0) has a product neighbor-
hood W0×J0 ⊂U. By the shrinking lemma, there is a precompact neighbor-
hood J of k0 such that J ⊂J0, and thus (x0, k0) ∈W0 × J ⊂W0 × J0 ⊂U
(Figure 4.11). Because U is saturated, it follows that Sat(W0) × J ⊂U.
Now, Sat(W0)×J is a saturated subset of X ×K, but not necessarily open
(since π may not be an open map).
We will show that there exists an open set W1 ⊂X containing Sat(W0)
such that W1 × J ⊂U. To prove this, ﬁx some x ∈Sat(W0). For any
k ∈J, (x, k) has a product neighborhood in U. Finitely many of these
cover the compact set {x} × J; call them V1 × J1, . . . , Vm × Jm. If we set
Vx = V1 ∩· · ·∩Vm, then Vx is a neighborhood of {x} such that Vx ×J ⊂U.
Taking W1 to be the union of all such sets Vx for x ∈Sat(W0) proves the
claim.

Locally Compact HausdorﬀSpaces
87
U
K
J
X
W0
(x0, k0)
x
Sat(W0)
W1
FIGURE 4.11. Finding a saturated product neighborhood.
Repeating this construction, we obtain a sequence of open sets Wi ⊂X
such that
W0 ⊂Sat(W0) ⊂W1 ⊂Sat(W1) ⊂· · ·
and Wi × J ⊂U. Let W be the union of all the Wi’s. Then W is open
because it is a union of open sets, and W × J ⊂U. Moreover, W × J is
saturated: If (x, k) ∈W × J, then x is in some Wi; and if (x′, k) is any
point in the same ﬁber, then x′ ∈Wi+1, so (x′, k) ∈W × J as well. Thus
W × J is the required saturated product neighborhood of (x0, k0).

88
4. [[Connectedness]] and Compactness
Problems
4-1.
(a) If U is any open subset of R and x ∈U, show that U ∖{x} is
disconnected.
(b) Show that a topological space cannot be both a 1-manifold and
an n-manifold for any n > 1.
4-2. Show that the union of the x-axis and the y-axis in R2 is not a
manifold in the subspace topology.
4-3. Show that any n-manifold is a disjoint union of countably many con-
nected n-manifolds.
4-4. Suppose f : X →Y is a surjective local homeomorphism. If X is
locally connected, locally path connected, or locally compact, show
that Y has the same property.
4-5. Let X be the topologist’s sine curve (Example 4.10).
(a) Show that X is connected but not path connected or locally
connected.
(b) Determine the components and the path components of X.
4-6. Like Problem 3-7, this problem constructs a space that is locally Eu-
clidean and Hausdorﬀbut not second countable. Unlike that example,
however, this one is connected.
(a) Recall that a totally ordered set is said to be well-ordered if every
nonempty subset has a smallest element (see the Appendix).
Show that the well-ordering theorem (Theorem A.2) implies that
there exists an uncountable well-ordered set Y such that for
every p ∈Y , there are only countably many q < p. [Hint: Let X
be any uncountable well-ordered set. If X does not satisfy the
desired condition, let Y be an appropriate subset of X.]
(b) Now let
L =

Y × [0, 1)

∖{(a0, 0)},
where a0 is the smallest element of Y . We give L the dictionary
order: This means that (p, q) < (r, s) if either p < r, or p = r
and q < s. With the order topology, L is called the long line.
Show that L is locally Euclidean and Hausdorﬀbut not second
countable.
(c) Show that L is path connected.
4-7. Deﬁne a topology on Z by declaring a set A to be open if and only
if n ∈A implies −n ∈A. Show that Z with this topology is second
countable and limit point compact but not compact.

Problems
89
4-8. Let V be a ﬁnite-dimensional real vector space. A norm on V is a
real-valued function on V , written v 
→|v|, satisfying
• Positivity: |v| ≥0, and |v| = 0 if and only if v = 0.
• Homogeneity: |cv| = |c| |v| for any c ∈R and v ∈V .
• Triangle inequality: |v + w| ≤|v| + |w|.
A norm determines a metric by d(v, w) = |v−w|. Show that all norms
determine the same topology on V . [Hint: Consider the restriction of
the norm to the unit sphere.]
4-9. Suppose K and L are compact convex sets in Rn, both with nonempty
interior. Show that any continuous map f : ∂K →∂L has a continu-
ous extension to a map F : K →L. If f is a homeomorphism, show
that F can be chosen to be a homeomorphism also.
4-10. Let X be a noncompact, locally compact Hausdorﬀspace. The one-
point compactiﬁcation of X is the topological space X∗deﬁned as
follows. Let ∞be some object not in X, and let X∗= X ⨿{∞} with
the following topology:
T = {open subsets of X}
∪{U ⊂X∗: X∗∖U is a compact subset of X}.
(a) Show that T is a topology.
(b) Show that X∗is a compact Hausdorﬀspace.
(c) Show that X is open and dense in X∗and has the subspace
topology.
4-11. If X and Y are noncompact, locally compact Hausdorﬀspaces, show
that a continuous map f : X →Y extends to a continuous map
f ∗: X∗→Y ∗if and only if it is proper.
4-12. Let σ : Sn ∖{N} →Rn be stereographic projection, as deﬁned in
Example 3.6. Show that σ extends to a homeomorphism of Sn with
the one-point compactiﬁcation of Rn.
4-13. If M is a noncompact n-manifold, show that its one-point compact-
iﬁcation is an n-manifold if and only if there exists a precompact
open subset U ⊂M such that M ∖U is homeomorphic to Rn ∖Bn.
[Hint: You may ﬁnd the inversion map I : Rn ∖Bn →Bn deﬁned by
I(x) = x/|x|2 useful.]
4-14. Suppose M is a 1-dimensional manifold with boundary. Show that
the interior and boundary of M are disjoint. Use this to conclude
that M is a manifold if and only if ∂M = ∅.

5
Simplicial Complexes
In this chapter we give a brief introduction to simplicial complexes. These
are spaces constructed from building blocks called simplices, which are
points, line segments, ﬁlled-in triangles, solid tetrahedra, and their higher-
dimensional analogues. They provide a highly useful way of constructing
topological spaces, and play a fundamental role in geometry and algebraic
topology.
As we did with manifolds, we will deﬁne simplicial complexes in two
stages, starting with a very concrete version and proceeding to the most
general deﬁnition. Concretely, we think of a simplicial complex as a col-
lection of simplices in some Euclidean space that overlap “nicely.” More
abstractly, a simplicial complex is an abstract “vertex scheme,” specify-
ing which sets of vertices are supposed to span simplices. We will see that
any abstract simplicial complex determines a topological space, called a
polyhedron, in a natural way.
Then we apply these ideas to manifolds by asking which manifolds are
homeomorphic to polyhedra. Any such homeomorphism is called a trian-
gulation of the manifold, and any manifold that admits such a homeomor-
phism is said to be triangulable. We will give a complete proof that every
1-manifold is triangulable, and will give a brief sketch of the proof for 2-
manifolds. These results will be used in the next chapter as stepping stones
toward classifying curves and surfaces up to homeomorphism.
At the end of the chapter we explore two combinatorial properties of sim-
plicial complexes that are important in the study of manifolds. The ﬁrst
is the concept of an orientation of a complex, which generalizes and sys-
tematizes the intuitive notions of “direction” in 1-dimensional complexes,

92
5. Simplicial Complexes
FIGURE 5.1. Simplices.
“clockwise” and “counterclockwise” in 2-dimensional ones, and “handed-
ness” in 3-dimensional ones. The second is the Euler characteristic, which
is the alternating sum of the numbers of simplices in diﬀerent dimensions,
and generalizes Euler’s classical formula for compact convex polyhedra in
R3.
Euclidean Simplicial Complexes
We begin with a little linear algebra. An aﬃne map between vector spaces
is a map f : V →W of the form f(x) = a(x) + b, where a is a linear map
and b ∈W. An aﬃne subspace of a vector space is the zero set of some aﬃne
map: {x : a(x) + b = 0}. Its dimension is the dimension of the kernel of the
linear part of the aﬃne map. The special case of an aﬃne subspace of V
whose dimension is one less than that of V is called an aﬃne hyperplane in
V . Elementary linear algebra shows that if n ≥k, any k+1 points v0, . . . , vk
in Rn are contained in some k-dimensional aﬃne subspace (just choose a
linear map a: Rn →Rn−k whose kernel contains {v1 −v0, . . . , vk −v0} and
let b = −a(v0)). We say that k + 1 points are in general position if they are
not contained in any (k −1)-dimensional aﬃne subspace, or equivalently if
{v1 −v0, . . . , vk −v0} are linearly independent.
Given points v0, . . . , vk in general position in Rn, the simplex (plural:
simplices) spanned by them is the set of all points in Rn of the form
k

i=0
tivi,
where 0 ≤ti ≤1 and
k

i=0
ti = 1,
(5.1)
with the subspace topology. Each of the points vi is called a vertex of the
simplex. We will sometimes use the notation ⟨v0, . . . , vk⟩to denote the
simplex spanned by v0, . . . , vk. The integer k (one less than the number of
vertices) is called its dimension, and a k-dimensional simplex is often called
a k-simplex. A 0-simplex is a single point, a 1-simplex is a line segment,
a 2-simplex is a (ﬁlled-in) triangle, and a 3-simplex is a solid tetrahedron
(Figure 5.1).
For any subset A ⊂Rn, the convex hull of A is deﬁned to be the inter-
section of all convex sets containing A. It is immediate that the convex hull
is itself a convex set, in fact, the smallest convex set containing A.

Euclidean Simplicial Complexes
93
Lemma 5.1. A simplex is the convex hull of its vertices.
Exercise 5.1.
Prove Lemma 5.1.
Let σ be a simplex. Each simplex spanned by a nonempty subset of the
vertices is called a face of σ. The faces that are not equal to σ itself are
called its proper faces. The 0-dimensional faces of σ are just its vertices,
and the 1-dimensional faces are called its edges. The (k −1)-dimensional
faces of a k-simplex are sometimes called its boundary faces.
A map f : σ →τ between simplices is called a simplicial map if it is the
restriction of an aﬃne map that takes vertices of σ to vertices of τ. As the
next exercise shows, simplicial maps between a given pair of simplices are
in one-to-one correspondence with maps between their vertices.
Exercise 5.2.
(a) Show that given any map f0 from the set of vertices of σ to the set
of vertices of τ, there is a unique simplicial map f : σ →τ whose
restriction to the vertices of σ is f0.
(b) Show that any two k-simplices are homeomorphic by a simplicial home-
omorphism.
(c) Show that every k-simplex is homeomorphic to Bk. [Hint: Work with
a particular simplex in Rk and use Proposition 4.26.]
It follows from part (c) of the preceding exercise that a k-simplex is a
k-dimensional manifold with boundary. Thus we deﬁne the boundary of a
simplex to be the union of its boundary faces (which is the same as the
union of all of its proper faces), and its interior to be the simplex minus
its boundary. The interior of a k-simplex is sometimes called an open k-
simplex; it is the set of points of the form  tivi where {v0, . . . , vk} are the
vertices of σ and none of the coeﬃcients ti are zero. For example, if σ is a
0-simplex, Int σ = σ, and if σ is a 1-simplex, Int σ is σ minus its vertices.
Note that an open simplex is generally not an open subset of Rn, and the
interior and boundary of σ as a simplex may not be equal to its topological
interior and boundary as a subset of Rn.
A Euclidean simplicial complex is a collection K of simplices in some
Euclidean space Rn satisfying the following conditions:
(i) If σ ∈K, then every face of σ is in K.
(ii) The intersection of any two simplices in K is either empty or a face
of each.
(iii) Local Finiteness: Every point in a simplex of K has a neighbor-
hood that intersects at most ﬁnitely many simplices of K.

94
5. Simplicial Complexes
FIGURE 5.2. A complex in R2.
FIGURE 5.3. Not a complex.
The dimension of K is deﬁned to be the maximum dimension of any simplex
in K (which is well-deﬁned, since simplices in Rn have dimension at most
n). Figure 5.2 shows an example of a 2-dimensional simplicial complex in
R2. The set of simplices shown in Figure 5.3 is not a simplicial complex,
because the intersection condition is violated.
Given a Euclidean complex K, the union of all the simplices in K, with
the subspace topology inherited from Rn, is a topological space denoted by
|K| and called the (Euclidean) polyhedron of K.
Many of the spaces we have seen so far are homeomorphic to Euclidean
polyhedra. Here are some simple examples.
Example 5.2 (Euclidean Polyhedra).
(a) Any n-simplex together with its faces is a simplicial complex whose
polyhedron is homeomorphic to Bn.
(b) The proper faces of an n-simplex constitute an (n −1)-dimensional
complex whose polyhedron is homeomorphic to Sn−1.
(c) The set of all unit-length intervals [n, n + 1] ⊂R for n ∈Z, together
with their endpoints, is a simplicial complex whose polyhedron is R.
(d) For any integer m ≥3, let Pm be a regular m-sided polygon in the
plane. The set of edges and vertices of Pm is a simplicial complex
whose polyhedron is homeomorphic to S1.
Example 5.3. The set of closed line segments in the plane from the origin
to the points (1, 1/n) for n ∈N, together with their vertices (Figure 5.3),
is not a simplicial complex, because the local ﬁniteness condition fails at
the origin.
Exercise 5.3.
Prove the claims made in the two preceding examples.
You might wonder why we should focus on building spaces out of sim-
plices, and not out of cubes or some other sort of geometric object. The
simple answer is that simplicial complexes are the most general: It is not
hard to show that a locally ﬁnite “polyhedral complex” (under any reason-
able deﬁnition) can be subdivided to form a simplicial complex.

Euclidean Simplicial Complexes
95
FIGURE 5.4. Failure of local ﬁniteness.
Let K be a Euclidean simplicial complex. Any subset K′ ⊂K that is
itself a simplicial complex is called a subcomplex of K. It is clear that the
only condition that needs to be checked is that the faces of each simplex
in K′ are in K′. In particular, for any nonnegative integer k, the subset
K(k) ⊂K consisting of all simplices of dimension less than or equal to k is
a subcomplex, called the k-skeleton of K.
Let K and L be two Euclidean simplicial complexes. A continuous map
f : |K| →|L| whose restriction to each simplex of K is a simplicial map
to a simplex of L is called a simplicial map, and is denoted by f : K →L.
The restriction of f to K(0) is called the vertex map of f.
Exercise 5.4.
Let K and L be Euclidean simplicial complexes.
(a) Let f0 : K(0) →L(0) be any map with the property that whenever
{v0, . . . , vk} are the vertices of a simplex of K, {f0(v0), . . . , f0(vk)} are
the vertices of a simplex of L (possibly with repetitions). Show that
there is a unique simplicial map f : K →L whose vertex map is f0.
(b) Now let f0 be as in (a), and assume in addition that f0 is bijective
and {v0, . . . , vk} are the vertices of a simplex of K if and only if
{f0(v0), . . . , f0(vk)} are the vertices of a simplex of L. Show that |K|
and |L| are homeomorphic by a simplicial map.
All the considerations of this section carry over without change if we
replace Rn by an arbitrary ﬁnite-dimensional vector space V . We give V
the metric topology induced by any norm; Problem 4-8 shows that the
resulting topology is independent of the norm. The only properties of Rn
that we use are its vector space structure and its topology, and since any
choice of basis gives a linear homeomorphism of V with Rn, all the results
of this section are true with Rn replaced by V . We will use this slightly
more general setting in the next section.

96
5. Simplicial Complexes
Abstract Simplicial Complexes
Just as it is too restrictive to deﬁne manifolds to be subsets of Euclidean
spaces, Euclidean simplicial complexes are not suﬃciently general for many
important applications. In this section we will deﬁne a more general kind
of simplicial complex. The key idea is already implicit in Exercise 5.4(b),
which says that a simplicial complex is completely determined, up to simpli-
cial homeomorphism, by knowledge of which sets of vertices span simplices.
Motivated by this observation, we deﬁne an abstract simplicial complex
to be a collection K of nonempty ﬁnite sets called (abstract) simplices,
subject only to one condition: If σ ∈K, then every nonempty subset of σ
is in K. Any element of a simplex σ ∈K is called a vertex of σ, and any
nonempty subset of σ is called a face of σ. (We make no distinction between
a vertex v and the corresponding face {v}.) To distinguish the simplices we
deﬁned earlier (as convex subsets of some Euclidean space) from abstract
simplices in this sense, we will sometimes refer to the former as Euclidean
simplices.
The dimension of an abstract simplex consisting of k+1 vertices is deﬁned
to be k. The dimension of K is the maximum dimension of any simplex in
K, if it exists; if there are simplices of arbitrarily high dimensions, K is
said to be inﬁnite-dimensional. We say that K is a ﬁnite complex if K is
a ﬁnite set, and locally ﬁnite if every vertex belongs to only ﬁnitely many
simplices.
A subset of K that is itself a simplicial complex (i.e., that contains all the
faces of each of its simplices) is called a subcomplex of K. The set K(k) of
all simplices of dimension at most k is a k-dimensional subcomplex called
the k-skeleton of K.
Given two abstract complexes K, L, a map f : K →L is called a simpli-
cial map if it is of the form f({v0, . . . , vk}) = {f0(v0), . . . , f0(vk)} for some
map f0 : K(0) →L(0), called the vertex map of f (which must have the
property that {f(v0), . . . , f(vk)} ∈L whenever {v0, . . . , vk} ∈K). A sim-
plicial map f is called an [[Isomorphism|isomorphism]] if f0 is a bijection and {v0, . . . , vk}
is a simplex of K if and only if {f0(v0), . . . , f0(vk)} is a simplex of L.
One way of constructing an abstract simplicial complex, as you have
probably already guessed, is the following. Given a Euclidean simplicial
complex K, let K denote the set of all those ﬁnite subsets {v0, . . . , vk} ⊂
K(0) that consist of the vertices of some simplex of K. It is immediate
that K is an abstract simplicial complex, called the vertex scheme of K. It
is an immediate consequence of Exercise 5.4(b) that two Euclidean com-
plexes are simplicially homeomorphic if and only if their vertex schemes
are isomorphic.
Exercise 5.5.
Show that every ﬁnite abstract complex is the vertex
scheme of a Euclidean simplicial complex. [Hint: Use basis vectors ei =
(0, . . . , 1, . . . , 0) as vertices.]

Abstract Simplicial Complexes
97
Not all abstract simplicial complexes are vertex schemes of Euclidean
complexes, however. Such an abstract complex must obviously be ﬁnite-
dimensional and locally ﬁnite. Moreover, since the local ﬁniteness condition
forces the vertex set of a Euclidean complex to be a discrete subset of Rn,
its vertex scheme can have only countably many simplices. Problem 5-5
shows that these conditions are also suﬃcient.
The theory of quotient spaces gives a useful way of constructing topolog-
ical spaces out of abstract complexes without these restrictions. The ﬁrst
step is to construct a canonical Euclidean k-simplex for each abstract k-
simplex. Using equation (5.1) as a guide, we wish to think of our simplex
as “a set of points of the form  tivi.” The trouble is that the vertices
vi of an abstract simplex are just abstract objects and not points in some
Euclidean space, so this expression no longer makes literal sense as a vector
sum. Instead, we consider such a sum as a “formal linear combination” of
the vertices vi. (The word “formal” is used here to indicate that the expres-
sion has the form of a linear combination, but may not actually represent
addition of vectors in a vector space.) To make this precise, we introduce
a bit of algebraic terminology.
Given a set S, we wish to deﬁne a vector space whose elements we can
think of as “formal linear combinations” of the elements of S. The main
property of such a linear combination is that it is completely determined
by the coeﬃcient t attached to each v ∈S. Thus we are led to the following
deﬁnition: A formal linear combination of elements of S is a function t: S →
R such that t(v) = 0 for all but ﬁnitely many v ∈S. Under the operations
of pointwise addition and multiplication by constants, the set of all such
functions is a vector space, denoted by R⟨S⟩and called the free vector space
on S.
Any element t ∈R⟨S⟩can be represented symbolically as
t =
k

i=0
tivi,
(5.2)
where vi are the (ﬁnitely many) elements of S for which t(v) ̸= 0, and
ti = t(vi). To be a bit more precise, each v ∈S determines in a natural
way a function from S to R, also denoted by v for simplicity, given by
v(w) =

1,
w = v,
0,
w ̸= v.
It is easy to check that each t ∈R⟨S⟩has a unique expression as a ﬁnite lin-
ear combination of these functions; this is the appropriate way to interpret
(5.2).
Now consider any abstract simplex {v0, . . . , vk}. We deﬁne its geometric
realization to be the k-simplex ⟨v0, . . . , vk⟩in the ﬁnite-dimensional vector
space R⟨v0, . . . , vk⟩. With the topology on R⟨v0, . . . , vk⟩induced by any
norm, this geometric realization is homeomorphic to a Euclidean k-simplex.

98
5. Simplicial Complexes
π
FIGURE 5.5. The quotient map deﬁning the topology of |K|.
Since each abstract simplex determines its geometric realization and
vice versa, we will sometimes use the term “simplex” and the notation
⟨v0, . . . , vk⟩interchangeably to refer either to an abstract simplex or to
its geometric realization. When we need to distinguish between the two,
we will use the notation |σ| for the geometric realization of σ. As in the
Euclidean case, the open simplex Int |σ| is the subset of |σ| consisting of
points all of whose coeﬃcients ti are nonzero.
For any abstract simplicial complex K, let |K| denote the set of all formal
linear combinations of the form k
i=0 tivi with ⟨v0, . . . , vk⟩a simplex of K
and with coeﬃcients satisfying 0 ≤ti ≤1 and k
i=0 ti = 1. This can be
thought of abstractly as a subset of the free vector space R⟨K(0)⟩on the
vertex set of K. More concretely, |K| is just the union of all the geometric
realizations of the simplices of K, with points in two simplices identiﬁed
whenever they have the same expression as linear combinations of vertices.
We topologize |K| in the following way. Let 
σ∈K |σ| be the disjoint union
of the geometric realizations of all the simplices of K, with the disjoint union
topology as in Problem 2-9 (this just means that a set is open in 
σ∈K |σ|
if and only if its intersection with each |σ| is open in |σ|), and let
π:

σ∈K
|σ| →|K|
be the natural map that sends each simplex |σ| to itself (Figure 5.5). We
give |K| the quotient topology with respect to π. Unwinding the deﬁnitions,

Abstract Simplicial Complexes
99
this is the same as saying that a subset of |K| is open (or closed) if and only
if its intersection with each simplex is open (or closed). With this topology,
|K| is called the geometric realization of K.
This way of characterizing a topology turns out to be of great importance,
so it has a name. Given any collection {Sα}α∈A of subspaces of a topological
space X whose union is X, the topology of X is said to be coherent with
the subspaces Sα if a set is open in X if and only if its intersection with
each Sα is open in Sα. It is easy to check that this is equivalent to saying
that a set is closed in X if and only if its intersection with each Sα is closed
in Sα.
Lemma 5.4. Let K be an abstract simplicial complex and |K| its geometric
realization.
(a) Each simplex |σ| is a closed, compact subset of |K|.
(b) If dim K = n, then each open n-simplex Int |σ| is an open subset of
|K|.
(c) The topology of |K| is the unique topology coherent with the collection
of subspaces {|σ| : σ ∈K}.
(d) A map F : |K| →|L| is continuous if and only if its restriction to |σ|
is continuous for each σ ∈K.
Exercise 5.6.
Prove Lemma 5.4.
Any simplicial map f : K →L between abstract complexes induces in
an obvious way a map |f| : |K| →|L|. (On each simplex |σ|, |f| is just the
Euclidean simplicial map determined by the vertex map of f.) Since the
restriction of |f| to each simplex is continuous, |f| is a continuous map.
Lemma 5.5. Let K, L, and M be simplicial complexes.
(a) If Id: K →K denotes the identity map of K, then | Id | is the identity
map of |K|.
(b) If f : K →L and g: L →M are simplicial maps, then |g◦f| = |g|◦|f|.
(c) Isomorphic complexes have homeomorphic geometric realizations.
Exercise 5.7.
Prove Lemma 5.5.
Lemma 5.6. If K is the vertex scheme of a Euclidean simplicial complex
K, then the geometric realization of K is homeomorphic to |K|.
Proof. Recall that an abstract simplex σ ∈K is just the set of vertices of
some Euclidean simplex σ ∈K. Let π′ denote the natural map
π′ :

σ∈K
|σ| →|K|,

100
5. Simplicial Complexes
which, restricted to each simplex |σ|, is the obvious simplicial homeomor-
phism |σ| →σ. This map makes the same identiﬁcations as the map π we
used above to deﬁne the topology of |K|. If we can show that π′ is a quo-
tient map, the lemma will follow from the uniqueness of quotient spaces.
To show that it is a quotient map is the same as showing that |K| has the
topology coherent with its simplices.
To verify this, let G ⊂|K| be an arbitrary subset. If G is closed, then
clearly its intersection with any simplex is closed, because it is an inter-
section of closed sets. Conversely, suppose the intersection of G with each
simplex is closed. If x ∈|K| is any limit point of G, by local ﬁniteness x
has a neighborhood U that intersects only ﬁnitely many simplices. Thus
G ∩U is the union of ﬁnitely many closed subsets of U and hence closed in
U. This implies x ∈G, so G is closed in |K|. (This is the reason we insisted
on local ﬁniteness in the deﬁnition of Euclidean simplicial complexes.)
Any topological space that is homeomorphic to the geometric realiza-
tion of some simplicial complex is called a polyhedron. A particular such
homeomorphism is called a triangulation of X. Any space that admits a tri-
angulation (i.e., any polyhedron) is said to be triangulable. Sometimes one
can obtain a better understanding of the topology of an unknown space by
ﬁrst showing that it is triangulable; this will be our approach, for example,
to the classiﬁcation of 1-dimensional and 2-dimensional manifolds.
Example 5.7. The following abstract complexes are isomorphic to the
vertex schemes of the Euclidean complexes of Example 5.2, and therefore
yield triangulations of the indicated spaces.
(a) The set of all nonempty subsets of {0, 1, 2, . . . , n} is an abstract com-
plex whose geometric realization is homeomorphic to Bn.
(b) The set of all proper nonempty subsets of {0, 1, 2, . . . , n} is an abstract
complex whose geometric realization is homeomorphic to Sn−1.
(c) Let K∞be the abstract complex consisting of 0-simplices {{n} : n ∈
Z} and 1-simplices {{n, n + 1} : n ∈Z}. Its geometric realization is
homeomorphic to R.
(d) For any integer m ≥3, let Km be the abstract complex whose
0-simplices are {{1}, {2}, . . . , {m}}, and whose 1-simplices are
{{1, 2}, {2, 3}, . . . , {m −1, m}, {m, 1}}. Its geometric realization is
homeomorphic to S1.
Example 5.8 (Graphs).
We deﬁne a graph to be a 1-dimensional poly-
hedron with a given triangulation. (For some applications, it is useful to
have a more general deﬁnition, allowing two edges to share more than one
vertex, or one edge to begin and end at the same vertex; but this will suﬃce
for our purposes. The kind of graph we have deﬁned is sometimes called a

Abstract Simplicial Complexes
101
simple graph to distinguish it from other more general types. Note that this
use of the word graph has no relation to the graph of a function as deﬁned
in Chapter 3.) A subgraph of a graph is the polyhedron of a 1-dimensional
subcomplex. A graph is said to be ﬁnite if its associated simplicial complex
is ﬁnite.
We will illustrate the utility of simplicial complexes by showing how
a topological property of polyhedra—connectedness—can be detected by
purely combinatorial means. Let K be a simplicial complex. An edge path
in K is a ﬁnite or inﬁnite sequence of vertices such that any two consecutive
vertices span an edge. An edge path is said to be reduced if in addition any
three consecutive vertices are all distinct. (The idea is that a reduced edge
path contains no “dead-end excursions” like v, w, v.) We say that K is edge
path connected if any two vertices can be joined by a ﬁnite edge path.
Proposition 5.9. Let K be a simplicial complex. Then |K| is connected if
and only if K is edge path connected, in which case any two vertices can be
joined by a reduced edge path.
Proof. Suppose K is edge path connected. Because simplices are connected,
any two vertices that span an edge lie in the same component of |K|. It
follows easily by induction that any two vertices joined by a ﬁnite edge
path lie in the same component. Thus if K is edge path connected, all the
vertices lie in the same component V0 of |K|. Any point x ∈|K| lies in some
simplex |σ|, and since |σ| contains at least one vertex in common with V0,
it must be contained in V0. This shows that V0 = |K|, so |K| is connected.
Conversely, suppose |K| is connected. Choose a vertex v ∈K, and let C
denote the subcomplex of K consisting of all vertices that are traversed in
edge paths starting from v, together with all the simplices of K they span.
If σ is a simplex of K that has a vertex w ∈C, then every vertex w′ of σ
must lie in C, because we can form an edge path from v to w′ by starting
with an edge path to w and then appending w′ (since ⟨w, w′⟩is an edge
of σ). Thus σ ∈C as well. It follows that |C| is both open and closed in
|K|, because its intersection with each simplex is either empty or the entire
simplex. Thus C = K, which shows that K is edge path connected.
Now suppose K is edge path connected. Given any two vertices v, v′ ∈
K, there is an edge path (v, . . . , v′) connecting them. If this edge path is
not reduced, it must have three consecutive vertices of the form w, w′, w
for some pair of vertices w, w′ that span an edge. It is easy to see that
the sequence obtained by replacing these three vertices with the single
vertex w is still an edge path connecting the same two vertices. Repeatedly
shortening the edge path in this way until it is impossible to shorten it any
more, we obtain a reduced edge path joining the same two vertices.

102
5. Simplicial Complexes
Triangulation Theorems
In the next chapter we will begin to study the problem of classifying man-
ifolds up to homeomorphism. Our approach to classifying 1-manifolds and
2-manifolds will be to start with a triangulated manifold and study the
combinatorial properties of the triangulation. For this we will need to know
that all manifolds of dimensions 1 and 2 are triangulable.
Theorem 5.10 (Triangulation Theorem for 1-Manifolds). Every 1-
manifold can be triangulated by a 1-dimensional simplicial complex.
Proof. We begin by showing that there exists a sequence of compact sub-
spaces Gn ⊂M, n = 1, 2, . . . , whose union is M, satisfying the following
conditions:
(i) Each Gn is a ﬁnite graph.
(ii) For each n, Gn is a subgraph of Gn+1.
(iii) For each n there exists m > n such that Gn ⊂Int Gm.
By Lemma 4.31, M admits a countable cover {Bi} by regular Euclidean
balls. From the deﬁnition of regular balls, it is evident that the closure of
each regular ball is homeomorphic to a 1-simplex whose topological interior
in M is equal to its interior as a simplex.
Begin by letting G1 be the graph consisting of the single 1-simplex B1
and its vertices. Now let n > 1, and assume by induction that we have
found ﬁnite graphs G1 ⊂G2 ⊂· · · ⊂Gn satisfying (i) and (ii) with Gn =
B1 ∪· · · ∪Bn. Consider the next 1-simplex Bn+1. Some of the vertices
of Gn may lie in Bn+1 (the interior of Bn+1); the ones that do deﬁne a
subdivision of Bn+1 into a ﬁnite graph S, with the property that no vertex
of Gn lies in the interior of any edge of S.
For each of the edges e ⊂S, we will prove the following claim: Either e
intersects each of the edges of Gn only at vertices, or e is entirely contained
in one of the edges of Gn. To prove this, suppose e has an interior point
that lies in some edge e′ ⊂Gn (Figure 5.6). By the remark above, it must
be an interior point of e′ as well.
Note that Int e∩Int e′ is open in Int e. On the other hand, e′ is a compact
subset of the Hausdorﬀspace M, so it is closed in M, and therefore Int e ∩
Int e′ = Int e∩e′ is closed in Int e. By connectedness, therefore, Int e∩Int e′
is all of Int e. In other words, Int e ⊂Int e′, which implies e ⊂e′ and proves
the claim.
Now simply throw away those edges of S that are contained in Gn, and
redeﬁne S to be the graph consisting of the remaining edges and their
vertices. Let Gn+1 = Gn ∪S. We wish to show that Gn+1 is a ﬁnite graph
containing Gn as a subgraph. The edges of S intersect each of the edges
of Gn only at vertices; but it may happen that both vertices of some edge

Triangulation Theorems
103
Gn
S
e′
e
FIGURE 5.6. Proof that e ⊂e′.
e in S intersect a single edge e′ in Gn. If so, simply subdivide e into two
edges by adding a new vertex in its interior. With this modiﬁcation, each
of the edges of S intersects each edge of Gn at most in a single vertex.
Since Gn+1 has only ﬁnitely many simplices, its topology is coherent
with the simplices by Problem 5-1. Thus the foregoing argument proves
that Gn+1 is a ﬁnite graph whose polyhedron is B1 ∪· · · ∪Bn+1 and that
contains Gn as a subgraph. Continuing by induction, we obtain an increas-
ing sequence {Gn : n = 1, 2, . . . } of graphs such that every point of M is
contained in Gn for some n. Since the interiors of the Euclidean balls Bi
cover M, for each n there is some m > n such that the compact set Gn is
covered by B1 ∪· · · ∪Bm, and therefore Gn ⊂Int Gm. This completes the
induction.
Let K be the abstract simplicial complex whose 0-skeleton is the union
of the 0-skeletons of Gn for all n, and whose 1-simplices are the pairs
{v, v′} that span an edge in some Gn. There is an obvious bijective map
|K| →M, deﬁned by choosing a homeomorphism from each 1-simplex of
|K| onto the corresponding edge in M. To see that this map is a homeo-
morphism, we need only show that M has the topology coherent with the
simplices. Clearly, any set that is closed in M has closed intersection with
each simplex, because the simplices have the subspace topology. Conversely,
suppose K ⊂M is a subset whose intersection with each simplex is closed.
If x ∈M is a limit point of K, choose n large enough that x ∈Int Gn.
Since the intersection of K with each of the (ﬁnitely many) simplices of Gn
is closed in Gn, it follows that K ∩Int Gn is closed in Int Gn. In particular,
x ∈K, which proves that K is closed in M and thus the topology of M is
coherent with the simplices.
For use in the next chapter, we will need the following property of tri-
angulated 1-manifolds.
Proposition 5.11. If K is a simplicial complex whose geometric realiza-
tion is a 1-manifold, each vertex of K lies on exactly two edges.

104
5. Simplicial Complexes
Proof. Let v be any vertex, and let V be the union of {v} together with
the interiors of all the edges that have v as a vertex. Since the intersection
of V with each simplex is open in the simplex, V is open in |K|.
Because |K| is a 1-manifold, v has a neighborhood U ⊂V homeomorphic
to an open interval. It follows that U ∖{v} has exactly two components.
For each edge e containing v, Int e∩(U ∖{v}) is an open subset of U ∖{v}.
These sets are disjoint (because all the edges have disjoint interiors), and
nonempty (because e∩U is nonempty and open in e and thus must contain
some interior points of e). Therefore, if v lies on more than two edges, we
have a separation of U ∖{v} into more than two nonempty disjoint open
subsets, contradicting the fact that it has only two components. This shows
that each vertex lies on at most two edges.
On the other hand, if some vertex v lies on only one edge e, the con-
struction above shows that v has a Euclidean neighborhood U contained
entirely in e. This means that v has a neighborhood Y ⊂U such that
Y ∖{v} is connected—just take Y to be the image of [0, ε) under some
homeomorphism ϕ: [0, 1] →e taking 0 to v. But any Euclidean neighbor-
hood minus a point is disconnected by Problem 4-1(a), so there can be no
such vertex.
We turn our attention next to 2-manifolds. The following theorem was
proved by Tibor Rad´o [Rad25] in 1925.
Theorem 5.12 (Triangulation Theorem for Surfaces).
Every
2-
manifold admits a triangulation by a 2-dimensional simplicial complex, in
which each edge lies on exactly two 2-simplices.
Sketch of proof. The basic approach is analogous to the proof of triangu-
lability of 1-manifolds: Cover the manifold with countably many regular
disks, and inductively show that each successive disk can be triangulated
in a way that is compatible with the triangulations that have already been
deﬁned, so that the manifold is ultimately written as an increasing union of
polyhedra. In the case of surfaces, however, ﬁnding a triangulation of each
successive disk that is compatible with the previous ones is much more dif-
ﬁcult, primarily because the boundary of the new disk might intersect the
boundaries of the already-deﬁned simplices inﬁnitely many times. Even if
there are only ﬁnitely many intersections, showing that the regions deﬁned
by the intersecting curves are homeomorphic to closed disks, and therefore
triangulable, requires a delicate topological result known as the Sch¨onﬂies
theorem, which asserts that any topological embedding of the circle into R2
extends to an embedding of the closed disk. The details of the proof are
long and intricate and would take us too far from our main goals, so we
leave it to the reader to look it up. A readable presentation can be found
in [Moi77].

Orientations
105
v1
v1
v2
v3
v4
v4
v5
v6
FIGURE 5.7. The M¨obius band.
Finally, although we will not use it, we mention the following more recent
result, proved by Edwin Moise in 1977 [Moi77].
Theorem 5.13 (Triangulation Theorem for 3-Manifolds).
Every
3-manifold is triangulable.
Beyond dimension 3, matters are not nearly so nice. It has recently been
shown that there are manifolds of dimension 4 that admit no triangula-
tions; and it is still not known whether all manifolds of dimension greater
than 4 can be triangulated. See [Ran96] for a history of the subject of
triangulations and a summary of the current state of the art.
Orientations
The M¨obius band is the famous topological space obtained by identifying
two edges of the square I × I according to the relation (0, t) ∼(1, 1 −t)
(Figure 5.7). It is a manifold with boundary (though not a manifold), and
it is triangulable (one triangulation is shown in Figure 5.7). If you have
ever made a paper model (it is best to start with a long, narrow rectangle
instead of a square), you have undoubtedly noticed that it has the curious
property that it is impossible to consistently pick out which is the “front”
side and which is the “back”—you cannot continuously color one side gray
and the other side white.
By using simplicial theory, we can make this notion precise and extend
it to complexes of other dimensions as well. Instead of choosing which side
of each triangle to call the front, we will, in eﬀect, choose which direction
of travel around the vertices to consider “counterclockwise.”
Let σ be an abstract k-simplex. Given any two orderings (vi0, . . . , vik)
and (vj0, . . . , vjk) of the vertices of σ, there is a permutation s of the set
{0, . . . , k} such that s(ip) = jp for p = 0, . . . , k. Deﬁne an equivalence rela-
tion on the set of all orderings by saying that two orderings are equivalent
if they diﬀer by an even permutation (see the Appendix). A choice of an
equivalence class of vertex orderings is called an orientation of σ. For ex-
ample, an orientation of a 1-simplex is just a choice of initial and terminal
vertices, which can be indicated schematically by drawing an arrow along

106
5. Simplicial Complexes
v0
v0
v0
v1
v1
v1
v2
v2
v3
FIGURE 5.8. Orientations of simplices.
the simplex (see Figure 5.8). An orientation of a 2-simplex is a choice of a
preferred direction of rotation, which can be indicated by a circular arrow;
and an orientation of a 3-simplex is a choice of “handedness”: The preferred
hand is the one whose ﬁngers curl around the ﬁrst three vertices in order
while the thumb points toward the fourth. Since there is only one way to
order a single vertex, by convention an orientation for a 0-simplex is just a
choice of a plus or minus sign.
An oriented simplex is a simplex together with a choice of orientation.
We will write [v0, . . . , vk] for the k-simplex ⟨v0, . . . , vk⟩oriented by the
vertex ordering (v0, . . . , vk), and we will let −[v0, . . . , vk] denote the same
simplex with the opposite orientation. Thus, for example, for 1-simplices
and 2-simplices we have
[v, w] = −[w, v],
[v, w, x] = [w, x, v] = [x, v, w] = −[v, x, w] = −[x, w, v] = −[w, v, x].
Any n-simplex in Rn automatically gets an orientation, which we call
the natural orientation, by declaring [v0, . . . , vn] to be oriented if and only
if det(v1 −v0, v2 −v0, . . . , vn −v0) > 0. To see that this is well-deﬁned, ﬁrst
note that the n vectors {v1 −v0, . . . , vn −v0} are independent precisely
when the vertices {v0, . . . , vn} are in general position. Interchanging two
vertices other than v0 has the same eﬀect as interchanging two rows of
the determinant, which changes its sign. If v0 is interchanged with another
vertex vi, the determinant becomes det(v1 −vi, . . . , v0 −vi, . . . , vn −vi);
multiplying the ith row by −1 (which changes the sign of the determinant)
and then adding the ith row to each other row (which leaves the deter-
minant unchanged) transforms the new determinant back to the original
one. Thus a transposition of two vertices always changes the sign of the
determinant, so an arbitrary permutation of the vertices changes the sign
of the determinant if and only if it is even, which shows that this rule gives
a well-deﬁned orientation. Geometrically, for a 1-simplex in R the natural
orientation is from the smaller to the larger vertex; for a 2-simplex in R2 it

Orientations
107
+
−
FIGURE 5.9. Induced orientations of boundary faces.
is the counterclockwise direction of rotation; and for a 3-simplex in R3 it
is the right-handed orientation. (These statements can be taken as mathe-
matical deﬁnitions of the terms “counterclockwise” and “right-handed.”)
If σ = [v0, . . . , vk] is an oriented k-simplex, the orientation of σ deter-
mines an orientation on each of its boundary faces (i.e., faces of dimension
k −1), called the induced orientation, by the following rule: The induced
orientation on the face τi = ⟨v0, . . . , vi, . . . , vk⟩(where the hat indicates
that vi is omitted) is deﬁned to be (−1)i[v0, . . . , vi, . . . , vk]. To check that
this is well-deﬁned, we need to show that the induced orientation of τi is un-
changed if the vertices of σ are subjected to an even permutation. Because
every permutation can be written as a composition of transpositions of ad-
jacent vertices (see Exercise A.19 in the Appendix), it suﬃces to show that
the induced orientation is reversed if two adjacent vertices of σ are trans-
posed. This is clear if neither of the vertices is vi. If vi is transposed with
vi±1, the induced orientation becomes (−1)i±1[v0, . . . , vi−1, vi+1, . . . , vk],
which is the opposite of what it was originally.
For an oriented 1-simplex [v0, v1], the induced orientation gives a minus
sign to the initial vertex v0 and a plus sign to the terminal vertex v1 (Figure
5.9). For an oriented 2-simplex [v0, v1, v2], the induced orientations on the
edges are [v1, v2], −[v0, v2] = [v2, v0], and [v0, v1]. Thus the arrow on each
edge points in the preferred direction of rotation.
Now suppose K is an n-dimensional simplicial complex in which every
(n−1)-simplex is a face of no more than two n-simplices. (It can be shown,
though we will not do so, that any triangulated manifold has this form.)
If σ and σ′ are two n-simplices that share a boundary face τ, we say that
orientations of σ and σ′ are consistent if they induce opposite orientations
on τ. An orientation of K is a choice of orientation of each n-simplex
in such a way that any two simplices that intersect in an (n −1)-face are
consistently oriented. Figure 5.10 gives schematic indications of orientations
of 1-dimensional and 2-dimensional complexes. If a complex K admits an
orientation, it is said to be orientable.
Example 5.14. The triangulation of the M¨obius band shown in Figure 5.7
is not orientable. To see why, suppose there exists an orientation. Reversing
the orientations of all the 2-simplices if necessary, we may assume that
the leftmost triangle is oriented as [v1, v4, v5] (i.e., in the counterclockwise

108
5. Simplicial Complexes
FIGURE 5.10. Orientations of simplicial complexes.
direction). Then the consistency condition implies that the next simplex
is oriented as [v1, v5, v2]. Similarly, each of the succeeding simplices must
be oriented in the counterclockwise direction. But then both the leftmost
and the rightmost 2-simplices induce the same orientation [v1, v4] on their
common edge, which contradicts the consistency condition. Therefore, there
exists no orientation.
Example 5.15. Let σ = ⟨v0, . . . , vn+1⟩be an (n+1)-simplex in Rn+1, and
let K be the set of proper faces of σ, which is a triangulation of Sn. Give
σ the natural orientation inherited from Rn+1, and give the n-simplices
of K the induced orientation. Each (n −1)-simplex of K is of the form
τ = ⟨v0, . . . , vi, . . . , vj, . . . , vn+1⟩, and belongs to two n-simplices: the one
opposite vi and the one opposite vj. It is easy to check that the orientations
induced on τ by these two faces are opposite, because in one case vi is
removed ﬁrst and then vj, while in the other case the order is reversed.
Thus we have produced an orientation of K.
Proposition 5.16. Let K be any n-dimensional Euclidean complex in Rn.
The natural orientation of each n-simplex determines an orientation of K.
Proof. First we show that no more than two n-simplices in K can have an
(n −1)-face in common. Let τ be an (n −1)-simplex in K. The vertices
of τ determine a unique aﬃne hyperplane (i.e., (n −1)-dimensional aﬃne
subspace) in Rn, whose complement has exactly two components, which
we call the sides of τ. Because the vertices of σ are in general position, the
additional vertex of σ that is not in τ must lie on one side of τ or the other,
and therefore all of σ ∖τ must lie on the same side (since it is connected).
For any x ∈Int τ and any suﬃciently small ε > 0, Bε(x) ∖τ has two
components, one lying on each side of τ. Any n-simplex that contains τ
must contain exactly one of these components for ε small enough. Thus if
more than two n-simplices contain τ, two of them must contain the same

Combinatorial Invariants
109
component of Bε(x) ∖τ and therefore have interior points in common,
which contradicts the deﬁnition of a Euclidean complex.
Now we must show that the natural orientations of any two sim-
plices σ, σ′ ∈K that share an (n −1)-face τ are consistent. Write
τ = ⟨v0, . . . , vn−1⟩, σ = ⟨v0, . . . , vn−1, vn⟩, and σ′ = ⟨v0, . . . , vn−1, v′
n⟩.
The function f(v) = det(v1 −v0, . . . , v −v0) is an aﬃne function of v
that is zero precisely when v lies in the aﬃne hyperplane determined by
τ, so it must be positive on one side of τ and negative on the other side.
Since the argument above implies that vn and v′
n lie on opposite sides
of τ, it follows that det(v1 −v0, . . . , v′
n −v0) has the opposite sign from
det(v1 −v0, . . . , vn −v0). If the vertices have been ordered so that the
natural orientation of σ is [v0, . . . , vn], then the natural orientation of σ′
is −[v0, . . . , v′
n], and it is immediate that they induce opposite orientations
on τ.
Combinatorial Invariants
Simplicial complexes were invented in the hope that they would enable
topological questions about manifolds to be reduced to combinatorial ques-
tions about simplicial complexes. To make sense of this, we need a notion
of equivalence of complexes that is weaker than simplicial isomorphism but
strong enough to imply that they have homeomorphic geometric realiza-
tions, and that can be detected purely from the combinatorial structure of
the abstract complexes.
The most natural way to modify a simplicial complex to obtain another
one with a homeomorphic geometric realization is to “subdivide” the sim-
plices of the original complex into smaller ones. We can then consider two
complexes to be equivalent if they both have a common subdivision. In this
section we make this notion precise, and study one important property of
complexes that is preserved by this kind of equivalence. For our purposes,
it is suﬃcient and simpler to restrict our attention to ﬁnite complexes,
although many of the deﬁnitions can be extended to the general case.
Let K be a ﬁnite Euclidean simplicial complex. A subdivision of K is a
simplicial complex K′ with the following properties:
• |K′| = |K|.
• Each simplex of K′ is contained in a simplex of K.
• Each simplex of K is a ﬁnite union of simplices of K′.
Some examples of subdivisions are shown in Figure 5.11.
Example 5.17 (Barycentric Subdivision). A particularly useful kind
of subdivision is obtained in the following way. Let σ = ⟨v0, . . . , vk⟩be a

110
5. Simplicial Complexes
K
L
M
N
K′
L′
M ′
N ′
FIGURE 5.11. Subdivisions.
Euclidean k-simplex in Rn. If v is a point not in the k-dimensional aﬃne
subspace determined by σ, we deﬁne
v ∗σ = ⟨v, v0, . . . , vk⟩.
This is a (k + 1)-simplex, called the cone on σ from v.
Now let K be a ﬁnite Euclidean complex. For each k-simplex σ =
⟨v0, . . . , vk⟩∈K, deﬁne the barycenter of σ to be the point
bσ =
k

i=0
1
k + 1vi ∈Int σ.
It is the “center of gravity” of the vertices of σ. (The name comes from
Greek barys, meaning “heavy.”) For example, the barycenter of a 1-simplex
is just its midpoint; the barycenter of a vertex v is v itself.
We will deﬁne a complex SK, called the barycentric subdivision of K,
whose vertices are the barycenters of all the simplices in K. It is easiest
to deﬁne by induction on the dimension of K. If dim K = 0, then we set
SK = K (you cannot subdivide a point!). Assuming that we have deﬁned
SK for all ﬁnite complexes of dimension less than n, we deﬁne SK for
a complex of dimension n as the union of S(K(n−1)) with the set of all
simplices of the form bσ ∗τ where σ is an n-simplex of K and τ is any
simplex of S(K(n−1)) contained in a face of σ. It is straightforward to
check that SK is indeed a subdivision of K (see Problem 5-7). Examples
of barycentric subdivisions are pictured in Figure 5.12.
The key fact about barycentric subdivision is that it reduces the sizes of
all the simplices by a uniform ratio, as the following lemma shows.
Lemma 5.18. If σ is a Euclidean k-simplex in Rm, the diameter of each
simplex in the barycentric subdivision of σ is at most k/(k + 1) times that
of σ.

Combinatorial Invariants
111
K
SK
S(SK)
FIGURE 5.12. Barycentric subdivisions.
Proof. Note ﬁrst that for any point x ∈σ, the maximum of the function
|x −y| for y ∈σ is achieved when y is a vertex. To see why, let R be
the maximum distance from x to any vertex of σ; since σ is the convex
hull of its vertices and the closed ball BR(x) is a convex set containing the
vertices, σ ⊂BR(x), which proves the claim. It follows immediately that
the diameter of σ is the maximum of the distances between its vertices.
The following computation shows that the distance from the barycenter
bτ of a q-simplex τ = ⟨v0, . . . , vq⟩to any of its vertices vj is at most q/(q+1)
times the diameter of τ:
|bτ −vj| =

q

i=0
1
q + 1vi −vj

=

q

i=0
1
q + 1vi −
q

i=0
1
q + 1vj

≤
q

i=0
1
q + 1|vi −vj|
≤
q
q + 1 diam τ.
Now if σ′ is any face of the barycentric subdivision of σ and w1, w2 are
any two vertices of σ′, by Problem 5-7 each wj is the barycenter of a kj-
dimensional face τj of σ, and we may assume that τ1 is a face of τ2. By
the computation above, the distance from w2 to any point of τ2 is at most
k2/(k2 + 1) times the diameter of τ2. Since w1, in particular, is a point in
τ2, we have
|w1 −w2| ≤
k2
k2 + 1 diam τ2 ≤
k
k + 1 diam σ.

112
5. Simplicial Complexes
It follows from the remark at the beginning of the proof that diam σ′ sat-
isﬁes the same inequality.
To express subdivisions in terms of the combinatorics of abstract com-
plexes, we will show how to decompose an arbitrary subdivision into a
sequence of subdivisions that are combinatorially simpler. Suppose K′ is
a subdivision of K. We say that it is an elementary subdivision if K′ con-
tains precisely one more vertex than K. (For example, the 3-dimensional
complex M ′ in Figure 5.11 is an elementary subdivision of M, obtained by
adding one vertex in the bottom face of M.)
Suppose we start with a ﬁnite Euclidean complex K and choose a k-
simplex σ = ⟨v0, . . . , vk⟩∈K, choose a point v ∈Int σ, and replace
each simplex ⟨v0, . . . , vk, w1, . . . , wm⟩that has σ as a face (including σ
itself) by the set of all simplices of the form ⟨v, vi1, . . . , vij, w1, . . . , wm⟩as
{vi1, . . . , vij} ranges over proper subsets of {v0, . . . , vk}. Then it is easy to
check that K′ is an elementary subdivision of K, and that every elementary
subdivision is of this form. Moreover, if K′′ is any subdivision of K, there
is a ﬁnite sequence K = K0, K1, . . . , Km = K′′ of complexes such that
Ki+1 is an elementary subdivision of Ki. One advantage of working with
elementary subdivisions is that the eﬀect of an elementary subdivision on
the vertex scheme of K is clearly determined solely by the choice of σ, and
so elementary subdivisions can be deﬁned by the recipe above for arbitrary
abstract complexes as well.
Two ﬁnite simplicial complexes are said to be combinatorially equivalent
if they become isomorphic after ﬁnitely many elementary subdivisions. It
was conjectured by Ernst Steinitz and Heinrich Tietze in 1908 that if two
ﬁnite simplicial complexes have homeomorphic polyhedra, they are com-
binatorially equivalent; this conjecture became known as the Hauptvermu-
tung (main conjecture) of combinatorial topology. It is now known to be
true for all ﬁnite complexes of dimension 2 and for triangulated compact
manifolds of dimension 3, but false in all higher dimensions. (See [Ran96]
for a nice discussion of the history of this problem.) Thus the hope of re-
ducing topological questions about manifolds to combinatorial ones about
simplicial complexes has not been realized. Nonetheless, simplicial theory
has provided us with a number of extremely useful combinatorial invariants
that turn out to have important topological ramiﬁcations. We conclude this
chapter with an introduction to one of them, called the Euler characteristic.
The Euler Characteristic
One of the oldest results in global surface theory is Euler’s formula: If
P ⊂R3 is a compact polyhedral surface that is the boundary of a convex
open set, and P has F faces, E edges, and V vertices, then V −E +F = 2.
This quantity has a natural generalization to arbitrary ﬁnite simplicial
complexes: If K is a ﬁnite simplicial complex of dimension n, we deﬁne the

Combinatorial Invariants
113
Euler characteristic of K, denoted by χ(K), by
χ(K) =
n

k=0
(−1)knk,
where nk is the number of k-dimensional simplices in K. Although we are
not yet in a position to prove Euler’s formula in full generality, we can
at least show that the Euler characteristic of a simplicial complex is a
combinatorial invariant.
Theorem 5.19. If K and L are combinatorially equivalent ﬁnite simpli-
cial complexes, then χ(K) = χ(L).
Proof. It clearly suﬃces to prove that the Euler characteristic is unchanged
by an elementary subdivision. Let K′ be an elementary subdivision of K
obtained by adding a vertex v in the k-simplex σ = ⟨v0, . . . , vk⟩, and let
Δχ = χ(K′) −χ(K). We must show that Δχ = 0.
For each simplex τ = ⟨v0, . . . , vk, w1, . . . , wm⟩of K that has σ as a
face, K′ has one less (k + m)-simplex. In its place, for each j-element
proper subset {vi1, . . . , vij} ⊂{v0, . . . , vk}, K′ has a new (j + m)-simplex
⟨v, vi1, . . . , vij, w1, . . . , wm⟩. There are
k+1
j

=
(k+1)!
j!(k+1−j)! such subsets, so
each such τ makes a contribution to Δχ of
−(−1)k+m +
k

j=0
k + 1
j

(−1)j+m =
k+1

j=0
k + 1
j

(−1)j+m.
By the binomial theorem, this last sum is the expansion of the polynomial
(−1)m(x + 1)k+1 evaluated at x = −1, and therefore is equal to zero.
Note that we are not claiming yet that the Euler characteristic is a
topological invariant, because two triangulations of the same compact space
are not necessarily combinatorially equivalent. In fact, it is a topological
invariant. For compact surfaces, this will follow from the classiﬁcation of
surfaces, which we will complete in Chapter 10. For more general simplicial
complexes, the proof will require techniques of homology theory, which we
will develop in Chapter 13.

114
5. Simplicial Complexes
Problems
5-1. Suppose X is a topological space, and G1, . . . , Gk are ﬁnitely many
closed subspaces of X whose union is X. Show that the topology of
X is coherent with these subspaces. Explain what this has to do with
the gluing lemma (Lemma 3.8).
5-2. Let v be a vertex of the simplicial complex K, and let St v (the open
star of v) be the union of the open simplices Int σ as σ ranges over all
simplices that have v as a vertex. Show that St v is a neighborhood
of v in |K|, and the collection of open stars of all the vertices is an
open cover of |K|.
5-3. Show that every polyhedron is Hausdorﬀand locally path connected.
5-4. Let K be an abstract simplicial complex. Show that |K| is compact if
and only if K is ﬁnite, and locally compact if and only if K is locally
ﬁnite.
5-5. Show that an abstract simplicial complex is the vertex scheme of
a Euclidean complex if and only if it is ﬁnite-dimensional, locally
ﬁnite, and countable. [Hint: If the complex has dimension n, let the
vertices be the points vk = (k, k2, k3, . . . , k2n+1) ∈R2n+1. Use the
fundamental theorem of algebra to show that no 2n+2 vertices lie in
a proper aﬃne subspace, so any 2n+2 or fewer vertices are in general
position. If two simplices σ, τ with vertices in this set intersect, let
σ0, τ0 be the smallest face of each containing an intersection point,
and consider the set consisting of all the vertices of σ0 and τ0. (This
proof is from [Sti93].)]
5-6. Deﬁne an abstract simplicial complex K to be the following collection
of abstract 2-simplices together with all of their faces:
{{a, b, e}, {b, e, f}, {b, c, f}, {c, f, g}, {a, c, g}, {a, e, g},
{e, f, h}, {f, h, j}, {f, g, j}, {g, j, k}, {e, g, k}, {e, h, k},
{a, h, j}, {a, b, j}, {b, j, k}, {b, c, k}, {c, h, k}, {a, c, h}}.
Show that the geometric realization of K is homeomorphic to the
torus. [Hint: Look at Figure 5.13.]
5-7. If K is a ﬁnite Euclidean simplicial complex, show that its barycentric
subdivision SK is in fact a subdivision of K, and that the simplices of
SK are those of the form ⟨bσ0, . . . , bσk⟩in which each σj is a simplex
in K and σj is a face of σj+1 for j = 0, . . . , k −1.
5-8. Let K be a ﬁnite complex. Give an explicit algorithm for obtaining the
barycentric subdivision of K as a sequence of elementary subdivisions.

Problems
115
a
a
a
a
b
b
c
c
e
e
f
g
h
h
j
k
FIGURE 5.13. Triangulation of the torus.
5-9. Let K be the 1-dimensional abstract complex whose vertices are the
nonnegative integers and whose 1-simplices are {⟨0, n⟩: n ∈N}, and
let S be the subspace of R2 obtained by taking the union of all the
line segments in Example 5.3. Deﬁne a map F : |K| →S by sending
0 to the origin, sending each n > 0 to the point (1, 1/n), and sending
each 1-simplex ⟨0, n⟩linearly onto the corresponding line segment.
Show that F is continuous and bijective but not a homeomorphism.
5-10. Suppose K is any simplicial complex whose geometric realization is a
1-manifold. Show that K is 1-dimensional.
5-11. Show that every triangulated 1-manifold is orientable.
5-12. Show that orientability is a combinatorial invariant of ﬁnite simplicial
complexes. [Hint: It suﬃces to prove that if K is a ﬁnite Euclidean
complex and K′ is a subdivision of K, then an orientation of either
K or K′ determines an orientation of the other. Show that if σ is an
oriented Euclidean n-simplex and σ′ is an n-simplex in some subdi-
vision of σ, there is a unique orientation of σ′ such that any aﬃne
embedding σ →Rn that determines the given orientation of σ also
determines the given orientation of σ′.]

6
Curves and Surfaces
In this chapter we undertake a detailed study of curves (1-manifolds) and
surfaces (2-manifolds). These are the manifolds that are most familiar from
our everyday experience, and about which the most is known mathemat-
ically. They are thus excellent prototypes for the study of manifolds in
higher dimensions.
We begin by proving the classiﬁcation theorem for 1-manifolds, which
says that every connected 1-manifold is homeomorphic to S1 or R. Using
the triangulation theorem for 1-manifolds proved in Chapter 5, this is a
simple exercise in the combinatorics of graphs.
We then proceed to a general discussion of 2-manifolds and a detailed
examination of the basic examples of compact surfaces: the sphere, the
torus, and the projective plane. Next we show how to form other compact
surfaces by the technique of connected sums, a way of patching together
simpler surfaces to form more complicated ones. To unify these results, we
introduce the notion of polygonal presentations of surfaces, which generalize
simplicial complexes by representing surfaces as a collection of polygons
(not necessarily triangles) with edges identiﬁed in pairs.
The central part of the chapter presents the main part of the classiﬁcation
theorem for compact surfaces, which says that every compact, connected
surface is homeomorphic to a sphere, a connected sum of tori, or a con-
nected sum of projective planes. Again, the triangulation theorem reduces
the problem to one of showing that every polygonal presentation can be
reduced to a standard presentation of one of the model surfaces.

118
6. Curves and Surfaces
In the last section we revisit orientations and the Euler characteristic,
introduced in the last chapter for simplicial complexes, and reinterpret
them in the context of polygonal surface presentations.
Classiﬁcation of Curves
Our ﬁrst goal in this chapter is to prove that up to homeomorphism, the
only connected 1-manifolds are the line and the circle. (Of course, this clas-
siﬁes the disconnected ones too, because it implies that each component of
a disconnected 1-manifold is a line or a circle, so every 1-manifold is home-
omorphic to a countable disjoint union of lines and/or circles.) You can
think of this classiﬁcation theorem as a warm-up for the more complicated
classiﬁcation of surfaces to follow; but it is also quite important in its own
right.
Theorem 6.1 (Classiﬁcation of 1-Manifolds).
A
connected
1-
manifold is homeomorphic to S1 if it is compact and to R if it is
not.
Proof. By the triangulation theorem (Theorem 5.10) and Proposition 5.11,
M is homeomorphic to a graph in which every vertex lies on exactly two
edges. Let K denote the abstract simplicial complex associated with this
graph. We will show that K is isomorphic either to one of the complexes
Km of Example 5.7(d) (the vertex scheme of a regular m-gon, whose poly-
hedron is homeomorphic to S1) or to the complex K∞of Example 5.7(c)
(whose polyhedron is homeomorphic to R). Since isomorphic complexes
have homeomorphic polyhedra, this suﬃces to prove the theorem.
The ﬁrst step is to show that every vertex in M is contained in a reduced
edge path {vn : n ∈Z} that extends indeﬁnitely in both directions. Start
with any vertex v0. By assumption v0 lies on two edges, so we can label the
other vertices of those edges arbitrarily as v1 and v−1. Now by induction
deﬁne vn+1 for each n ≥1 to be the unique vertex other than vn−1 such
that vn and vn+1 span an edge. Similarly, we deﬁne v−n by induction on
n.
Let U be the union of all the edges ⟨vn, vn+1⟩⊂M for vn in the edge
path. The set U is closed in M (because its intersection with each sim-
plex is closed and M has the coherent topology), and open (because the
edges minus their vertices are open, and each vertex has a neighborhood
intersecting only two edges, both of which must be in U). Thus U = M.
Now we distinguish two cases.
Case I: vn ̸= vk for any n ̸= k. In this case, the correspondence sending
n 
→vn is easily seen to give an isomorphism between K∞and K, so M is
homeomorphic to R.

Surfaces
119
vi
vi+m
vi+m+1
vi+m−1
vi+1
FIGURE 6.1. Periodic edge path.
Case II: vn = vn+m for some n ∈Z and some m > 0. We may assume
that m and n have been chosen so that m is the least positive integer with
this property. (Note that m ≥3 because the edge path is reduced.) We
will show by induction that the edge path is periodic, in the sense that
vi = vi+m for every i. By hypothesis this is true for i = n. If it is true for
some i ≥n, we argue as follows. The two vertices vi+m−1 and vi+m+1 are
the only vertices that are connected to vi+m by edges (Figure 6.1). Since
vi = vi+m, the vertex vi+1 also is connected by an edge to vi+m, so it must
be equal to either vi+m−1 or vi+m+1. By minimality of m it cannot be equal
to vi+m−1, so vi+1 = vi+m+1, completing the induction for i ≥n. A similar
induction takes care of i ≤n.
Now let Km be the complex of Example 5.7(d), and deﬁne a map
f : K(0)
m →K(0) by f(n) = vn for n = 1, . . . , m. Again, it is straightfor-
ward to check that {f(i), f(j)} are the vertices of a simplex of K if and
only if {i, j} are the vertices of a simplex of Km. Thus f extends to a
simplicial isomorphism, so M is homeomorphic to S1.
Surfaces
The rest of this chapter is devoted to the study of compact surfaces. We
have already seen several important examples: the sphere S2, the torus T2,
and the projective plane P2 (i.e., the projective space of dimension 2). As
we will soon see, these examples are fundamental because every compact
surface can be built up from these three.
In order to systematize our knowledge of surfaces, it will be useful to
have a uniform way to represent them that is somewhat more general than
simplicial complexes. The prototype is the representation of the torus as a

120
6. Curves and Surfaces
π
FIGURE 6.2. The sphere as a quotient of the disk.
quotient of the square by identifying the edges in pairs (Example 3.24). It
turns out that every compact surface can be represented as a quotient of a
polygonal region in the plane by an equivalence relation that identiﬁes its
edges in pairs.
Let us begin by seeing how our three basic compact examples can be
so represented. We have already shown how to represent the torus as a
quotient of a square (Example 3.24), so we focus on the sphere and the
projective plane.
Proposition 6.2. The sphere S2 is homeomorphic to the following quo-
tient spaces.
(a) The closed disk B2 ⊂R2 modulo the equivalence relation generated by
(x, y) ∼(−x, y) for x ∈∂B2 (Figure 6.2).
(b) The square I ×I modulo the equivalence relation generated by (0, t) ∼
(t, 0) and (t, 1) ∼(1, t) for 0 ≤t ≤1 (Figure 6.3).
Proof. To see that each of these spaces is homeomorphic to the sphere,
all we need to do is exhibit a quotient map from the given space to the
sphere that makes the same identiﬁcations, and then appeal to uniqueness
of quotient spaces (Corollary 3.32).
For (a), deﬁne a map from the disk to the sphere by wrapping each
horizontal line segment around a “latitude circle” (Figure 6.2). Formally,
π: B2 →S2 is given by
π(x,y)
=
⎧
⎪
⎪
⎪
⎨
⎪
⎪
⎪
⎩

−

1 −y2 cos
πx

1 −y2 , −

1 −y2 sin
πx

1 −y2 , y

,
y ̸= ±1;
(0, 0, y),
y = ±1.

Surfaces
121
γ
π
α
β
FIGURE 6.3. The sphere as a quotient of the square.
This is a quotient map by the closed map lemma; it is straightforward to
check that it makes exactly the same identiﬁcations as the given equivalence
relation.
To prove (b), we will construct a quotient map from I×I to the sphere as
a composition of several simpler maps (Figure 6.3). First let S denote the
square {(x, y) : |x|, |y| ≤1}, and deﬁne a homeomorphism α: I × I →S
by ﬁrst scaling both coordinates by a factor of 2 and then translating
the new center (1, 1) back to the origin: α(x, y) = (2x −1, 2y −1). Then
let β : S →B2 be the homeomorphism whose existence is guaranteed by
Proposition 4.26; it sends each radial line segment between the origin and
the boundary of S linearly onto the parallel segment between the center of
the disk and its boundary. Next let γ : B2 →B2 be the counterclockwise
rotation through π/4 radians (obviously a homeomorphism), and consider
the composite map ϕ = π ◦γ ◦β ◦α:
I × I
α
−→S
β
−→B2
γ
−→B2
π
−→S2,
where π is the quotient map of the preceding paragraph. Since this is a
composition of quotient maps, it is a quotient map. Threading through the
deﬁnitions (with help from the pictures!), you will see that it makes the
same identiﬁcations as the quotient map deﬁned in (b), thus completing
the proof.
Proposition 6.3. The projective plane P2 is homeomorphic to each of the
following quotient spaces (Figure 6.4).

122
6. Curves and Surfaces
(b)
(c)
x
−x
(a)
FIGURE 6.4. Representations of P2 as a quotient space.
(a) The sphere S2 modulo the equivalence relation x ∼−x for each x ∈
S2.
(b) The closed disk B2 modulo the relation (x, y) ∼(−x, −y) for each
(x, y) ∈∂B2.
(c) The square I×I modulo the relation (t, 0) ∼(1−t, 1), (0, 1−t) ∼(1, t)
for 0 ≤t ≤1.
Proof. Let S2/∼denote the quotient space of S2 obtained by identifying
each point x with its antipodal point −x, and let p: S2 →S2/∼denote the
quotient map. Consider also the composite map
S2
ι	→R3 ∖{0}
π
−→P2,
where ι is inclusion and π is the quotient map deﬁning P2. Note that π ◦ι
is a quotient map by the closed map lemma. It makes exactly the same
identiﬁcations as p, so by uniqueness of quotient spaces P2 is homeomorphic
to S2/∼.
If F : B2 →S2 is the map sending the disk onto the upper hemisphere
by F(x, y) = (x, y,

1 −x2 −y2), then p ◦F : B2 →S2/∼is easily seen
to be surjective, and is thus a quotient map by the closed map lemma. It
identiﬁes only (x, y) ∈∂B2 with (−x, −y) ∈∂B2, so P2 is homeomorphic
to the resulting quotient space.
Part (c) is left as an exercise.
Exercise 6.1.
Prove Proposition 6.3(c).
When doing geometric “cutting and pasting” constructions like the ones
in the last two propositions, it is often safe to rely on pictures and a few
words to describe the maps and identiﬁcations being constructed. So far, we
have been careful to give explicit deﬁnitions (often with formulas) of all our
maps, together with rigorous proofs that they do in fact give the results

Surfaces
123
q
FIGURE 6.5. An edge point.
v
FIGURE 6.6. A vertex.
we claim; but as your sophistication increases and you become adept at
carrying out such explicit constructions yourself, you can leave out many
of the details. The main thing is that before you skip any such details,
you should be absolutely sure that you could quickly write them down and
check your claims rigorously; this is the only way to be sure that you are not
hiding real diﬃculties behind “hand-waving.” In this book we will begin to
leave out some such details in our proofs; for a while, you should ﬁll them
in for yourself to be sure that you know how to turn an argument based
on pictures into a complete proof.
Now we describe a general method for building surfaces by identifying
edges of geometric ﬁgures. Let us say that a subset P of the plane is a polyg-
onal region if it is a compact subset whose boundary is a ﬁnite 1-dimensional
Euclidean simplicial complex, satisfying the following conditions:
(i) Each point q of an edge other than a vertex has a neighborhood U in
R2 such that P ∩U is equal to the intersection with U of some closed
half-plane {(x, y) : ax + by + c ≥0} (Figure 6.5).
(ii) Each vertex v has a neighborhood V in R2 such that P ∩V is equal
to the intersection of V with two closed half-planes whose boundaries
intersect only at v (Figure 6.6).
Any ﬁnite collection of disjoint 2-simplices in the plane is easily seen to
be a polygonal region, as is a ﬁlled-in square, or any compact convex region
bounded by ﬁnitely many 1-simplices. Below, we will see some more exam-
ples of manifolds obtained as quotients of polygonal regions by identifying
the edges in pairs. It is a general fact that such a quotient space is always
a surface.
Proposition 6.4. Let P be a polygonal region in the plane with an even
number of edges, and suppose we are given an equivalence relation that

124
6. Curves and Surfaces
q1
q2
U1
U2
α1
α2
FIGURE 6.7. Euclidean neighborhood of an edge point.
identiﬁes each edge with exactly one other edge by means of a simplicial
homeomorphism. The resulting quotient space is a compact 2-manifold.
Proof. Let M be the quotient space, and let π: P →M denote the quotient
map. Clearly, M is compact, because it is the continuous image of the
compact space P.
Since the equivalence relation identiﬁes only edges with edges and ver-
tices with vertices, the points of M fall into three disjoint sets: (a) face
points, whose inverse images in P are in the interior of P; (b) edge points,
whose inverse images are on edges but not vertices; and (c) vertex points,
whose inverse images are vertices. To prove that M is locally Euclidean,
we consider the three types separately.
Because π is injective on Int P, Int P is a saturated open subset of P, so
the restriction of π to Int P is a one-to-one quotient map and therefore a
homeomorphism. Thus π(Int P) is a Euclidean neighborhood of each face
point.
An edge point q has exactly two inverse images q1 and q2, each on a
diﬀerent edge. Using condition (i) in the deﬁnition of polygonal region,
there exist disjoint neighborhoods U1 of q1 and U2 of q2 such that P ∩Ui
is a closed half-disk (Figure 6.7). Let Vi = P ∩Ui. It is straightforward
to construct aﬃne homeomorphisms α1 taking V1 to a half-disk in the
upper half-plane and α2 taking V2 to a half-disk in the lower half-plane,
in such a way that q1 and q2 both go to the origin and the boundary
identiﬁcations are respected. Deﬁne α: V1 ∪V2 →R2 by letting α = α1 on
V1 and α = α2 on V2. Shrinking V1 and V2 if necessary, we can ensure that
V1 ∪V2 is a saturated open set in P (this just means that for each point
in V1 ∩∂P, the corresponding boundary point is in V2, and conversely).
Then the restriction of π to V1 ∪V2 is a quotient map, so α descends to a
map α: V →R2, where V = π(V1 ∪V2). Its image contains a neighborhood

Surfaces
125
v2
v4
v3
v1
FIGURE 6.8. Euclidean neighborhood of a vertex point.
of the origin by construction, and its domain V is the image under π of
a saturated open set and therefore open. This shows that q has a locally
Euclidean neighborhood.
Similarly, a vertex point v has as its inverse image a ﬁnite set of ver-
tices {v1, . . . , vk} ⊂P. For each i, choose a homeomorphism from a
neighborhood of vi in P to an open subset in a closed “wedge” of an-
gle 2π/k in the plane, which is a set described in polar coordinates by
{(r, θ) : θ0 ≤θ ≤θ0 + 2π/k}. (If we place vi at the origin, such a homeo-
morphism is given in polar coordinates by a fan transformation of the form
(r, θ) 
→(r, θ0 + cθ) for suitable constants θ0, c.)
Because each edge is paired with exactly one other, the k wedges can
be mapped onto a set containing a neighborhood of the origin by rotating
and piecing them together (Figure 6.8). However, this may not respect
the edge identiﬁcations. To correct this, we can subject each wedge to
a preliminary transformation that rescales its edges independently. First,
by a rotation followed by a fan transformation, take the wedge to the ﬁrst
quadrant so that one edge lies along the positive x-axis and the other along
the positive y-axis. Then rescale the two axes by a linear transformation
(x, y) 
→(ax, by). Finally, use another fan transformation to insert the
wedge into its place. (The case k = 1 deserves special comment. This
case can occur only if the two edges adjacent to the single vertex v1 are
identiﬁed with each other; then you can check that our construction maps
a neighborhood of v1 onto a neighborhood of the origin, with both edges
going to the same ray.) In each case, we end up with a map deﬁned on
a saturated open set in P, which descends to a homeomorphism from a
neighborhood of v to a neighborhood of the origin.
The quotient is second countable by Lemma 3.21. To prove that it is
Hausdorﬀis the same as showing that the ﬁbers of π can be separated by

126
6. Curves and Surfaces
FIGURE 6.9. The Klein bottle.
saturated open sets. It is straightforward to check on a case-by-case basis
that the inverse images of suﬃciently small Euclidean balls will do.
Here is another example of a manifold formed as a quotient of a polygonal
region.
Example 6.5. The Klein bottle is the 2-manifold K obtained by iden-
tifying the edges of the square I × I according to (0, t) ∼(1, t) and
(t, 0) ∼(1 −t, 1) for 0 ≤t ≤1. To visualize K, think of gluing the left and
right edges together to form a cylinder, and then passing the upper end of
the cylinder through the cylinder wall near the lower end, in order to glue
the upper circle to the lower one “from the inside” (Figure 6.9). Of course,
this cannot be done with a physical model; in fact, it can be shown that
the Klein bottle is not homeomorphic to any subspace of R3. Nonetheless,
the preceding proposition shows that it is a 2-manifold.
Connected Sums
To construct other examples of surfaces, we now introduce an important
way of producing manifolds by gluing together simpler ones, called “con-
nected sum.” Although we will use this primarily for surfaces, it works for
manifolds of any dimension, so we will deﬁne it in arbitrary dimensions.
Let M1 and M2 be connected n-manifolds. Geometrically, the connected
sum is obtained by cutting out a small open ball from each of M1 and M2
and gluing the resulting spaces together along their boundary spheres. More
precisely, let Bi ⊂Mi be regular Euclidean balls. Choose a homeomorphism
σ: ∂B1 →∂B2 (such a homeomorphism exists because both boundaries are
homeomorphic to Sn−1). Let M ′
i = Mi ∖Bi, and deﬁne a quotient space
of M ′
1 ⨿M ′
2 by identifying each q ∈∂B1 with σ(q) ∈∂B2 (Figure 6.10).
The resulting quotient space is called a connected sum of M1 and M2 and
is denoted by M1 # M2.
Proposition 6.6. If M1 and M2 are connected n-manifolds, any connected
sum M1 # M2 is a connected n-manifold.

Connected Sums
127
M1
M2
π
B1
B2
M1 # M2
FIGURE 6.10. A connected sum.
Proof. First we show that M1#M2 is locally Euclidean. Let π: M ′
1⨿M ′
2 →
M1 # M2 denote the quotient map, and let S = π(∂B1 ∪∂B2). Since π is
one-to-one and thus a homeomorphism away from S, M1 # M2 ∖S is a
manifold and therefore locally Euclidean. Thus we need only consider points
in S.
For any nonempty interval J ⊂[0, ∞), let us use the notation AJ to
denote the annulus {x ∈Rn : |x| ∈J}. Thus, for example, A[1,2) is equal to
B2(0) ∖B1(0). Our regular balls Bi for i = 1, 2 come with neighborhoods
Ui containing Bi and homeomorphisms ϕi : Ui →B2(0) taking Ui∖Bi onto
A[1,2) (Figure 6.11). (If ϕi takes Ui onto a ball of radius diﬀerent from 2,
we can adjust it by a dilation to make sure that its image is B2(0).) Notice
that ϕi sends ∂Bi to the unit sphere.
The ﬁrst thing we need to do is to adjust one of these maps to compensate
for the fact that ϕ−1
2
◦ϕ1 does not make the same identiﬁcation between
∂B1 and ∂B2 as σ does. To correct this, observe that the composite map
β = ϕ2 ◦σ ◦ϕ−1
1
from Sn−1 ⊂Rn to itself is a homeomorphism:
Sn−1 ϕ−1
1
−→∂B1
σ
−→∂B2
ϕ2
−→Sn−1.
Deﬁne a homeomorphism β from B2(0) to itself by sending the ray through
each point x0 ∈Sn−1 linearly onto the ray through β(x0); formally, since

128
6. Curves and Surfaces
U1 ∖B1
U2 ∖B2
ϕ1
β
A[1,2)
A[1,2)
ϕ2
ϕ1
A(1/2,2)
I
FIGURE 6.11. Euclidean neighborhood of points in S.
x/|x| is the point where the ray through x intersects Sn−1,
β(x) = |x| β
 x
|x|

.
Let ϕ1 = β ◦ϕ1. It is immediate from the deﬁnitions that
ϕ1 = ϕ2 ◦σ
on ∂B1.
(6.1)
The inversion map I(x) = x/|x|2 maps the annulus A[1,2) homeomorphi-
cally onto the annulus A(1/2,1], and restricts to the identity map on Sn−1.
We deﬁne a map Φ from the open set (U1 ∖B1) ∪(U2 ∖B2) ⊂M ′
1 ⨿M ′
2
to Rn by
Φ(q) =

I ◦ϕ1(q),
q ∈U1 ∖B1,
ϕ2(q),
q ∈U2 ∖B2.
Let us check that Φ respects the identiﬁcations made by π. If q ∈∂B1
and p = σ(q) ∈∂B2, then
I ◦ϕ1(q) = ϕ1(q)
(because I is the identity on Sn−1)
= ϕ2 ◦σ(q)
(by (6.1))
= ϕ2(p).
Thus Φ passes to the quotient and deﬁnes a homeomorphism from a neigh-
borhood of S to the open annulus A(1/2,2), showing that M1 #M2 is locally

Polygonal Presentations of Surfaces
129
#
=
FIGURE 6.12. Connected sum with a sphere.
Euclidean. The proofs that it is second countable and Hausdorﬀare anal-
ogous to those in Proposition 6.4, and are left as an exercise.
To show that M1 # M2 is connected, just note M1 # M2 is the union of
the two sets π(M ′
1) and π(M ′
2), which are both connected and have points
of S in common.
Exercise 6.2.
Prove that M1 # M2 is Hausdorﬀand second countable.
Our deﬁnition of M1 # M2 depends on several choices—the sets Bi and
the homeomorphism σ. When M1 and M2 are surfaces, it can be shown
that diﬀerent choices yield homeomorphic connected sums. We will not
prove this in full generality, but in the case of compact surfaces it will
turn out to be a consequence of the classiﬁcation theorem (see Problem
10-4). Nevertheless, we will sometimes use the imprecise terminology “the
connected sum M1 # M2” to refer to any connected sum between M1 and
M2.
Example 6.7. If M is any n-manifold, a connected sum M #Sn is homeo-
morphic to M, at least if we choose the set to cut out of Sn carefully (Figure
6.12). Let B2 ⊂Sn be the open lower hemisphere, so (Sn)′ = Sn ∖B2 is
the closed upper hemisphere, which is homeomorphic to a closed ball. Then
M #Sn is obtained from M by cutting out the open ball B1 and gluing back
a closed ball along the boundary sphere, so we have not changed anything.
Example 6.8. The n-fold connected sum T2 # T2 # · · · # T2 (Figure
6.13), is called the n-holed torus, or the sphere with n handles. The lat-
ter terminology refers to the fact that this surface is also homeomorphic to
S2 # T2 # · · · # T2, and each added torus looks like a “handle” attached to
the sphere (Figure 6.14).
Polygonal Presentations of Surfaces
As we mentioned earlier in this chapter, for the classiﬁcation theorem we
need a uniform way to describe surfaces. We will represent all of our surfaces

130
6. Curves and Surfaces
FIGURE 6.13. A connected sum of tori.
FIGURE 6.14. A sphere with handles.
as quotients of 2n-sided polygonal regions. Informally, we can describe any
edge equivalence relation by labeling the edges with letters a1, . . . , an, and
giving each edge an arrow pointing toward one of its vertices, in such a
way that edges with the same label are to be identiﬁed, with the arrows
indicating which way the vertices match up. With each such labeling of a
polygon we associate a sequence of symbols, obtained by reading oﬀthe
boundary labels counterclockwise from the top, and for each boundary label
ai, placing ai in the sequence if the arrow points counterclockwise and a−1
i
if it points clockwise. For example, the equivalence relation on I × I of
Example 3.24 that yields the torus might result in the sequence of symbols
aba−1b−1.
Formally, given a set S, we deﬁne a word in S to be an ordered k-tuple of
symbols, each of the form a or a−1 for some a ∈S. (To be more precise, if
you like, you can deﬁne a word to be a ﬁnite sequence of ordered pairs of the
form (a, 1) or (a, −1) for a ∈S, and then deﬁne a and a−1 as abbreviations
for (a, 1) and (a, −1), respectively.) A polygonal presentation, written
P = ⟨S | W1, . . . , Wk⟩,
is a ﬁnite set S together with ﬁnitely many words W1, . . . , Wk in S of length
3 or more, such that every symbol in S appears in at least one word. As a

Polygonal Presentations of Surfaces
131
S2
a
a
a
a
P2
FIGURE 6.15. Presentations of S2 and P2.
matter of notation, when the set S is described by listing its elements, we
will leave out the braces surrounding the elements of S, and will denote the
words Wi by juxtaposition, so for example the presentation with S = {a, b}
and the single word W = (a, b, a−1, b−1) will be written ⟨a, b | aba−1b−1⟩.
We also allow as a special case any presentation in which S has one element
and there is a single word of length 2. There are only four such: ⟨a | aa⟩,
⟨a | a−1a−1⟩, ⟨a | aa−1⟩, and ⟨a | a−1a⟩.
Any polygonal presentation P determines a topological space |P|, called
the geometric realization of P, by the following recipe:
1. For each word Wi, let Pi denote the convex k-sided polygonal region
in the plane that has its center at the origin, sides of length 1, and
one vertex on the positive y-axis. (Here k is the length of the word
Wi.)
2. Deﬁne a one-to-one correspondence between the symbols of Wi and
the edges of Pi in counterclockwise order, starting at the vertex on
the y-axis.
3. Let |P| denote the quotient space of 
i Pi determined by identifying
each pair of edges that have the same edge symbol according to the
simplicial homeomorphism that matches up the ﬁrst vertices in coun-
terclockwise order if both edges have the same label a or a−1, and
matches the ﬁrst vertex of one with the second vertex of the other if
the edges are labeled a and a−1.
If P is one of the special presentations with a word of length 2, motivated
by Propositions 6.2 and 6.3 we deﬁne |P| to be the sphere if the word is
aa−1 or a−1a, and the projective plane if it is aa or a−1a−1 (Figure 6.15).
The interiors, edges, and vertices of the polygonal regions Pi are called
the faces, edges, and vertices of the presentation. The number of faces is the
same as the number of words, while the number of edges is the total number
of symbols that occur in all the words. For an edge labeled a, the initial
vertex is the ﬁrst one in counterclockwise order, and the terminal vertex

132
6. Curves and Surfaces
p2
p1
P1
F
P2
FIGURE 6.16. Simplicial homeomorphism between polygons.
is the other one; for an edge labeled a−1, these deﬁnitions are reversed.
In terms of our informal description above, if we label each edge with an
arrow pointing counterclockwise when the symbol is a and clockwise when
it is a−1, the arrow points from the initial vertex to the terminal vertex.
The geometric realization of a presentation with only one face is con-
nected, because it is a quotient of a single connected polygon; with more
than one face, it might or might not be connected. Although for deﬁniteness
we have deﬁned the geometric realization as a quotient of a disjoint union
of a speciﬁc collection of polygonal regions, the following lemma shows
that we could have used arbitrary disjoint convex polygonal regions in the
plane with the same numbers of edges, because between any two polygonal
regions with the same sequence of edge labels there is a homeomorphism
that respects the edge labels. Because of this, in the arguments that fol-
low we will illustrate our presentations with any convex polygons that are
convenient.
Lemma 6.9. Let P1, P2 be convex polygons with the same number of edges,
and let f : ∂P1 →∂P2 be a simplicial homeomorphism. Then f extends to
a homeomorphism F : P1 →P2.
Proof. Choose any points pi ∈Int Pi, i = 1, 2. By convexity, the line seg-
ment from pi to each vertex of Pi lies entirely in Pi. The edges and vertices
of Pi together with pi, these new line segments, and the triangles they
bound form a Euclidean simplicial complex whose polyhedron is Pi (Fig-
ure 6.16). The required map F : P1 →P2 is the simplicial map whose
restriction to ∂P1 is f and that takes p1 to p2.
A polygonal presentation is called a surface presentation if each symbol
a ∈S occurs exactly twice in W1, . . . , Wk (counting either a or a−1 as
one occurrence). By Proposition 6.4, the geometric realization of a surface
presentation is a compact surface.

Polygonal Presentations of Surfaces
133
K
S2
b
b
b
b
b
b
b
b
a
a
a
a
a
a
a
a
P2
T2
FIGURE 6.17. Standard presentations.
Example 6.10. The following surfaces are determined by the given polyg-
onal presentations, which we call their standard presentations (Figures 6.15
and 6.17).
(a) The sphere: ⟨a | aa−1⟩or ⟨a, b | abb−1a−1⟩(Proposition 6.2).
(b) The torus: ⟨a, b | aba−1b−1⟩(Example 3.24).
(c) The projective plane: ⟨a | aa⟩or ⟨a, b | abab⟩(Proposition 6.3).
(d) The Klein bottle: ⟨a, b | abab−1⟩(Example 6.5).
If K is a 2-dimensional simplicial complex in which every simplex is con-
tained in some 2-simplex, then K determines in an obvious way a polygonal
presentation in which each 2-simplex corresponds to a word of length 3.
For later use in proving the classiﬁcation theorem, we will develop some
general rules for transforming polygonal presentations. If two presentations
P1 and P2 have homeomorphic geometric realizations, we will say that they
are topologically equivalent and write P1 ≈P2.
The following operations are called elementary transformations of a
polygonal presentation. As a matter of notation, in what follows S will
denote any sequence of symbols; a, b, c, a1, a2, . . . will denote any symbols
from S or their inverses; e will denote any symbol not in S; and W1, W2, . . .
will denote any words made from the symbols in S. Given two words
W1, W2, the notation W1W2 denotes the word formed by concatenating
W1 and W2 together. We adopt the convention that (a−1)−1 = a.
• Relabeling: Changing all occurrences of a symbol a to a new symbol
not already in the presentation, interchanging all occurrences of two
symbols a and b, or interchanging all occurrences of a and a−1 for
some a ∈S.
• Subdividing: Replacing every occurrence of a by ae and every oc-
currence of a−1 by e−1a−1, where e is a new symbol not already in
the presentation.

134
6. Curves and Surfaces
a5
a5
a4
a4
a3
a3
a1
a1
a2
a2
FIGURE 6.18. Reﬂecting.
a3
a3
a4
a4
a5
a5
a1
a1
a2
a2
FIGURE 6.19. Rotating.
W1
W1
W2
W2
e
e
FIGURE 6.20. Cutting/pasting.
e
e
e
a
a
b
b
c
c
FIGURE 6.21. Folding/unfolding.
• Consolidating: If a and b always occur adjacent to each other either
as ab or b−1a−1, replacing every occurrence of ab by a and every
occurrence of b−1a−1 by a−1, provided that the result is one or more
words of length at least 3 or a single word of length 2.
• Reflecting (Figure 6.18):
⟨S | a1 . . . am, W2, . . . , Wk⟩
→⟨S | a−1
m . . . a−1
1 , W2, . . . , Wk⟩.
• Rotating (Figure 6.19):
⟨S | a1a2 . . . am, W2, . . . , Wk⟩
→⟨S | a2 . . . ama1, W2, . . . , Wk⟩.
• Cutting (Figure 6.20): If W1 and W2 both have length at least 2,
⟨S | W1W2, W3, . . . , Wk⟩
→⟨S, e | W1e, e−1W2, W3, . . . , Wk⟩.
• Pasting (Figure 6.20):
⟨S, e | W1e, e−1W2, W3, . . . , Wk⟩
→⟨S | W1W2, W3, . . . , Wk⟩.
• Folding (Figure 6.21): If W1 has length at least 3,
⟨S, e | W1ee−1, W2, . . . , Wk⟩
→⟨S | W1, W2, . . . , Wk⟩.
We also allow W1 to have length 2, provided that the presentation
has only one word.

Polygonal Presentations of Surfaces
135
• Unfolding (Figure 6.21):
⟨S | W1, W2, . . . , Wk⟩
→⟨S, e | W1ee−1, W2, . . . , Wk⟩.
Proposition 6.11. Each elementary transformation of a polygonal pre-
sentation produces a topologically equivalent presentation.
Proof. Clearly, subdividing and consolidating are inverses of each other,
as are cutting/pasting and folding/unfolding, so by symmetry only one of
each pair needs to be proved. We demonstrate the techniques by proving
the proposition for cutting and folding, and leave the rest as exercises.
To prove that cutting produces a homeomorphic geometric realization,
let P1 and P2 be convex polygons labeled W1e and e−1W2, respectively,
and let P ′ be a convex polygon labeled W1W2. For the moment, let us
assume that these are the only words in their respective presentations. Let
π: P1 ⨿P2 →S and π′ : P ′ →S′ denote the respective quotient maps.
The line segment going from the terminal vertex of W1 in P ′ to its initial
vertex lies in P ′ by convexity; label this segment e. By Lemma 6.9 there is
a continuous map f : P1 ⨿P2 →P ′ that takes each edge of P1 or P2 to the
edge in P ′ with the corresponding label, and whose restriction to each Pi
is a homeomorphism. By the closed map lemma, f is a quotient map. Since
f identiﬁes the two edges labeled e and e−1 but nothing else, the quotient
maps π′ ◦f and π make precisely the same identiﬁcations, so their quotient
spaces are homeomorphic. If there are other words W3, . . . , Wk, we just
extend f by declaring it to be the identity on their respective polygons and
proceed as above.
For folding, as before we can ignore the additional words W2, . . . , Wk. If
W1 has length 2, we can subdivide to lengthen it, then perform the folding
operation, and then consolidate, so we assume that W1 has length at least
3. Assume ﬁrst that W1 = abc has length exactly 3. Let P and P ′ be convex
polygons with edge labels abcee−1 and abc, respectively, and let π: P →S,
π′ : P ′ →S′ be the quotient maps. Adding edges as shown in Figure 6.21
turns P and P ′ into polyhedra of Euclidean simplicial complexes, and there
is a unique simplicial map f : P →P ′ that takes each edge of P to the edge
of P ′ with the same label. As before, π′ ◦f and π are quotient maps that
make the same identiﬁcations, so their quotient spaces are homeomorphic.
If W1 has length 4 or more, we can write W1 = Xbc for some X of length
at least 2. Then we cut along a to obtain
⟨S, b, c, e | Xbcee−1⟩≈⟨S, a, b, c, e | Xa−1, abcee−1⟩,
and proceed as before.
Exercise 6.3.
Prove the rest of Proposition 6.11. Note that you will have
to consider a word of length 2 as a special case when treating subdividing
or consolidating.

136
6. Curves and Surfaces
f
P ′
1
Q
P1
π
π′
M1
M1
B1
f
v
v
v
v
a
a
a
c
c
c
b
b
b
W1
W1
FIGURE 6.22. The presentation ⟨S1, a, b, c | W1c−1b−1a−1, abc⟩.
Next we need to ﬁnd standard polygonal presentations for connected
sums. The key is the following proposition.
Proposition 6.12. Let M1 and M2 be surfaces determined by presenta-
tions ⟨S1 | W1⟩and ⟨S2 | W2⟩, respectively, in which S1 and S2 are disjoint
sets and each presentation has a single face. Then ⟨S1, S2 | W1W2⟩is a
presentation of a connected sum M1 # M2. (Here W1W2 denotes the word
formed by concatenating W1 and W2 together.)
Proof. Consider the presentation ⟨S1, a, b, c | W1c−1b−1a−1, abc⟩(pictured
in the left half of Figure 6.22). Pasting along a and folding twice, we see
that this presentation is equivalent to ⟨S1 | W1⟩and therefore is a pre-
sentation of M1. Let B1 denote the image in M1 of the interior of the
polygonal region bounded by triangle abc. We will show below that B1
is a regular Euclidean disk in M1. Assuming this, it follows immediately
that the geometric realization of ⟨S1, a, b, c | W1c−1b−1a−1⟩is homeomor-
phic to M1 ∖B1 (which we denote by M ′
1), and ∂B1 is the image of the
edges c−1b−1a−1. A similar argument shows that ⟨S2, a, b, c | abcW2⟩is a
presentation of M2 with a Euclidean disk removed (denoted by M ′
2). There-
fore, ⟨S1, S2 | W1c−1b−1a−1, abcW2⟩is a presentation of M ′
1 ⨿M ′
2 with the
boundaries of the respective disks identiﬁed, which is M1 # M2. Pasting
along a and folding twice, we arrive at the presentation ⟨S1, S2 | W1W2⟩.
It remains only to show that B1 is a regular disk in M1, i.e., that it has an
open disk neighborhood in which B1 corresponds to a smaller closed disk.
Let P1, P ′
1, and Q be convex polygons with edges labeled by the words W1,
W1c−1b−1a−1, and abc, respectively. Triangulating the polygons as shown
in Figure 6.22, we obtain a simplicial map f : P ′
1 ⨿Q →P1 such that π ◦f

Classiﬁcation of Surface Presentations
137
v
FIGURE 6.23. Showing that B1 is a regular disk.
makes the same identiﬁcations as π′, and so descends to a homeomorphism
f : M1 →M1. The inverse image of f(B1) under π is a small triangle in P1
sharing one vertex v in common with P1.
Now look back at the proof in Proposition 6.4 that the quotient space
of a surface presentation is a manifold. In constructing a Euclidean neigh-
borhood of a vertex point, we assembled “wedges” at the various vertices
into a Euclidean disk. Applying that construction to the vertex v, the small
triangle is taken to a set that is homeomorphic to a closed disk in the plane
(Figure 6.23), and it is an easy matter to extend that homeomorphism to
a slightly larger open disk.
Example 6.13. Using the preceding proposition, we can augment our list
of presentations of known surfaces as follows:
• Connected sum of n tori:
⟨a1, b1, . . . , an, bn | a1b1a−1
1 b−1
1
. . . anbna−1
n b−1
n ⟩.
• Connected sum of n projective planes:
⟨a1, . . . , an | a1a1 . . . anan⟩.
We call these the standard presentations of these surfaces.
Classiﬁcation of Surface Presentations
We are now ready to state the main result in the classiﬁcation of surfaces.
This theorem was ﬁrst proved in 1907 by Max Dehn and Poul Heegaard
[DH07] under the assumption that the surface had some polygonal presen-
tation. Using the triangulation theorem of Chapter 5, we now know that
every compact surface has a triangulation, which determines a polygonal
presentation.

138
6. Curves and Surfaces
a
a
a
a
a
a a
b
b
b
b
b
b
b
b
c
c
c
c
c
c
FIGURE 6.24. Transforming the Klein bottle to P2 # P2.
Theorem 6.14 (Classiﬁcation of Surface Presentations).
Any sur-
face presentation is equivalent by a sequence of elementary transformations
to a presentation of one of the following:
(a) the sphere S2;
(b) a connected sum T2 # · · · # T2; or
(c) a connected sum P2 # · · · # P2.
Therefore, every compact surface is homeomorphic to one of the surfaces
in this list.
Before we prove the theorem, we need to make one important observa-
tion. You might have noticed that some surfaces appear to be absent from
the list—the Klein bottle, for example, and T2 # P2, and, for that mat-
ter, every connected sum involving both tori and projective planes. These
apparent deﬁciencies are explained by the following two lemmas.
Lemma 6.15. The Klein bottle is homeomorphic to P2 # P2.
Proof. By a sequence of elementary transformations, we ﬁnd that the Klein
bottle has the following presentations (see Figure 6.24):
⟨a, b | abab−1⟩
≈⟨a, b, c | abc, c−1ab−1⟩
(cut along c)
≈⟨a, b, c | bca, a−1cb⟩
(rotate and reﬂect)
≈⟨b, c | bbcc⟩.
(paste along a and rotate)
This last is a presentation of the connected sum of two projective planes.
Lemma 6.16. The connected sum T2#P2 is homeomorphic to P2#P2#P2.
Proof. Start with ⟨a, b, c | abab−1cc⟩(Figure 6.25), which is a presentation
of K #P2, and therefore by the preceding lemma of P2 #P2 #P2. Following
Figure 6.25, we cut along d, paste along c, cut along e, and paste along b,
rotating and reﬂecting as necessary, to obtain ⟨a, d, e | a−1d−1adee⟩, which
is a presentation of T2 # P2.

Classiﬁcation of Surface Presentations
139
a
a
a
a
a
a
a
a
a
a
b
b
b
b
b
b
b
b
c
c
c c
d
d
d
d
d
d
d
d
d
e
e
e
e
e
FIGURE 6.25. Transforming P2 # P2 # P2 to T2 # P2.
Proof of the classiﬁcation theorem. By the triangulation theorem we can
assume that M comes with a given presentation. We will prove the theorem
by transforming this presentation to one of our standard presentations in
several steps. Let us say that a pair of edges that are to be identiﬁed
are complementary if they appear in the presentation as both a and a−1,
and twisted if they appear as a, . . . , a or as a−1, . . . , a−1. (The terminology
reﬂects the fact that if a polygonal region is cut from a piece of paper, you
have to twist the paper to paste together a twisted edge pair, but not for
a complementary pair.)
Step 1: M admits a presentation with only one face. Since M is con-
nected, if there are two or more faces, some edge in one face must be
identiﬁed with an edge in a diﬀerent face; otherwise, M would be the dis-
joint union of the quotients of its faces, and since each such quotient is open
and closed, they would provide a separation of M. Thus by performing suc-
cessive pasting transformations (together with rotations and reﬂections as
necessary), we can reduce the number of faces in the presentation to one.
Step 2: Either M is homeomorphic to the sphere, or M admits a presen-
tation in which there are no adjacent complementary pairs. Each adjacent
complementary pair can be eliminated by folding, unless it is the only pair
of edges in the presentation; in this case the presentation is equivalent to
⟨a | aa−1⟩and M is homeomorphic to the sphere.
From now on, we assume that the presentation is not the standard pre-
sentation of the sphere.
Step 3: M admits a presentation in which all twisted pairs are adjacent.
If a twisted pair is not adjacent, the presentation is described by a word of
the form V aWa, where neither V nor W is empty. Figure 6.26 shows how
to transform the word V aWa into V W −1bb by cutting along b, reﬂecting,
and pasting along a. (Here W −1 denotes the word obtained from W by
reﬂecting). In this last presentation, the twisted pair a, a has been replaced

140
6. Curves and Surfaces
a
a
a
a
b
b
b
b
b
V
V
W
W −1
V W −1
FIGURE 6.26. Making a twisted pair adjacent.
by another twisted pair b, b, which is now adjacent. Moreover, no other ad-
jacent pairs have been separated. We may have created some new twisted
pairs when we reﬂected W, but we decreased the total number of nonadja-
cent pairs by at least one. Thus, after ﬁnitely many such operations, there
will be no more nonadjacent twisted pairs. We may also have created some
new adjacent complementary pairs. These can be eliminated by repeating
Step 2, which does not increase the number of nonadjacent pairs.
Step 4: M admits a presentation in which all vertices are identiﬁed to
a single point. Choose some equivalence class of vertices, and call it v.
If there are vertices that are not identiﬁed with v, there must be some
edge that goes from a v vertex to a vertex in some other equivalence class;
label the edge a and the other vertex class w (Figure 6.27). The other
edge that touches a at its v vertex cannot be identiﬁed with a: If it were
complementary to a, we would have eliminated both edges in Step 3, while
if it formed a twisted pair with a, then the quotient map would identify the
initial and terminal vertices of a with each other, which we are assuming
is not the case. So label this other edge b, and label its other vertex x (this
one may be identiﬁed with v, w, or neither one).
Somewhere in the polygon is another edge labeled b or b−1. Let us assume
for deﬁniteness that it is b−1; the argument for b is similar except for an
extra reﬂection. Thus we can write the word describing the presentation in
the form baXb−1Y , where X and Y are unknown words, not both empty.
Now cut along c and paste along b as in Figure 6.27. In the new presentation,
the number of vertices labeled v has decreased, and the number labeled w
has increased. We may have introduced a new adjacent complementary
pair, so perform Step 2 again to remove it. This may again decrease the
number of vertices labeled v (for example, if a v vertex lies between edges
labeled aa−1 that are eliminated by folding), but it cannot increase their
number. So repeating this sequence a ﬁnite number of times—decrease
the v vertices by one, then eliminate adjacent complementary edges—we
eventually eliminate the vertex class v from the presentation altogether.
Iterate this procedure for each vertex class until there is only one left.
Step
5: If the presentation has any complementary pair a, a−1,
then it has another b, b−1 that occurs intertwined with the ﬁrst, as in
a, . . . , b, . . . , a−1, . . . , b−1. If this is not the case, then the presentation is of
the form aXa−1Y , where X contains only matched complementary pairs or

Classiﬁcation of Surface Presentations
141
a
b
c
b
v
w
x
v
x
X
Y
b
c
a
c
x
v
w
w
x
X
Y
FIGURE 6.27. Reducing the number of vertices equivalent to v.
a
a
a
a
b
b
b
b
b
b
b
b
c
c
c
c
c
c
c
d
d
d
W
W
W
W
X
X
X
X
Y
Y
Y
Y
Z
Z
Z
Z
FIGURE 6.28. Bringing intertwined complementary pairs together.
adjacent twisted pairs. Thus each edge in X is identiﬁed only with another
edge in X, and the same is true of Y . But this means that the terminal
vertices of the a and a−1 edges, both of which touch only X, can be identi-
ﬁed only with vertices in X, while the initial vertices can be identiﬁed only
with vertices in Y . This is a contradiction, since all vertices are identiﬁed
together by Step 4.
Step 6: M admits a presentation in which all intertwined complementary
pairs occur together with no other edges intervening: aba−1b−1. If the pre-
sentation is given by the word WaXbY a−1Zb−1, perform the elementary
transformations indicated in Figure 6.28 (cut along c, paste along a, cut
along d, and paste along b) to obtain the new word cdc−1d−1WZY X. This
replaces the old intertwined set of pairs with a new adjacent set cdc−1d−1,
without separating any edges that were previously adjacent. Repeat this for
each set of intertwined pairs. (Note that this step requires no reﬂections.)
Step 7: M is homeomorphic to either a connected sum of tori or a con-
nected sum of projective planes. From what we have done so far, all twisted
pairs occur adjacent to each other, and all complementary pairs occur in
intertwined groups like aba−1b−1. This is a presentation of a connected sum

142
6. Curves and Surfaces
of tori (presented by aba−1b−1) and projective planes (presented by cc). If
there are only tori or only projective planes, we are done.
The only remaining case is that in which the presentation contains both
twisted and complementary pairs. In that case, some twisted pair must oc-
cur next to a complementary one; thus the presentation is described either
by a word of the form aba−1b−1ccX or by one of the form ccaba−1b−1X. In
either case, this is a connected sum of a torus, a projective plane, and what-
ever surface is described by the word X. But Lemma 6.16 shows that the
standard presentation of T2#P2 can be transformed to that of P2#P2#P2.
Making this transformation, we eliminate one of the occurrences of T2 in
the connected sum. Iterating this procedure, we eliminate them all, thus
completing the proof.
Combinatorial Invariants
Two of the properties of simplicial complexes introduced in Chapter 5—
orientations and the Euler characteristic—generalize easily to polygonal
surface presentations, and give us interesting information about surfaces.
Let us extend the notion of combinatorial invariance by saying that a prop-
erty of a polygonal presentation is a combinatorial invariant if it is un-
changed by elementary transformations. Of course, any topological invari-
ant of the geometric realization (such as connectedness) is automatically a
combinatorial invariant, because elementary transformations yield homeo-
morphic surfaces. It would not be diﬃcult to show that every polygonal
presentation can be triangulated and that the two notions of combinatorial
invariants coincide; however, in this case it is easier just to work directly
with the polygonal presentations.
The Euler Characteristic
The Euler characteristic can be generalized to polygonal presentations in
the following form. If P is a polygonal presentation, deﬁne the Euler char-
acteristic of P to be V −E + F, where V is the number of vertices (after
identiﬁcations), E is the number of edge symbols (which is equal to the
number of edges after identiﬁcations), and F is the number of faces. If P
is the presentation determined by a 2-dimensional simplicial complex, it is
easy to check that this deﬁnition agrees with the deﬁnition given in Chapter
5.
Theorem 6.17. The Euler characteristic of a polygonal presentation is
unchanged by elementary transformations.
Proof. It is obvious that relabeling, rotating, and reﬂecting do not change
the Euler characteristic of a presentation, because they leave the numbers

Combinatorial Invariants
143
of vertices, edges, and faces individually unchanged. For the other trans-
formations, we need only check that the changes to these three numbers
cancel out. Subdividing increases both the number of edges and the number
of vertices by one, leaving the number of faces unchanged. Cutting increases
both the number of edges and the number of faces by one, and leaves the
number of vertices unchanged. Unfolding increases the number of edges and
the number of vertices by one, and leaves the number of faces unchanged.
Finally, consolidating, pasting, and folding leave the Euler characteristic
unchanged, since they are the inverses of subdividing, cutting, and unfold-
ing, respectively.
Proposition 6.18 (Euler Characteristics of Compact Surfaces).
The Euler characteristic of a standard surface presentation is equal to
(a) 2 for the sphere;
(b) 2 −2n for the connected sum of n tori;
(c) 2 −n for the connected sum of n projective planes.
Proof. Just compute.
These results allows us to conclude a great deal about a surface from a
given presentation, without actually carrying out the reduction to a stan-
dard presentation. For example, any presentation with Euler characteristic
2 gives the sphere, and a presentation with Euler characteristic 0 gives
either the torus or the Klein bottle ≈P2 # P2.
At the moment, we do not know that the Euler characteristic is a topo-
logical invariant, for the simple reason that we still do not know that the
standard surfaces on our list are not homeomorphic to each other. (If you
do not believe this, just try to prove, for example, that the projective plane
is not homeomorphic to the torus using the techniques we have developed
so far!) The problem is that we cannot yet rule out the possibility that P2,
say, could have a presentation that is so exotic that it is not related to the
standard one by a series of elementary transformations, but somehow man-
ages to reduce to a presentation of the torus after following the algorithm
of the classiﬁcation theorem. We will remedy this deﬁciency in Chapter 10,
when we show that all of our standard compact surfaces are topologically
distinct; only then will we be able to complete the classiﬁcation of compact
surfaces.
The Euler characteristic can be used by itself to distinguish presentations
that reduce to connected sums of diﬀerent numbers of tori or connected
sums of diﬀerent numbers of projective planes. However, to distinguish a
presentation of the connected sum of n tori from one of the connected sum
of 2n projective planes (for example, the torus from the Klein bottle), we
will need one more property: orientability.

144
6. Curves and Surfaces
Orientability
In Chapter 5 we introduced the notion of orientation of a simplicial com-
plex. In this section we show how to extend it to polygonal presentations.
Note that a permutation of a set with three elements is even if and only
if it is a cyclic permutation (i.e., of the form i 
→j 
→k 
→i). Thus an
orientation of a 2-simplex is just an equivalence class of vertex orderings
modulo cyclic permutations. Suppose P is a surface presentation arising
from a simplicial complex, so that every word has length 3. Each word
determines an orientation of the associated 2-simplex, by ordering the ver-
tices in counterclockwise order. It is easy to check that when two simplices
are glued together via an edge pairing, their orientations are consistent if
and only if the edge pair is complementary. Motivated by this, we make
the following deﬁnition. A surface presentation P is said to be oriented if
it has no twisted edge pairs. Intuitively, this means that you can decide
which is the “front” side (or “outside”) of |P| by coloring the top surface of
each polygon white and the bottom side gray; the condition on edge pairs
ensures that the colors will match up when edges are pasted together.
A compact surface is said to be orientable if it admits an oriented pre-
sentation. By looking a little more closely at the proof of the classiﬁcation
theorem, we can identify exactly which compact surfaces are orientable.
Proposition 6.19. A compact surface is orientable if and only if it is
homeomorphic to the sphere or a connected sum of one or more tori.
Proof. The standard presentations of the sphere and the connected sums
of tori are oriented, so these surfaces are certainly orientable. To show that
an orientable surface is homeomorphic to one of these, let M be any sur-
face that admits at least one orientable presentation. Starting with that
presentation, follow the algorithm described in the proof of the classiﬁ-
cation theorem to transform it to one of the standard presentations. The
only elementary transformation that can introduce a twisted pair into an
oriented presentation is reﬂection. The only steps in which reﬂections are
used are Steps 3, 4, and 7, and you can check that none of those steps
require any reﬂections if there were no twisted pairs to begin with. Thus
the classiﬁcation theorem tells us that the presentation can be reduced to
one of the standard ones with no twisted pairs, which means that M is
homeomorphic to a sphere or a connected sum of tori.
Because of this result, the connected sum of n tori is also known as the
orientable surface of genus n, and the connected sum of n projective planes
is called the nonorientable surface of genus n. By convention, the sphere is
the (unique, orientable) surface of genus 0. Technically, this terminology is
premature, because we still do not know that a connected sum of projective
planes is not homeomorphic to an oriented surface. But for now we will
go ahead and use this standard terminology with the caveat that all we

Combinatorial Invariants
145
know about the “nonorientable surface of genus n” is that its standard
presentation is not oriented.
Before moving away from classiﬁcation theorems, it is worth remarking
on the situation with higher-dimensional manifolds. Because of the triangu-
lation theorem for 3-manifolds stated in Chapter 5, one might hope that a
similar approach to classifying 3-manifolds might bear fruit. Unfortunately,
the combinatorial problem of reducing any given 3-manifold triangulation
to some standard form is, so far, unsolved. And this approach cannot get
us very far in dimensions higher than 3, because we do not have trian-
gulation theorems. Thus, in order to make any progress in understanding
higher-dimensional manifolds, as well as to resolve the question of whether
the standard surfaces are distinct, we will need to develop more powerful
tools. This we will do in the remainder of the book.

146
6. Curves and Surfaces
Problems
6-1. For each of the following surface presentations, compute the Euler
characteristic, and then apply the algorithm of the classiﬁcation the-
orem to determine which of our standard surfaces it is.
(a) ⟨a, b, c | abacb−1c−1⟩.
(b) ⟨a, b, c | abca−1b−1c−1⟩.
(c) ⟨a, b, c, d, e, f | abc, bde, c−1df, e−1fa⟩.
(d) ⟨a, b, c, d, e, f, g, h, i, j, k, l, m, n, o |
abc, bde, dfg, fhi, haj, c−1kl, e−1mn,
g−1ok−1, i−1l−1m−1, j−1n−1o−1⟩.
6-2. Show that a connected sum of one or more projective planes contains
a subspace that is homeomorphic to the M¨obius band.
6-3. Show that the projective plane is homeomorphic to the quotient ob-
tained by gluing a M¨obius band and a disk together along their com-
mon boundary.
6-4. Show that the Klein bottle is homeomorphic to the quotient obtained
by gluing two M¨obius bands together along their common boundary.

7
[[Homotopy]] and the Fundamental
Group
The results of the preceding chapter left a serious gap in our attempt to
classify compact 2-manifolds up to homeomorphism: Although we have
exhibited a list of surfaces and shown that every compact, connected surface
is homeomorphic to one on the list, we still have no way of knowing when
two surfaces are not homeomorphic. For all we know, all the surfaces on
our list might be homeomorphic to the sphere! (Think, for example, of the
unexpected homeomorphism between P2 # P2 # P2 and T2 # P2.)
To distinguish nonhomeomorphic surfaces, we need topological invari-
ants. For some surfaces, the properties we already know suﬃce. For exam-
ple, the 2-sphere is not homeomorphic to the plane because one is compact,
while the other is not. The plane, the disjoint union of two planes, and the
disjoint union of three planes are all topologically distinct, because they
have diﬀerent numbers of components. It follows from Problem 4-1 that
the line is not homeomorphic to the plane; the proof involved a rather sub-
tle use of connectedness. But to decide whether, for example, the sphere is
homeomorphic to the torus, or the plane is homeomorphic to the punctured
plane R2 ∖{0}, we need to introduce some new invariants.
In this chapter we begin our study of the fundamental group, an algebraic
group that measures the number of “holes” in a space, in a certain sense. To
set the stage, let us think about the diﬀerence between the plane and the
punctured plane. Both are connected, noncompact 2-manifolds, so they
cannot be distinguished by any of the basic topological properties that
we have discussed so far. Yet intuition suggests that they should not be
homeomorphic to each other because the punctured plane has a “hole,”
while the full plane does not.

148
7. [[Homotopy]] and the Fundamental Group
To see how this distinction might be detected topologically, observe that
every closed curve in R2 can be continuously shrunk to a point (you will
prove this rigorously in Exercise 7.3 below); by contrast, it is intuitively
clear that a circle drawn around the hole in the space R2 ∖{0} can never
be continuously shrunk to a point while remaining in the space, and in fact
cannot be deformed into any closed path that does not go around the hole.
We will deﬁne an equivalence relation on closed paths with a ﬁxed start-
ing and ending point: Two paths are equivalent if one can be continuously
deformed into the other while keeping the starting and ending point ﬁxed.
The set of equivalence classes is called the fundamental group of the space;
the product of two elements of the group is obtained by ﬁrst following one
path and then the other. After making the basic deﬁnitions, we will prove
that homeomorphic spaces have isomorphic fundamental groups. Then we
will prove that the fundamental group satisﬁes an even stronger invariance
property, that of homotopy invariance. As a consequence, we will be able
to reduce the computations of fundamental groups of many spaces to those
of simpler ones.
Proving that the fundamental group of a space is not trivial turns out to
be somewhat harder, and we will not do so until the next chapter.
[[Homotopy]]
Let X and Y be topological spaces, and let f, g: X →Y be continuous
maps. A homotopy from f to g is a continuous map H : X × I →Y (where
I = [0, 1] is the unit interval) such that for all x ∈X,
H(x, 0) = f(x);
H(x, 1) = g(x).
(7.1)
If there exists a homotopy from f to g, we say that f and g are homo-
topic, and write f ≃g (or H : f ≃g if we want to emphasize the speciﬁc
homotopy).
A homotopy deﬁnes a one-parameter family of maps Ht(x) = H(x, t) for
0 ≤t ≤1 (Figure 7.1), and condition (7.1) says that H0 = f and H1 = g.
We usually think of the parameter t as time, and think of H as giving
a “deformation” of f into g as t goes from 0 to 1. The continuity of H
guarantees that this deformation proceeds continuously without breaks or
jumps.
Lemma 7.1. For any topological spaces X and Y , homotopy is an equiv-
alence relation on the set of all continuous maps from X to Y .
Proof. Any map f is homotopic to itself via the trivial homotopy H(x, t) =
f(x), so homotopy is reﬂexive. Similarly, if H : f ≃g, then a homotopy
from g to f is given by H(x, t) = H(x, 1 −t), so homotopy is symmetric.
Finally, if F : f ≃g and G: g ≃h, deﬁne H : X × I →Y by following F at

[[Homotopy]]
149
H
f0
f1
X × I
Y
FIGURE 7.1. A homotopy between f0 and f1.
double speed for 0 ≤t ≤1
2, and then following G at double speed for the
remainder of the unit interval. Formally,
H(x, t) =

F(x, 2t),
0 ≤t ≤1
2;
G(x, 2t −1),
1
2 ≤t ≤1.
Since F(x, 1) = g(x) = G(x, 0), the two deﬁnitions of H agree at t =
1
2, where they overlap. Thus H is continuous by the gluing lemma, and
is therefore a homotopy between f and h. This shows that homotopy is
transitive.
Lemma 7.2. The homotopy relation is preserved by composition: If
f0, f1 : X →Y
and
g0, g1 : Y →Z
are continuous maps with f0 ≃f1 and g0 ≃g1, then g0 ◦f0 ≃g1 ◦f1.
Proof. Suppose F : f0 ≃f1 and G: g0 ≃g1 are homotopies. Deﬁne H : X ×
I →Z by H(x, t) = G(F(x, t), t). At t = 0, H(x, 0) = G(f0(x), 0) =
g0(f0(x)), and at t = 1, H(x, 1) = G(f1(x), 1) = g1(f1(x)). Thus H is a
homotopy from g0 ◦f0 to g1 ◦f1.
Example 7.3. Deﬁne maps f : R →R2 by
f(x) = (x, x2);
g(x) = (x, x).
Then the map H(x, t) = (x, x2 −tx2 + tx) is a homotopy from f to g.
Example 7.4. Let B ⊂Rn and let X be any topological space. Suppose
f, g: X →B are any two continuous maps with the property that for all

150
7. [[Homotopy]] and the Fundamental Group
X × I
B
Rn
FIGURE 7.2. A straight-line homotopy.
x ∈X, the line segment from f(x) to g(x) lies in B. This will be the case,
for example, if B is convex. Deﬁne a homotopy H : f ≃g by letting H(x, t)
trace out the line segment from f(x) to g(x) at constant speed as t goes
from 0 to 1 (Figure 7.2):
H(x, t) = (1 −t)f(x) + tg(x).
This is called the straight-line homotopy between f and g. It shows, in
particular, that all maps from a given space into a convex set are homotopic.
The Fundamental Group
Recall that a path in a topological space X is a continuous map f : I →X.
The points p = f(0) and q = f(1) are called the initial point and terminal
point of f, respectively, and we say that f is a path “from p to q.” We will
use paths to detect “holes” in a space.
Example 7.5. Consider the path α: I →R2 ∖{0} deﬁned (in complex
notation) by
α(s) = e2πis
and the map H : I × I →R2 ∖{0} by
H(s, t) = e2πist.
At each time t, Ht is a path that follows the circle only as far as angle 2πt,
so H0 is the constant path c1(s) ≡1 and H1 = α. Thus H is a homotopy
from the constant path to α.

The Fundamental Group
151
This last example shows that the circular path around the origin is ho-
motopic in R2 ∖{0} to a constant path, so that simply asking whether
a closed path is homotopic to a constant is not suﬃcient to detect holes.
To remedy this, we will need to consider homotopies of paths throughout
which the endpoints stay ﬁxed. More generally, it will be useful to consider
homotopies that ﬁx an arbitrary subset of the domain.
Let X and Y be topological spaces, and A ⊂X an arbitrary subspace.
A homotopy H between maps f, g: X →Y is called a homotopy relative
to A if
H(x, t) = f(x)
for all x ∈A, t ∈I.
In other words, for each t, the map Ht agrees with f on A. If there exists
such a homotopy, we say that f and g are homotopic relative to A and
write f ≃A g. Notice that this implies g|A = H1|A = f|A, so for two maps
to be homotopic relative to A they must ﬁrst of all agree on A.
Now suppose f and g are two paths in X. A path homotopy from f to g is
a homotopy relative to {0, 1}, that is, a homotopy that ﬁxes the endpoints
for all time. If there exists a path homotopy between f and g, we say they
are path homotopic, and write f ∼g. By the remark above, this is possible
only if f and g both have the same initial point and the same terminal
point.
Lemma 7.6. For any points p, q ∈X, path homotopy is an equivalence
relation on the set of all paths from p to q.
Exercise 7.1.
Prove Lemma 7.6.
For any path f in X, we denote the path homotopy equivalence class of
f by [f], and call it the path class of f. For our purposes, we will be most
interested in paths that start and end at the same point. Such a path is
called a loop. If f is a loop whose initial and terminal point is q ∈X, we say
that f is based at q, and we call q the base point of f. The set of all loops
in X based at q is denoted by Ω(X, q). The constant loop cq ∈Ω(X, q) is
the map cq(s) ≡q. If a loop is path homotopic to the constant loop, we
say that it is null homotopic.
One (not very interesting, but sometimes useful) way to get homotopic
paths is by the following construction. A reparametrization of a path f : I →
X is a path of the form f ◦ϕ for some homeomorphism ϕ: I →I ﬁxing 0
and 1.
Lemma 7.7. Any reparametrization of a path f is path homotopic to f.
Proof. Suppose f ◦ϕ is a reparametrization of f, and let H : I × I →I
denote the straight-line homotopy from the identity map to ϕ. Then f ◦H
is a homotopy from f to f ◦ϕ.

152
7. [[Homotopy]] and the Fundamental Group
F
G
H
s
t
f0
f0
f1
f1
g0
g0
g1
g1
FIGURE 7.3. [[Homotopy]] invariance of path multiplication.
Lemma 7.6 says that path homotopy is an equivalence relation on
Ω(X, q). We deﬁne the fundamental group of X based at q, denoted by
π1(X, q), to be the set of path classes of loops based at q.
To make π1(X, q) into a group, we must deﬁne a multiplication operation.
This is done ﬁrst on the level of paths: The product of two paths f and
g is the path obtained by ﬁrst following f and then following g, both at
double speed. For future use, we will deﬁne products of paths in a more
general setting—instead of requiring that both paths start and end at the
same point, we will require simply that the second one start where the ﬁrst
ends.
Thus let f, g: I →X be paths with f(1) = g(0). We deﬁne their product
f · g: I →X by
f · g(s) =

f(2s);
0 ≤s ≤1
2;
g(2s −1);
1
2 ≤s ≤1.
(Here and throughout the book we will consistently use s as the “space
variable” parametrizing individual paths, and reserve t for the “time vari-
able” in homotopies.) The condition f(1) = g(0) guarantees that f · g is
continuous by the gluing lemma.
Lemma 7.8 ([[Homotopy]] Invariance of Path Multiplication).
Path
multiplication is well-deﬁned on path classes. More precisely, if f0 ∼f1 and
g0 ∼g1, and if f0 · g0 is deﬁned (that is, if f0(1) = g0(0)), then f1 · g1 is
also deﬁned and f0 · g0 ∼f1 · g1.
Proof. Let F : f0 ∼f1 and G: g0 ∼g1 be homotopies (Figure 7.3). The
required homotopy H : f0 · g0 ∼f1 · g1 is given by
H(s, t) =

F(2s, t);
0 ≤s ≤1
2, 0 ≤t ≤1;
G(2s −1, t);
1
2 ≤s ≤1, 0 ≤t ≤1.

The Fundamental Group
153
s
t
p
cp
f
f
FIGURE 7.4. f ∼cp · f.
s
t
cp
f
f −1
FIGURE 7.5. cp ∼f · f −1.
Again, this is continuous by the gluing lemma.
With this result, it makes sense to deﬁne multiplication of path classes by
setting [f]· [g] = [f · g] whenever f · g is deﬁned. In particular, it is always
deﬁned for [f], [g] ∈π1(X, q). We wish to show that π1(X, q) is a group
under this multiplication, which amounts to proving associativity of path
class multiplication and the existence of an identity and inverses. Again, it
will be useful to prove these properties in a slightly more general setting,
for paths that do not necessarily have the same initial and terminal points.
For any path f, we deﬁne the reverse path f −1 by f −1(s) = f(1 −s); this
just retraces f from its terminal point to its initial point. Recall that cq
denotes the constant loop at q.
Theorem 7.9 (Properties of Path Multiplication).
Let f be any
path from p to q in a space X, and let g and h be any paths in X. Path
multiplication satisﬁes the following properties:
(a) [cp] · [f] = [f] · [cq] = [f].
(b) [f] · [f −1] = [cp]; [f −1] · [f] = [cq].
(c) [f] · ([g] · [h]) = ([f] · [g]) · [h] whenever either side is deﬁned.
Proof. For (a), let us show that cp·f ∼f; the product the other way works
similarly. Deﬁne H : I × I →X (Figure 7.4) by
H(s, t) =
⎧
⎨
⎩
p,
t ≥2s;
f
2s −t
2 −t

,
t ≤2s.
Geometrically, this maps the portion of the square on the left of the line
t = 2s to the point p, while it maps the portion on the right along the
path f at increasing speeds as t goes from 0 to 1. (The slanted lines in the
picture are the level sets of H, i.e., the lines along which H takes the same

154
7. [[Homotopy]] and the Fundamental Group
value.) This map is continuous by the gluing lemma, and you can check
that H(s, 0) = f(s) and H(s, 1) = cp · f(s). Thus H : f ∼cp · f.
For (b), we will just show that f·f −1 ∼cp. Since (f −1)−1 = f, the other
relation follows by interchanging the roles of f and f −1. Deﬁne a homotopy
H : cp ∼f · f −1 by the following recipe (Figure 7.5): At any time t, the
path Ht follows f as far as f(t) at double speed while the parameter s is
in the interval [0, t/2]; then for s ∈[t/2, 1 −t/2] it stays at f(t); then it
retraces f at double speed back to q. Formally,
H(s, t) =
⎧
⎪
⎨
⎪
⎩
f(2s),
0 ≤s ≤t/2;
f(t),
t/2 ≤s ≤1 −t/2;
f(2 −2s)
1 −t/2 ≤s ≤1.
It is easy to check that H is a homotopy from cp to f · f −1.
Finally, to prove associativity, we need to show that (f·g)·h ∼f·(g·h).
The ﬁrst path follows f and then g at quadruple speed for s ∈[0, 1
2], and
then follows h at double speed for s ∈[ 1
2, 1], while the second follows f
at double speed and then g and h at quadruple speed. The two paths are
therefore reparametrizations of each other and thus homotopic.
Corollary 7.10. For any space X and any point q ∈X, π1(X, q) is a
group.
Note that path multiplication is not associative on the level of paths,
only on the level of path homotopy classes. For deﬁniteness, let us agree to
interpret products of more than two paths as being grouped from left to
right if no parentheses are present, so that f · g · h means (f · g) · h.
The next question we need to address is how the fundamental group
depends on the choice of base point. The ﬁrst thing to notice is that if
X is not path connected, we cannot expect the fundamental groups based
at points in diﬀerent path components to have any relationship to each
other; π1(X, q) can give us information only about the path component
containing q. Therefore, the fundamental group is usually used only to
study path connected spaces. When X is path connected, it turns out that
the fundamental groups at diﬀerent points are all isomorphic; the next
theorem gives an explicit isomorphism between them.
Theorem 7.11 (Change of Base Point).
Suppose X
is path con-
nected, p, q ∈X, and g is any path from p to q. The map Φg : π1(X, p) →
π1(X, q) deﬁned by
Φg[f] = [g−1] · [f] · [g]
is an isomorphism.
Proof. Before we begin, we should verify that Φg makes sense (Figure 7.6):

The Fundamental Group
155
f
g
p
q
FIGURE 7.6. Change of base point.
Since g goes from p to q and f goes from p to p, paths in the class [g−1] ·
[f] · [g] go from q to p (by g−1), then from p to p (by f), and then from p
back to q (by g), so Φg(f) does indeed deﬁne an element of π1(X, q).
To check that Φg is a group homomorphism, use Theorem 7.9:
Φg[f1] · Φg[f2]
= [g−1] · [f1] · [g] · [g−1] · [f2] · [g]
= [g−1] · [f1] · [cp] · [f2] · [g]
= [g−1] · [f1] · [f2] · [g]
= Φg([f1] · [f2]).
(This is one reason why we needed to prove the properties of Theorem 7.9
for paths that start and end at diﬀerent points.)
Finally, the fact that Φg is an isomorphism follows easily from the fact
that it has an inverse, given by Φg−1 : π1(X, q) →π1(X, p).
Because of this theorem, when X is path connected we sometimes use
the imprecise notation π1(X) to refer to the fundamental group of X with
respect to an unspeciﬁed base point, if the base point is irrelevant. For ex-
ample, we might say “π1(X) is trivial” if π1(X, q) = {[cq]} for any q ∈X;
or we might say “π1(X) ∼= Z” if there exists an isomorphism π1(X, q) →Z
for some (hence any) q. However, we cannot dispense with the base point
altogether: Since diﬀerent paths from p to q may give rise to diﬀerent iso-
morphisms, when we need to refer to a speciﬁc element of the fundamental
group, or to a speciﬁc homomorphism between fundamental groups, we
must be careful to specify all base points.

156
7. [[Homotopy]] and the Fundamental Group
F
X
I × I
f
g
h
k
FIGURE 7.7. The map of Lemma 7.12.
If X is path connected and π1(X) is trivial, we say that X is simply
connected. This means that every loop in X can be continuously shrunk to
a constant loop while its endpoints are kept ﬁxed.
Exercise 7.2.
Let X be a topological space.
(a) Let f, g: I →X be two paths from p to q. Show that f ∼g if and only
if f · g−1 ∼cp.
(b) Show that X is simply connected if and only if any two paths in X
with the same initial and terminal points are path homotopic.
Exercise 7.3.
Show that any convex subset of Rn is simply connected.
In particular, Exercise 7.3 shows that the plane is simply connected. We
will see later that the punctured plane is not, thus proving that the two
spaces are not homeomorphic. In fact, we will show that both R2 ∖{0} and
S1 have inﬁnite cyclic fundamental groups, generated by the path class of
a loop that winds once around the origin. The proof will occupy most of
our eﬀorts for the remainder of this chapter and the next.
Lemma 7.12. Let F : I × I →X be a continuous map, and let f, g, h,
and k be the paths in X deﬁned by
f(s) = F(s, 0);
g(s) = F(1, s);
h(s) = F(0, s);
k(s) = F(s, 1).
(See Figure 7.7.) Then f · g ∼h · k.
Exercise 7.4.
Prove Lemma 7.12.
Consider now the loop α: I →S1 given by α(s) = e2πis. This map wraps
the interval once around the circle counterclockwise, and maps 0 and 1 to

The Fundamental Group
157
0
1
1
f
f
q
α
X
FIGURE 7.8. The circle representative of a loop.
the base point 1 ∈S1. By the closed map lemma, it is a quotient map. If
f : I →X is any loop in a space X, it passes to the quotient to give a
unique map f : S1 →X such that f ◦α = f (Figure 7.8), which we call
the circle representative of f. Conversely, any continuous map f from the
circle to X is the circle representative of the map f = f ◦α.
The next proposition gives a convenient criterion for detecting null ho-
motopic loops in terms of their circle representatives.
Proposition 7.13. A loop in a space X is null homotopic if and only if
its circle representative extends to a map from the closed disk into X.
Proof. Let f : I →X be a loop based at q ∈X, and f : S1 →X its circle
representative. Suppose ﬁrst that f extends to a map F : B2 →X. Since
B2 is convex, the loop α is null homotopic when thought of as a loop in B2.
Let A: I × I →B2 be a path homotopy from α to the constant loop c1.
Because A(s, t) ∈S1 when t = 0 or 1, the composite map F ◦A: I ×I →X
satisﬁes
F ◦A(s, 0) = f ◦A(s, 0) = f ◦α(s) = f(s),
F ◦A(s, 1) = f ◦A(s, 1) = f ◦c1(s) = f(1) = q,
and is therefore a homotopy from f to cq.
Conversely, suppose f is null homotopic, and let H : I × I →X be a
homotopy from cq to f. Observe that H sends the sides and bottom of the
square to the point q. We will show below that there is a quotient map
π: I × I →B2 that sends these three sides to 1 ∈S1, makes no other
identiﬁcations, and restricts to α on the top side I × {1}. Granting this
for the moment, the homotopy H passes to the quotient to give a map

158
7. [[Homotopy]] and the Fundamental Group
a
a
b
b
c
c
d
d
e
e
h
h
A
B
C
FIGURE 7.9. A quotient map sending three sides of the square to a point.
H : B2 →X satisfying H ◦π = H. The restriction of H to the circle is
clearly the circle representative of f, so H is the desired extension.
We will construct the claimed quotient map π: I × I →B2 in several
steps. Let T be an equilateral triangle of altitude 2 in the plane. Triangulate
I × I and T as shown in Figure 7.9, and let A: I × I →T be the simplicial
homeomorphism determined by the indicated vertex map. Then let B : T →
B2 be the (nonsimplicial) map that sends each horizontal line segment in
T linearly onto the horizontal segment at the same height in the disk. The
resulting composite map B ◦A is a quotient map by the closed map lemma,
and it identiﬁes the sides and bottom of the square to a point but makes
no other identiﬁcations. It is not quite the map we are seeking, because it
takes the sides and bottom to −i instead of 1, and maps the top interval
around the circle in the wrong direction. A suitable rotation and reﬂection
of the disk, which we denote by C, corrects these problems. Let β : I →S1
denote the restriction of C ◦B ◦A to the top segment I ×{1} of the square
(identiﬁed with I). Although β is still not equal to α, the two maps diﬀer
only by a homeomorphism of S1 (since both α and β are quotient maps
that make the same identiﬁcations). This homeomorphism extends to a
homeomorphism of the closed disk by Problem 4-9, and composing with
the inverse of this homeomorphism yields the desired map.
Homomorphisms Induced by Continuous Maps
In this section we explore the eﬀect of a continuous map on the fundamental
groups of its domain and range. The ﬁrst thing we need to know is that
continuous maps preserve the path homotopy relation.
Lemma 7.14. The path homotopy relation is preserved by composition
with continuous maps. That is, if f0, f1 : I →X are path homotopic and
ϕ: X →Y is continuous, then ϕ ◦f0 and ϕ ◦f1 are path homotopic.
Exercise 7.5.
Prove Lemma 7.14

Homomorphisms Induced by Continuous Maps
159
An immediate consequence of this lemma is that any continuous map
ϕ: X →Y induces a well-deﬁned map ϕ∗: π1(X, q) →π1(Y, ϕ(q)) simply
by setting ϕ∗[f] = [ϕ ◦f].
Lemma 7.15. For any continuous map ϕ, ϕ∗is a group homomorphism.
Proof. Just note that
ϕ∗([f] · [g]) = ϕ∗[f · g] = [ϕ ◦(f · g)].
Thus it suﬃces to show that ϕ◦(f ·g) = (ϕ◦f)·(ϕ◦g). This is immediate,
because expanding both sides using the deﬁnition of path multiplication
results in identical formulas.
The homomorphism ϕ∗: π1(X, q) →π1(Y, ϕ(q)) is called the homomor-
phism induced by ϕ. It has the following properties:
Proposition 7.16 (Properties of the Induced Homomorphism).
(a) Let ϕ: X →Y and ψ: Y →Z be continuous maps. Then (ψ ◦ϕ)∗=
ψ∗◦ϕ∗.
(b) If IdX : X →X denotes the identity map of X, then for any q ∈X,
(IdX)∗is the identity map of π1(X, q).
Proof. Compute:
ψ∗(ϕ∗[f]) = ψ∗[ϕ ◦f] = [ψ ◦ϕ ◦f] = (ψ ◦ϕ)∗[f];
(IdX)∗[f] = [IdX ◦f] = [f].
Corollary 7.17 (Topological Invariance of π1).
Homeomorphic
spaces have isomorphic fundamental groups. Speciﬁcally, if ϕ: X →Y is
a homeomorphism, then ϕ∗: π1(X, q) →π1(Y, ϕ(q)) is an isomorphism.
Proof. If ϕ is a homeomorphism, then (ϕ−1)∗◦ϕ∗= (ϕ−1 ◦ϕ)∗= (IdX)∗=
Idπ1(X,q), and similarly ϕ∗◦(ϕ−1)∗is the identity on π1(Y, ϕ(q)).
Be warned that injectivity or surjectivity of a continuous map does not
necessarily imply that the induced homomorphism has the same property.
For example, accepting for the moment the fact that π1(S1) is inﬁnite cyclic
(we will prove it in the next chapter), the inclusion map S1 	→R2 is injec-
tive, but its induced homomorphism is not, while the map ϕ: [0, 1) →S1
of Exercise 2.7 that wraps the interval once around the circle is surjective
(in fact bijective), but its induced homeomorphism is the trivial homomor-
phism because [0, 1) is convex and therefore simply connected.

160
7. [[Homotopy]] and the Fundamental Group
A
FIGURE 7.10. S1 is a retract of T2.
E
B
FIGURE 7.11. Figure eight space.
There is, however, one case in which the homomorphism induced by
inclusion can be easily shown to be injective. Let X be a space and A ⊂
X a subspace. A continuous map r: X →A is called a retraction if the
restriction of r to A is the identity map of A, or equivalently if r◦ιA = IdA,
where ιA : A 	→X is the inclusion map. If there exists a retraction from X
to A, we say that A is a retract of X.
Proposition 7.18. Suppose A is a retract of X. If r: X →A is any
retraction, then for any q ∈A, (ιA)∗: π1(A, q) →π1(X, q) is injective and
r∗: π1(X, q) →π1(A, q) is surjective.
Proof. Since r ◦ιA = IdA, r∗◦(ιA)∗is the identity on π1(A, q), from which
it follows that (ιA)∗is injective and r∗is surjective.
Here are some examples of retractions. For these examples we will use
without proof the fact that the fundamental group of the circle is inﬁnite
cyclic.
Example 7.19. It is easy to check that the map r: Rn+1 ∖{0} →Sn
given by r(x) = x/|x| is a retraction. Thus the homomorphism π1(Sn) →
π1(Rn+1 ∖{0}) induced by inclusion is injective. In particular, in the case
n = 1, this means that π1(R2 ∖{0}) has an inﬁnite cyclic subgroup.
Example 7.20. The torus T2 = S1 × S1 has a subspace A = S1 × {1}
homeomorphic to S1 (Figure 7.10), and the map r: T2 →A given by
r(p, q) = (p, 1) is easily seen to be a retraction. Thus the image of the
map (ιA)∗: π1(S1) →π1(T2) is an inﬁnite cyclic subgroup of π1(T2).
Example 7.21. Consider the ﬁgure eight space E ⊂R2 (Figure 7.11),
which is the union of the circles of radius 1 around (0, 1) and (0, −1).
Let B denote the upper circle. There are at least two diﬀerent retractions
of E onto B—one that maps the entire lower circle to the origin and is the
identity on B, and another that “folds” the lower circle onto the upper one
(formally, (x, y) 
→(x, |y|)). Thus π1(E) has an inﬁnite cyclic subgroup.

[[Homotopy]] Equivalence
161
[[Homotopy]] Equivalence
Although retractions are sometimes useful tools for showing that a certain
fundamental group is not trivial, it is much more useful to have a criterion
under which a continuous map induces an isomorphism of fundamental
groups. In this section we explore a very general such criterion.
Let ϕ: X →Y be a continuous map. We say that another continuous
map ψ: Y →X is a homotopy inverse for ϕ if ψ◦ϕ ≃IdX and ϕ◦ψ ≃IdY .
If there exists a homotopy inverse for ϕ, ϕ is called a homotopy equivalence.
In this case, we say that X is homotopy equivalent to Y , or X has the same
homotopy type as Y , and we write X ≃Y .
Lemma 7.22. [[Homotopy]] equivalence is an equivalence relation.
Exercise 7.6.
Prove Lemma 7.22.
One kind of homotopy equivalence is relatively easy to visualize. A sub-
space A ⊂X is said to be a deformation retract of X if there exists a
retraction r: X →A such that the identity of X is homotopic to ιA ◦r.
The homotopy H : IdX ≃ιA ◦r is called a deformation retraction. Intu-
itively, this means that X can be continuously deformed into A in such a
way that points in A end up where they started. We say that A is a strong
deformation retract of X if in addition IdX ≃A (ιA ◦r), which means that
points in A remain ﬁxed throughout the deformation. In this case, the
homotopy H can be called a strong deformation retraction.
Example 7.23. In Example 7.19 we showed that Sn is a retract of Rn+1 ∖
{0}. In fact, it is a strong deformation retract: The deformation retraction
is given by H : (Rn+1 ∖{0}) × I →Rn+1 ∖{0}, where
H(x, t) = (1 −t)x + t x
|x|.
This is just the straight-line homotopy from the identity map to the retrac-
tion onto the sphere (Figure 7.12).
If A is a deformation retract of X, since ιA ◦r ≃IdX and r ◦ιA = IdA,
the inclusion A 	→X is a homotopy equivalence.
Our main goal in this section is the following theorem, which is a much
stronger invariance property than homeomorphism invariance, and will en-
able us to compute the fundamental groups of many more spaces.
Theorem 7.24 ([[Homotopy]] Invariance of π1).
If ϕ: X →Y is a ho-
motopy equivalence, then for any point q ∈X, ϕ∗: π1(X, q) →π1(Y, ϕ(q))
is an isomorphism.
Before proving the theorem, let us look at several important examples.
Example 7.25. Let X be any space. If the identity map of X is homo-
topic to a constant map, we say that X is contractible. Other equivalent

162
7. [[Homotopy]] and the Fundamental Group
FIGURE 7.12. Strong deformation retraction of R2 ∖{0} onto S1.
deﬁnitions are that any point of X is a deformation retract of X, or X is
homotopy equivalent to a one-point space (Exercise 7.7). Concretely, con-
tractibility means that there exists a continuous map H : X × I →X such
that
H(x, 0) = x for all x ∈X;
H(x, 1) = q for all x ∈X.
In other words, the whole space X can be continuously shrunk to a point.
Some obvious examples of contractible spaces are convex subsets of Rn,
and, more generally, any subset B ⊂Rn that is star-shaped, which means
that there is some point q0 ∈B such that for every q ∈B, the line segment
from q0 to q is contained in B. Since a one-point space is simply connected,
it follows that every contractible space is simply connected.
Exercise 7.7.
Show that the following are equivalent:
(a) X is contractible.
(b) X is homotopy equivalent to a one-point space.
(c) Any point of X is a deformation retract of X.
Example 7.26. Example 7.23 showed that the circle is a strong deforma-
tion retract of R2 ∖{0}. Therefore, inclusion S1 	→R2 ∖{0} induces an
isomorphism of fundamental groups. Once we show that π1(S1) is inﬁnite
cyclic, this will characterize π1(R2 ∖{0}) as well.
Example 7.27. The ﬁgure eight space E of Example 7.21 and the theta
space, deﬁned by
Θ = {(x, y) ∈R2 : x2 + y2 = 4, or y = 0 and −2 ≤x ≤2},

[[Homotopy]] Equivalence
163
FIGURE 7.13. Deformation retractions onto E and Θ.
FIGURE 7.14. A tree.
FIGURE 7.15. Not a tree.
are both strong deformation retracts of R2 with the two points (0, 1) and
(0, −1) removed. The deformation retractions, indicated schematically in
Figure 7.13, are deﬁned by carving the space up into regions in which
straight-line homotopies are easily deﬁned; the resulting maps are con-
tinuous by the gluing lemma. Therefore, since homotopy equivalence is
transitive, E and Θ are homotopy equivalent to each other.
Example 7.28 (Finite Trees). Let Γ be a graph. A cycle in Γ is a closed
ﬁnite edge path, that is, an edge path (v0, . . . , vn) such that v0 = vn. A tree
is a connected graph that contains no reduced cycles (see Figures 7.14 and
7.15). We will show that any ﬁnite tree T is contractible and thus simply
connected.
The proof is by induction on the number of edges in T. If there is only one
edge, then T is homeomorphic to a closed interval in R, which is convex and
therefore contractible. So suppose every tree with n edges is contractible,
and let T be a tree with n + 1 edges.

164
7. [[Homotopy]] and the Fundamental Group
T0
v0
v1
FIGURE 7.16. Proof that a tree is contractible.
If every vertex in T lies on at least two edges, then arguing as in the proof
of the classiﬁcation theorem for 1-manifolds (Theorem 6.1), there must be
an inﬁnite reduced edge path {vi : i ∈Z} in T. Because T is ﬁnite, there
must be some integers n and n+k > n such that vn = vn+k. If n and k are
chosen so that k is the minimum positive integer with this property, this
means that (vn, . . . , vn+k) is a reduced cycle, contradicting the assumption
that T is a tree. Thus there must be at least one vertex v0 that lies on only
one edge. Since T is connected, v0 lies on exactly one edge, say ⟨v0, v1⟩.
Let T0 denote the subgraph of T with the vertex v0 and the edge ⟨v0, v1⟩
deleted (Figure 7.16). The straight-line homotopy deﬁnes a strong defor-
mation retraction of ⟨v0, v1⟩onto v1; extending this to be the identity on
T0 yields a strong deformation retraction of T onto T0, which is continuous
because its restriction to each simplex is continuous. Therefore, T is homo-
topy equivalent to T0, which is contractible by the induction hypothesis.
Now we turn to the proof of Theorem 7.24. Roughly speaking, we would
like to prove the theorem by showing that if ψ is a homotopy inverse for
ϕ, then ψ ◦ϕ ≃IdX implies that ψ∗◦ϕ∗is the identity map, and similarly
for ϕ∗◦ψ∗. This would require us to show that homotopic maps induce the
same fundamental group homomorphisms. However, there is an immediate
problem with this approach: If two maps F0 and F1 are homotopic, we have
no guarantee that both maps take the base point q ∈X to the same point
in Y , so their induced homomorphisms do not even map into the same
group!
The following rather complicated-looking lemma is a substitute for the
claim that homotopic maps induce the same fundamental group homomor-
phism. It says, in eﬀect, that homotopic maps induce the same homomor-
phism up to a canonical change of base point.
Lemma 7.29. Suppose ϕ, ψ: X →Y are continuous, and H : ϕ ≃ψ is a
homotopy. For any q ∈X, let h be the path in Y from ϕ(q) to ψ(q) deﬁned
by h(t) = H(q, t). Let Φh : π1(Y, ϕ(q)) →π1(Y, ψ(q)) be the isomorphism

[[Homotopy]] Equivalence
165
f
H
ϕ(q)
ψ(q)
ψ ◦f
ϕ ◦f
h
X
I
Y
ϕ
ψ
q
h(t)
Ht ◦f
FIGURE 7.17. Induced homomorphisms of homotopic maps.
deﬁned in Theorem 7.11. Then the following diagram commutes:
ψ∗@
@@
R
π1(Y, ϕ(q))
π1(X, q)
ϕ∗



π1(Y, ψ(q)).
?
Φh
Proof. Let f be any loop in X based at q. What we need to show is
ψ∗[f] = Φh(ϕ∗[f])
⇐⇒ϕ∗[f] = Φh−1(ψ∗[f])
⇐⇒[ϕ ◦f] = [h] · [ψ ◦f] · [h−1]
⇐⇒ϕ ◦f ∼h · (ψ ◦f) · h−1.
At any time t, the map Ht ◦f is a loop based at h(t) (Figure 7.17). Thus
we can deﬁne a homotopy G from ϕ ◦f to h · (ψ ◦f) · h−1 by letting Gt
be the “lasso-shaped” loop that ﬁrst follows h as far as h(t), then follows
Ht ◦f at triple speed, then follows h back to ϕ(q). Formally,
G(s, t) =
⎧
⎪
⎨
⎪
⎩
h(3ts),
0 ≤s ≤1
3,
H(f(3s −1), t),
1
3 ≤s ≤2
3,
h(3t(1 −s)),
2
3 ≤s ≤1.

166
7. [[Homotopy]] and the Fundamental Group
It is straightforward to check that G is continuous by the gluing lemma.
The path G0 is a reparametrization of cϕ(q) · (ϕ ◦f) · cϕ(q), which is path
homotopic to ϕ ◦f; and G1 is a reparametrization of h· (ψ ◦f)· h−1.
Proof of Theorem 7.24. Suppose ϕ: X →Y is a homotopy equivalence,
and let ψ: Y →X be a homotopy inverse for it. Consider the sequence of
maps
π1(X, q)
ϕ∗
−→π1(Y, ϕ(q))
ψ∗
−→π1(X, ψ(ϕ(q)))
ϕ∗
−→π1(Y, ϕ(ψ(ϕ(q)))). (7.2)
We need to prove that the ﬁrst ϕ∗above is bijective. As we mentioned
earlier, ψ∗is not an inverse for it, because it does not map into the right
space.
Since ψ ◦ϕ ≃IdX, Lemma 7.29 shows that there is a path h in X such
that the following diagram commutes:
ψ∗◦ϕ∗@
@@
R
π1(X, q)
π1(X, q)
Id



π1(X, ψ(ϕ(q))).
?
Φh
(7.3)
Thus ψ∗◦ϕ∗= Φh, which is an isomorphism. In particular, this means that
the ﬁrst ϕ∗in (7.2) is injective and ψ∗is surjective.
Similarly, the homotopy ϕ ◦ψ ≃IdY leads to the diagram
ϕ∗◦ψ∗@
@@
R
π1(Y, ϕ(q))
π1(Y, ϕ(q))
Id



π1(Y, ϕ(ψ(ϕ(q)))),
?
Φk
from which it follows that ϕ∗◦ψ∗: π1(Y, ϕ(q)) →π1(Y, ϕ(ψ(ϕ(q)))) is an
isomorphism. This means in particular that ψ∗is injective; since we already
showed that it is surjective, it is an isomorphism. Therefore, going back to
(7.3), we conclude that ϕ∗= (ψ∗)−1 ◦Φh : π1(X, q) →π1(Y, ϕ(q)) is also
an isomorphism.
[[Homotopy]] Equivalence and Deformation Retraction
In Example 7.27 we showed that the ﬁgure eight and theta spaces are
homotopy equivalent by showing that they are both deformation retracts

[[Homotopy]] Equivalence
167
X × I
Y
Y

X
f
π
Zf
FIGURE 7.18. The mapping cylinder.
of a single larger space. This example is not as special as it might seem. As
the next proposition shows, two spaces are homotopy equivalent if and only
if both are homeomorphic to deformation retracts of a single larger space.
This gives a rather concrete way to think about homotopy equivalence.
Let X and Y be topological spaces, and let f : X →Y be a continuous
map. Deﬁne the mapping cylinder Zf of f to be the quotient space of
(X × I) ⨿Y by the equivalence relation generated by (x, 0) ∼f(x) for all
x ∈X. Let π denote the quotient map. The space Zf can be visualized as
a “top hat” (Figure 7.18) formed by gluing the “cylinder” X × I to Y (the
“brim”) by attaching each point (x, 0) on the bottom of the cylinder to its
image f(x) in Y .
The subspace X ×{1} ⊂(X ×I)⨿Y is a saturated closed subset homeo-
morphic to X. The restriction of π to this subset is thus a one-to-one quo-
tient map, so its image 
X is also homeomorphic to X. Similarly, Y = π(Y )
is homeomorphic to Y .
Proposition 7.30. With notation as above, if f is a homotopy equiva-
lence, then Y and 
X are deformation retracts of Zf. Thus two spaces are
homotopy equivalent if and only if they are both homeomorphic to defor-
mation retracts of a single space.
Proof. For any (x, s) ∈X × I, let [x, s] = π(x, s) denote its equivalence
class in Zf; similarly, [y] = π(y) is the equivalence class of y ∈Y .
First we show that Y is a strong deformation retract of Zf, assuming only
that f is continuous. We deﬁne a retraction A: Zf →Zf, which collapses

168
7. [[Homotopy]] and the Fundamental Group
H1
H2
H3
F
G
f
g
FIGURE 7.19. Homotopies of the mapping cylinder.
Zf down onto Y , by
A[x, s] = [x, 0];
A[y] = [y].
To be a bit more precise, we should deﬁne a map A: (X × I) ⨿Y →Zf by
A(x, s) = [x, 0] and A(y) = [y]. This map is evidently continuous because its
restrictions to X × I and Y are compositions of continuous maps. Because
A(x, 0) = [f(x)] = A(f(x)), A respects the identiﬁcations made by π, so it
passes to the quotient to yield the continuous map A deﬁned above. This
kind of standard argument will be used repeatedly to show that a map
from Zf is continuous; we will generally abbreviate it by saying something
like “A is well-deﬁned and continuous because A[x, 0] = [f(x)] = A[f(x)].”
Deﬁne a homotopy H1 : Zf × I →Zf (Figure 7.19) by
H1([x, s], t) = [x, s(1 −t)];
H1([y], t) = [y].
Because H1([x, 0], t) = [x, 0] = [f(x)] = H1([f(x)], t), H1 is well-deﬁned.
To check that it is continuous, we need only observe that it respects the
identiﬁcations made by the map π ×Id: ((X ×I)⨿Y )×I →Zf ×I, which
is a quotient map by Lemma 4.35. Since H1(ζ, 0) = ζ and H1(ζ, 1) = A(ζ)
for any ζ ∈Zf, H1 is a homotopy between the identity map of Zf and
A. Since, moreover, H1([y], t) = [y] for all y ∈Y , it is in fact a strong
deformation retraction.
Now suppose f is a homotopy equivalence, and let g: Y →X be a
homotopy inverse for it. Thus there exist homotopies F : Y × I →Y and
G: X × I →X such that F : f ◦g ≃IdY and G: g ◦f ≃IdX. Deﬁne two

Higher [[Homotopy]] Groups
169
more homotopies H2 and H3 by
H2([x, s], t) = [F(f(x), 1 −t)];
H2([y], t) = [F(y, 1 −t)];
H3([x, s], t) = [G(x, st), t];
H3([y], t) = [g(y), t].
The straightforward veriﬁcation that H2 and H3 are well-deﬁned and con-
tinuous is left to the reader. Geometrically, H2 deforms all of Zf into the
image of f in Y along the homotopy F, and then H3 collapses Zf onto 
X
by deforming each point along the homotopy G (Figure 7.19).
Inserting t = 0 and t = 1 into the deﬁnitions of H2 and H3, we ﬁnd that
H2 : A ≃B and H3 : B ≃C, where
B[x, s] = [g(f(x)), 0];
B[y] = [g(y), 0];
C[x, s] = [G(x, s), 1];
C[y] = [g(y), 1].
Because homotopy is transitive, the three homotopies H1, H2, H3 yield
IdZf ≃A ≃B ≃C. Since G(x, 1) = x, we ﬁnd that C[x, 1] = [x, 1], so
C is a retraction onto 
X, which shows that 
X is a deformation retract of
Zf.
Higher [[Homotopy]] Groups
You might have wondered what the subscript 1 stands for in π1(X). As
the notation suggests, the fundamental group is just one in a series of
groups associated with a topological space, all of which measure “holes”
of various dimensions. In this section we introduce the basic deﬁnitions
without much detail, just so that you will recognize this construction when
you see it again. We will not use this material anywhere else in the book.
The deﬁnition of the higher homotopy groups is motivated by the fact
that by identifying loops with their circle representatives as described ear-
lier in this chapter, we can regard the fundamental group π1(X, q) as the
set of equivalence classes of maps from S1 into X taking 1 to q, modulo ho-
motopy relative to the base point 1. Generalizing this, for any nonnegative
integer n, we deﬁne πn(X, q) to be the set of equivalence classes of maps

170
7. [[Homotopy]] and the Fundamental Group
from Sn into X taking (1, 0, . . . , 0) to q, modulo homotopy relative to the
base point. Just as in the case of the fundamental group, it can be shown
that πn(X, q) is a topological invariant.
The simplest case is n = 0. Since S0 = {±1}, a map from S0 to X sending
the base point 1 to q is determined by where it sends −1. Two such maps
are homotopic if and only if the two images of −1 lie in the same path
component of X. Therefore, π0(X, q) can be identiﬁed with the set of path
components of X. There is no canonical group structure on π0(X, q); it is
merely a set with a distinguished element (the component containing q). It
is conventional to deﬁne π0(X) to be the set of path components without
any distinguished element.
For n > 1, πn(X, q) has a multiplication operator (which we will not
describe here) under which it turns out to be an abelian group, called the
nth homotopy group of X based at q. These groups measure the inequivalent
ways of mapping Sn into X, and tell us, in a sense, about the n-dimensional
“holes” in X. For example, we will see later that π1(R3 ∖{0}) is trivial; but
it can be shown that the inclusion S2 	→R3 ∖{0} represents a nontrivial
element of π2(R3 ∖{0}).
The higher homotopy groups are notoriously hard to compute. In fact,
only a limited amount is known about πk(Sn) for k much larger than n.
The structure and computation of these groups form the embarkation point
for a vast branch of topology known as homotopy theory. See [Whi78] for
an excellent introduction to the subject.
Categories and Functors
In this section we digress a bit to give a brief introduction to category
theory, a powerful idea that uniﬁes many of the concepts we have seen so
far, and indeed much of mathematics. We will only touch on these ideas
from time to time in this book, but you will use them extensively if you do
more advanced work in algebraic topology, so it is important to familiarize
yourself with the basic concepts.
A category C consists of the following:
• a class (not necessarily a set) of objects;
• for each pair of objects X, Y a set HomC(X, Y ) of morphisms; and
• for each triple X, Y, Z of objects a function called composition:
HomC(X, Y ) × HomC(Y, Z) →HomC(X, Z), written (f, g) 
→g ◦f;
such that the following axioms are satisﬁed:
(i) Composition is associative: (f ◦g) ◦h = f ◦(g ◦h).

Categories and Functors
171
(ii) For each object X there exists an identity morphism IdX
∈
HomC(X, X) such that for any morphism f ∈HomC(X, Y ) we have
IdY ◦f = f = f ◦IdX.
There are many alternative notations in use. The set HomC(X, Y ) is also
sometimes denoted by C(X, Y ) or even just Hom(X, Y ) if the category
in question is understood. An element f ∈HomC(X, Y ) is often written
f : X →Y . For the most part you can think of the objects in a category as
sets with some special structure and the morphisms as maps that preserve
the structure, although the deﬁnitions do not require this, and we will see
below that there are natural examples that are not of this type.
Here are some familiar examples of categories, which we describe by
specifying their objects and morphisms; the composition laws and identity
morphisms are the obvious ones.
• SET: Sets and functions.
• GROUP: Groups and group homomorphisms.
• AB: Abelian groups and group homomorphisms.
• RING: Rings and ring homomorphisms.
• CRING: Commutative rings and ring homomorphisms.
• VECTR: Real vector spaces and R-linear maps.
• VECTC: Complex vector spaces and C-linear maps.
• TOP: Topological spaces and continuous maps.
• TOP∗: Pointed topological spaces—topological spaces together with a
choice of base point in each—and base-point-preserving continuous
maps.
• SIMP: Abstract simplicial complexes and simplicial maps.
In each case, the veriﬁcation of the axioms of a category is straightforward.
The main point is to show that a composition of the appropriate structure-
preserving maps again preserves the structure. Associativity is automatic
because it holds for composition of maps.
In any category C, a morphism f ∈HomC(X, Y ) is called an isomorphism
if there exists a morphism g ∈HomC(Y, X) such that f ◦g = IdY and
g ◦f = IdX. For example, in SET, the isomorphisms are just the bijections;
in GROUP they are the group isomorphisms; and in TOP they are the
homeomorphisms.
A subcategory of C is a category D whose objects are (some of the) objects
of C and whose sets of morphisms are subsets of the morphisms in C, with
the composition law and identities inherited from C. A full subcategory is

172
7. [[Homotopy]] and the Fundamental Group
one in which HomD(X, Y ) = HomC(X, Y ) whenever X, Y are objects of D.
For example, AB is a full subcategory of GROUP.
The real power of category theory becomes apparent when we consider
relations between categories. Suppose C and D are categories. A covariant
functor F from C to D is a rule that assigns to each object X in C an object
F(X) in D, and to each morphism f ∈HomC(X, Y ) an induced morphism
F(f) ∈HomD(F(X), F(Y )), in such a way that composition and identities
are preserved:
F(g ◦h) = F(g) ◦F(h);
F(IdX) = IdF(X) .
In many cases, if the functor is understood, it is traditional to write the
induced morphism F(g) as g∗.
It is also frequently useful to consider contravariant functors, which
are deﬁned in exactly the same way as covariant functors, except that
the induced morphisms go in the reverse direction: If g: X →Y , then
F(g): F(Y ) →F(X); and the composition law becomes
F(g ◦h) = F(h) ◦F(g).
It is common for the morphism F(f) induced by a contravariant functor F
to be written f ∗if the functor is understood. (Note the upper star: The
use of a lower star to denote a covariant induced morphism and an upper
star to denote a contravariant one is universal.)
Here are some important examples of functors.
Example 7.31 (Covariant Functors).
• The fundamental group functor π1 : TOP∗→GROUP assigns to each
pointed topological space (X, q) its fundamental group based at q,
and to each base-point-preserving continuous map its induced homo-
morphism. The fact that it is a covariant functor is the content of
Proposition 7.16.
• The functor π0 : TOP →SET assigns to each topological space its set
of path components. For any continuous map f : X →Y , the induced
map f∗: π0(X) →π0(Y ) just takes a path component X0 of X to the
path component of Y containing f(X0).
• The forgetful functor F: TOP →SET just assigns to each topological
space its underlying set, and to each continuous map its underlying
set map. In fact, such a functor exists for any category whose ob-
jects are sets with some extra structure and whose morphisms are
structure-preserving maps.
• The geometric realization functor from SIMP to TOP takes an ab-
stract complex K to its geometric realization, and a simplicial map

Categories and Functors
173
f : K →L to the continuous map |f|: |K| →|L|. It is a functor
because of Lemma 5.5.
Example 7.32 (Contravariant Functors).
• The dual space functor from VECTR to itself assigns to each vector
space V its dual space V ∗(the vector space of linear maps V →
R), and to each linear map ϕ: V →W the dual map or transpose
ϕ∗: W ∗→V ∗deﬁned by ϕ∗(f)x = f(ϕx). The veriﬁcation of the
functorial properties can be found in most linear algebra texts.
• The functor C: TOP →CRING assigns to each topological space X its
commutative ring C(X) of continuous real-valued functions f : X →
R. For any continuous map ϕ: X →Y , the induced map ϕ∗: C(Y ) →
C(X) is given by ϕ∗(f) = f ◦ϕ.
• If X and Z are abelian groups, the set Hom(X, Z) of group homo-
morphisms is also an abelian group under pointwise addition. We get
a contravariant functor from AB to itself by sending each group X
to the group Hom(X, Z), and each homomorphism f : X →Y to
the dual homomorphism f ∗: Hom(Y, Z) →Hom(X, Z) deﬁned by
f ∗(g) = g ◦f.
An immediate consequence of the deﬁnitions is that any (covariant or
contravariant) functor from C to D takes isomorphisms in C to isomor-
phisms in D: The proof is exactly the same as the proof for the fundamental
group functor (Corollary 7.17).
The examples considered so far are all categories whose objects are sets
with some structure and whose morphisms are structure-preserving maps.
Here are some examples that are not of this type.
Example 7.33 ([[Homotopy]] Categories).
• The homotopy category HTOP is the category whose objects are topo-
logical spaces as in TOP, but whose morphisms are homotopy classes
of continuous maps. Since composition preserves the homotopy rela-
tion, this is indeed a category. The isomorphisms in this category are
the (homotopy classes of) homotopy equivalences.
• A closely related category is the pointed homotopy category HTOP∗,
which has the same objects as TOP∗but whose morphisms are the
equivalence classes of continuous maps modulo homotopy relative
to the base point. One consequence of the homotopy invariance of
the fundamental group is that π1 deﬁnes a functor from HTOP∗to
GROUP.

174
7. [[Homotopy]] and the Fundamental Group
Example 7.34 (Groups as Categories). Suppose C is a category with
one object, in which every morphism is an isomorphism. If we call the object
X, the entire structure of the category is contained in the set HomC(X, X)
of morphisms and its composition law. The axioms for a category say that
any two morphisms can be composed to obtain a third morphism, that
composition is associative, and that there is an identity morphism. The
additional assumption that every morphism is an isomorphism means that
each morphism has an inverse. In other words, HomC(X, X) is a group!
Functors between such categories are just group homomorphisms. In fact,
every group can be identiﬁed with such a category. One way to see this is
to identify a group G with the subcategory of SET consisting of the one
object G and the maps Lg : G →G given by left translation.
Another ubiquitous and useful technique in category theory goes by the
name of “universal mapping properties.” These give a uniﬁed way to deﬁne
common constructions that arise in many categories, such as products and
sums.
Let {Xα : α ∈A} be any indexed collection of objects in a category C. An
object P together with a set of morphisms πα : P →Xα called projections
is said to be a product of the objects {Xα} if given any object W in C and
morphisms fα : W →Xα, there exists a unique morphism f : W →P such
that each of the following diagrams commutes:
W
Xα.
-
fα
f



P
?
πα
Lemma 7.35. If a product exists in any category, it is unique up to an
isomorphism that respects the projections.
Proof. If (P, {πα}) and (P ′, {π′
α}) are both products of objects {Xα},
the deﬁning property guarantees the existence of maps f : P →P ′ and
f ′ : P ′ →P satisfying π′
α ◦f = πα and πα ◦f ′ = π′
α. Arguing exactly as in
the proof that the product topology on X1 ×· · ·×Xn is the unique one sat-
isfying the characteristic property (Theorem 3.10), we conclude that f ◦f ′
and f ′ ◦f are both identity maps.
In any particular category, products may or may not exist. Here are some
examples of familiar categories in which products always exist.
Example 7.36 (Categorical Products).
(a) The product of a collection of sets in the category SET is just their
Cartesian product.

Categories and Functors
175
(b) In the category TOP of topological spaces and continuous maps, the
product of ﬁnitely many spaces X1, . . . , Xn is the space X1 ×· · ·×Xn
with the product topology. The characteristic property of the prod-
uct topology guarantees that the product space satisﬁes the deﬁning
condition for a product. (The categorical deﬁnition of product, by the
way, determines the correct deﬁnition of the product topology on a
product of inﬁnitely many spaces; see Problem 7-12.)
(c) The product of groups {Gα : α ∈A} in GROUP is their direct prod-
uct group 
α Gα, with the group structure obtained by multiplying
elements componentwise.
Exercise 7.8.
Prove that each of the above constructions satisﬁes the
deﬁning property of a product in its category.
If we reverse all the morphisms in the deﬁnition of a product, we get
a dual concept called a sum. A sum of objects {Xα} in a category C is
an object S together with morphisms ια : Xα →S called injections such
that given any object W in C and morphisms fα : Xα →W, there exists
a unique morphism f : S →W such that each of the following diagrams
commutes:
Xα
W.
-
fα
f
@
@@
R
S
6
ια
Lemma 7.37. If a sum exists in a category, it is unique up to an isomor-
phism that respects the injections.
Exercise 7.9.
Prove Lemma 7.37.
Some examples of categorical sums are given in the problems.

176
7. [[Homotopy]] and the Fundamental Group
Problems
7-1. Let B ⊂Rn be any convex set, X any topological space, and A any
subset of X. Show that any two continuous maps f, g: X →B that
agree on A are homotopic relative to A.
7-2. Prove the following facts about retracts.
(a) A retract of a Hausdorﬀspace is closed.
(b) A retract of a connected space is connected.
(c) A retract of a compact space is compact.
(d) A retract of a simply connected space is simply connected.
(e) A retract of a retract is a retract, i.e., if A ⊂B ⊂X, A is a
retract of B, and B is a retract of X, then A is a retract of X.
7-3. Show that the M¨obius band (see Chapter 5) is homotopy equivalent
to S1.
7-4. Let X be a path connected space and p, q ∈X. Determine an alge-
braic necessary and suﬃcient condition on the fundamental group of
X under which all path classes from p to q give the same isomorphism
of π1(X, p) with π1(X, q).
7-5. For any compact surface S, show that S with one point removed is
homotopy equivalent to a bouquet of ﬁnitely many circles.
7-6. Let K be a simplicial complex and σ ∈K any simplex. Show that |σ|
has a neighborhood U ⊂|K| such that |σ| is a strong deformation
retract of U. [Hint: Let U = |K| ∖{|τ| : τ ∩σ = ∅}. For any
k-simplex τ = ⟨v0, . . . , vk⟩whose intersection with σ is nonempty,
deﬁne π: τ ∩U →τ ∩U by
π

k

i=0
tivi

=

l

i=0
ti
−1
l

i=0
tivi

,
where v0, . . . , vl are the vertices of τ ∩σ, and let H : (τ ∩U)×I →τ ∩U
be the straight-line homotopy between Id and π. Show that H deﬁnes
a strong deformation retraction of U onto |σ|.]
7-7. Give another proof of Lemma 7.29 by considering the map F : I×I →
Y deﬁned by F(s, t) = H(f(s), t) and applying Lemma 7.12.
7-8. Show that any two vertices in a tree are joined by a unique reduced
edge path.

Problems
177
7-9. Given any collection {Xα : α ∈A} of topological spaces, show that
their disjoint union 
α Xα, together with the disjoint union topology
and the natural inclusions ια : Xα 	→
α Xα, is their sum in the
category TOP.
7-10. Given any collection of abelian groups {Gα : α ∈A}, let 
α Gα
be the subgroup of the direct product 
α Gα consisting of all those
elements {gα}α∈A such that gα is the identity element in Gα for all
but ﬁnitely many α; and for each α let ια : Gα 	→
α Gα be the
obvious injection. Show that this group, called the direct sum of the
groups Gα, is the sum of the Gα’s in the category AB.
7-11. Show that the construction described in Problem 7-10 does not yield
the sum in the category GROUP as follows: Take G1 = G2 = Z,
and ﬁnd homomorphisms f1 and f2 from Z to some (necessarily non-
abelian) group H such that no homomorphism f : Z ⊕Z →H makes
the following diagram commute for i = 1, 2:
Z
H.
-
fi
f
@
@@
R
Z ⊕Z
6
ιi
(We will see how to construct the sum in GROUP in Chapter 9.)
7-12. Given any collection {Xα : α ∈A} of topological spaces, deﬁne a
basis in the Cartesian product 
α Xα consisting of product sets of
the form 
α Uα, where Uα is open in Xα and Uα = Xα for all but
ﬁnitely many α. Show that this is a basis, and that 
α Xα with this
topology is the product of the spaces Xα in the category TOP.
7-13. Show that any vertex in a connected ﬁnite tree is a strong deformation
retract of the tree.

8
Circles and Spheres
So far, we have not actually computed any nontrivial fundamental groups.
The main goal of this chapter is to remedy this by computing the funda-
mental group of the circle. We will show, as promised, that π1(S1, 1) is an
inﬁnite cyclic group generated by the path α that goes once around the
circle counterclockwise at constant speed. Thus each element of π1(S1, 1)
is uniquely determined by an integer, called its “winding number,” which
counts the net number of times and in which direction the path winds
around the circle.
Here is the essence of the plan. We would like to show that any loop in
the circle is in the path class [α]n for a unique integer n. The idea is to
represent a path by giving its angle θ(s) as a function of the parameter,
and then the winding number should be essentially 1/(2π) times the total
change in angle, θ(1) −θ(0).
Since the angle θ is not a well-deﬁned continuous function on the circle, in
order to make rigorous sense of this, we need to undertake a detailed study
of the exponential quotient map ε: R →S1 deﬁned at the end of Chapter 3.
An angle function for a loop f is just (up to a constant multiple) a “lift” of
f to a path in R. Because R is simply connected, we can always construct
a homotopy between two lifts that have the same total change in angle.
There are three key lifting lemmas that make this all work. In the begin-
ning of the chapter we state those lifting lemmas, and then we use them
to prove that the fundamental group of the circle is inﬁnite cyclic. In the
next section we prove the lifting lemmas. These three properties will make
another very important appearance later in the book, when we discuss
covering spaces.

180
8. Circles and Spheres
At the end of the chapter we compute the fundamental groups of the
higher-dimensional spheres and product spaces, and show that the funda-
mental group of any manifold is countable.
The Fundamental Group of the Circle
Throughout this chapter we will think of the circle as lying in the complex
plane, and we will always use the base point 1 ∈C, which corresponds to
(1, 0) ∈R2.
Let α: I →S1 denote the loop α(s) = e2πis. The complete structure of
the fundamental group of the circle is described by the following theorem.
Theorem 8.1. The group π1(S1, 1) is inﬁnite cyclic, with generator [α].
To prove this theorem we will use a concrete representative of the path
class [α]n, deﬁned as follows. For any integer n, let αn : I →S1 be the loop
αn(s) = e2πins. It is easy to see that αn is a reparametrization of αn−1 · α,
so by induction [αn] = [α]n.
As mentioned in the introduction to this chapter, the proof of the theo-
rem is based on a close examination of the quotient map ε: R →S1 deﬁned
by ε(x) = e2πix. If ϕ: B →S1 is any continuous map, a lift of ϕ is a
continuous map ϕ: B →R such that the following diagram commutes:
B
S1.
-
ϕ
ϕ




R
?
ε
For example, if f : I →S1 is a path in S1, then a lift f of f can be
interpreted geometrically by observing that θ(s) = 2π f(s) is a continuous
choice of angle function such that f(s) = eiθ(s).
It is important to be aware that some maps may have no lifts at all. For
example, suppose σ: S1 →R were a lift of the identity map of S1:
S1
S1.
-
IdS1
σ




R
?
ε
Then the equation ε ◦σ = IdS1 means that 2πσ is a continuous choice
of angle function on the circle. It is intuitively evident that this cannot
exist, because any choice of angle function would have to change by 2π
as one goes once around the circle, and thus could not be continuous on

The Fundamental Group of the Circle
181
the whole circle. Assuming for the moment the result of Theorem 8.1, we
can prove rigorously that σ cannot exist just by noting that if there were
such a map, the induced homomorphism ε∗◦σ∗would be the identity on
π1(S1, 1), which would mean in particular that ε∗: π1(R, 0) →π1(S1, 1)
was surjective. Since π1(R, 0) is the trivial group and π1(S1, 1) is not, this
is impossible.
The ﬁrst important fact about lifts is the following uniqueness lemma.
This is not actually used directly in the computation of π1(S1), but it is
necessary for proving the other two lifting properties.
Lemma 8.2 (Unique Lifting Property of the Circle). Suppose B is
connected, ϕ: B →S1 is continuous, and ϕ1, ϕ2 : B →R are lifts of ϕ that
agree at some point of B. Then ϕ1 ≡ϕ2.
The next lifting lemma shows that paths in the circle, at least, always
have lifts.
Lemma 8.3 (Path Lifting Property of the Circle).
Suppose
f : I →S1 is any path, and r0 ∈R is any point in the ﬁber of ε
over f(0). Then there exists a unique lift f : I →R of f such that
f(0) = r0.
Our third lifting lemma concerns lifts of homotopies: It says that lifts of
path homotopic paths are path homotopic, as long as they both start at
the same point.
Lemma 8.4 ([[Homotopy]] Lifting Property of the Circle).
Suppose
f0, f1 : I →S1 are path homotopic, and f0, f1 : I →R are lifts of f0 and f1
with the same initial points. Then f0 ∼f1.
Assuming these lifting lemmas, let us now carry out the proof of our
theorem about the fundamental group of the circle.
Proof of Theorem 8.1.
Deﬁne a map j : Z →π1(S1, 1) by j(n) = [α]n. It
suﬃces to show that j is an isomorphism (considering Z as an additive
group). Because [α]n+m = [α]n[α]m, j is a homomorphism. We will show
that it is injective and surjective.
To prove surjectivity, let [f] be any element of π1(S1, 1). By the path
lifting property of the circle, f has a lift f : I →R such that f(0) = 0
(Figure 8.1). Now, e2πi f(1) = ε ◦f(1) = f(1) = 1, so f(1) is an integer n.
We will show that [f] = [αn] = j(n).
If we let bn : I →R be the path bn(s) = ns, the two paths f and bn
both start at 0 and end at n. Because R is simply connected, f ∼bn. Since
continuous maps preserve path homotopy, this implies f = ε ◦f ∼ε ◦bn =
αn, thus proving that j is surjective.
To prove injectivity, suppose some n ∈Z is mapped by j to the identity
element [c1] ∈π1(S1, 1), or in other words, [α]n = [c1]. Representing the

182
8. Circles and Spheres
ε
f
f
bn
0
1
n
FIGURE 8.1. Proof that every path in S1 is homotopic to αn.
path class [α]n by αn as above, the assumption is αn ∼c1. If αn and c1
are lifts of αn and c1 starting at 0, the homotopy lifting property of the
circle guarantees that αn ∼c1 in R. In particular, they both have the same
terminal point. Now the lift of αn starting at 0 ∈R is easily seen to be bn,
and the lift of c1 is the constant loop c0. Thus n = bn(1) = c0(1) = 0, so j
is injective.
A close examination of this proof shows that we have actually constructed
an explicit inverse for j, which is of interest in its own right. Deﬁne a map
N : π1(S1, 1) →Z as follows: For any [f] ∈π1(S1, 1), let N[f] = f(1), where
f is the lift of f starting at 0 ∈R. Such a lift exists by the path lifting
property, and f(1) is independent of the choice of f by the homotopy lifting
property. The proof above shows that N = j−1.
If we think of 2π f as a continuous choice of angle function for f, then
2πN[f] represents, intuitively, the total change in the angle of f(s) as s
goes from 0 to 1, and N[f] represents the number of times f winds around
the circle. For this reason, N[f] is called the winding number of the path
f.

Proofs of the Lifting Lemmas
183
S1
R
ε
U
Un
q
FIGURE 8.2. Evenly covered neighborhood in S1.
Proofs of the Lifting Lemmas
Before proving the three lifting lemmas, we need some preliminary results.
The ﬁrst is a precise description of the behavior of the quotient map ε.
Lemma 8.5. Each point q ∈S1 has a neighborhood U such that ε−1(U)
is a disjoint union of countably many open intervals Un, on each of which
the restriction of ε is a homeomorphism from Un onto U (Figure 8.2).
Proof. This is just a straightforward computation from the deﬁnition of ε.
We can take, for example, U = S1 ∖{−q}; then the sets Un are the open
intervals of the form (r + n, r + n + 1), where r is a ﬁxed number such
that ε(r) = −q and n ranges over the integers. For each n, ε: Un →U is a
bijective open map and therefore a homeomorphism.

184
8. Circles and Spheres
An open set U ⊂S1 that has the properties described in this lemma is
said to be evenly covered. The most important property of an evenly covered
open set is that it admits local right inverses for ε, as we now describe.
First, a bit of terminology. If p: X →Y is any surjective continuous map,
a section of p is a continuous map σ: Y →X such that p ◦σ = IdY (i.e., a
right inverse for p):
X
p
σ
Y.
If U ⊂Y is an open set, a local section of p over U is a continuous map
σ: U →X such that p ◦σ = IdU.
Lemma 8.6 (Local Section Property of the Circle).
Let U ⊂S1 be
an evenly covered open set. For any q ∈U and any r in the ﬁber of ε over
q, there is a local section σ of ε over U such that σ(q) = r.
Proof. By deﬁnition of an evenly covered open set, r is contained in some
open set Un ⊂R such that ε: Un →U is a homeomorphism. Thus σ =
(ε|Un)−1 is the desired local section.
Proof of the Unique Lifting Property. Let S = {b ∈B : ϕ1(b) = ϕ2(b)}. By
hypothesis S is not empty. Since B is connected, if we can show that S is
open and closed in B, it must be all of B.
To show that S is open, let b ∈S. Write r = ϕ1(b) = ϕ2(b) and q =
ε(r) = ϕ(b). Let U ⊂S1 be an evenly covered neighborhood of q, and
let U be the component of ε−1(U) containing r (Figure 8.3). If we set
V = ϕ−1
1 (U) ∩ϕ−1
2 (U), then V is a neighborhood of b on which both ϕ1
and ϕ2 take their values in U. Now, the fact that ϕ1 and ϕ2 are lifts of ϕ
translates to ϕ = ε ◦ϕ1 = ε ◦ϕ2. Since ε is injective on U, we conclude
that ϕ1 and ϕ2 agree on V , which is to say that V ⊂S, so S is open.
To show that it is closed, we will show that its complement is open. Let
b ̸∈S, and set r1 = ϕ1(b) and r2 = ϕ2(b), so that r1 ̸= r2. As above, let
q = ε(r1) = ε(r2) = ϕ(b), and let U be an evenly covered neighborhood
of q. Then there are disjoint neighborhoods U1 of r1 and U2 of r2 such
that ε is a homeomorphism from U1 to U and from U2 to U. Letting
V = ϕ−1
1 (U1) ∩ϕ−1
2 (U2), we conclude that ϕ1(V ) ⊂U1 and ϕ2(V ) ⊂U2,
so ϕ1 ̸= ϕ2 on V , which is to say that V ∩S = ∅. Thus S is closed, and the
proof is complete.
Proof of the path lifting property. Let f : I →S1 be a path, and r0 ∈
ε−1(f(0)) as in the statement of the lemma. If U is an open cover of the
circle by evenly covered open sets, the collection {f −1(U) : U ∈U} is an
open cover of I. Let δ be a Lebesgue number for this cover. Choosing an

Proofs of the Lifting Lemmas
185
ϕ1
ϕ2
ϕ
ϕ−1
1 (U)
ϕ−1
2 (U)
V
B
r
U
q
U
b
ε
FIGURE 8.3. Proof of the unique lifting property.
integer n large enough that 1/n < δ, the Lebesgue number lemma says
that each interval [k/n, (k + 1)/n] of length 1/n is contained in one of the
sets f −1(U), which is to say that it is mapped by f into an evenly covered
open set.
We deﬁne the lift f : I →R inductively as follows. First choose an evenly
covered open set U0 such that f[0, 1/n] ⊂U0. Letting σ0 : U0 →R denote
the local section such that σ0(f(0)) = r0, we set
f = σ0 ◦f
on [0, 1/n].
It follows immediately that f is continuous and satisﬁes f(0) = r0 and
ε ◦f = f.
Proceeding by induction, suppose we have deﬁned a continuous lift of f
on an interval of the form [0, k/n] for some integer k. As before, f[k/n, (k+
1)/n] is contained in an evenly covered set Uk. Letting σk : Uk →R be the
local section such that σk(f(k/n)) = f(k/n), we set
f = σk ◦f
on [k/n, (k + 1)/n].

186
8. Circles and Spheres
The resulting map is continuous by the gluing lemma. By induction we
obtain a lift f deﬁned on all of I. It is unique by the unique lifting property.
Proof of the homotopy lifting property. Now suppose f0, f1 are path homo-
topic paths in the circle, and f0, f1 are any lifts of them starting at the
same point r0 ∈R. Let H : f0 ∼f1 be a path homotopy. This means that
H : I × I →S1 satisﬁes
H(s, 0) = f0(s);
H(s, 1) = f1(s);
H(0, t) = f0(0) = f1(0);
H(1, t) = f0(1) = f1(1).
We will show below that there exists a lift of H to a map H : I × I →R
such that H(0, 0) = r0. Assuming this, we argue as follows. First, note that
ε◦H(0, t) = H(0, t) = f0(0). Therefore, t 
→H(0, t) is a lift of the constant
loop at f0(0) to a path starting at r0; by the unique lifting property, it must
be the constant loop at r0, so H(0, t) = r0 for all t. The same argument
shows that H(1, t) is constant for all t, so H is a path homotopy. Moreover,
H0(s) = H(s, 0) is a lift of f0 starting at r0, and similarly, H1 is a lift of
f1 starting at r0. By the unique lifting property, these must be equal to
the given lifts f0 and f1, respectively, and H provides a path homotopy
between them.
All that remains is to prove the existence of the lift H. As in the proof
of the path lifting property, there exists δ > 0 such that any subset of I ×I
whose diameter is less than δ is mapped by H into an evenly covered subset
of S1. Choose n large enough that each square of side 1/n has diameter less
than δ. (Any n >
√
2/δ will do.)
For any integers i, j such that 0 ≤i, j ≤n −1, let Sij denote the square
[i/n, (i + 1)/n] × [j/n, (j + 1)/n] (Figure 8.4). For any point x ∈R in the
ﬁber of ε over H(i/n, j/n), there exists a unique lift Hij of H over Sij
satisfying Hij(i/n, j/n) = x, given by Hij = σ ◦Hij, where σ is the local
section of ε such that σ(H(i/n, j/n)) = x.
We deﬁne H inductively on I ×I as follows. On S00, let H00 be the lift of
H such that H(0, 0) = r0. On the next square to the right, S10, let H10 be
the lift such that H10(1/n, 0) = H00(1/n, 0). We now have two lifts deﬁned
on the line segment {(1/n, t) : 0 ≤t ≤1/n} where the two squares overlap.
But on this line segment, the paths t 
→H00(1/n, t) and t 
→H10(1/n, t)
are both lifts of the path t 
→H(1/n, t) starting at the same point; thus by
the unique lifting property they are equal.
Continuing in this way, we deﬁne lifts on each of the squares Si0, i =
0, . . . , n−1, and then on the squares of the second row, and so on. Suppose
by induction that we have deﬁned lifts Hi′j′ on all squares Si′j′ for j′ < j,

Fundamental Groups of Spheres
187
Sij
H
H
i/n
j/n
U
H(i/n, j/n)
ε
U
H(i/n, j/n)
FIGURE 8.4. Proof of the homotopy lifting property (inductive step).
and for j′ = j and i′ < i, and all such lifts agree where they overlap. We let
Hij be the unique lift of H on Sij that agrees with any (hence all) previous
lifts at the lower left corner (i/n, j/n). At a typical such square, we have to
check that the new lift agrees with two diﬀerent old ones: one coming from
the square Si−1,j to the left, and one coming from the square Si,j−1 below.
Just as in the preceding paragraph, the unique lifting property guarantees
that the old and new lifts agree on both of these line segments.
In the end we obtain the desired lift H by letting H = Hij on Sij; it is
continuous by the gluing lemma.
Fundamental Groups of Spheres
The situation is much simpler for the higher-dimensional spheres. The
sphere minus the north pole is homeomorphic to Rn by stereographic pro-
jection (see Example 3.6). In fact, composing stereographic projection with
a suitable rotation of the sphere, it is easy to see that the sphere minus
any point is homeomorphic to Rn. Therefore, if we knew that any loop in

188
8. Circles and Spheres
Sn omitted at least one point in the sphere, we could consider it as a loop
in Rn; since it is null homotopic there, it is null homotopic in Sn.
Unfortunately, an arbitrary loop might not omit any points. For example,
there is a continuous surjective map f : I →I ×I (a “space-ﬁlling curve”—
see, e.g., [Rud76]). Composing this with a surjective map I × I →S2 such
as the one constructed in Proposition 6.2(b) yields a path whose image is
all of S2. But as the proof of the next proposition shows, we can modify
any curve by a homotopy so that it does miss a point.
Theorem 8.7. For n ≥2, Sn is simply connected.
Proof. Let N = (0, . . . , 0, 1) denote the north pole, and S = −N the south
pole. Both the open sets U = Sn∖{N} and V = Sn∖{S} are homeomorphic
to Rn. If f : I →Sn is any path, by the Lebesgue number lemma there is an
integer n such that on each subinterval [k/n, (k + 1)/n], f takes its values
either in U or in V . Now, V ∖{N} is homeomorphic to Rn ∖{0}, which
is connected. (Here is where the dimensional restriction comes in—when
n = 1, Rn ∖{0} is disconnected.) Thus, for each such segment that lies in
V , there is another path in V with the same endpoints that misses N; since
V is simply connected, these two paths are path homotopic in V and thus
in Sn. Of course, each segment that lies in U already misses N. This shows
that f is homotopic to a path in Sn∖{N} ≈Rn, so f is null homotopic.
Corollary 8.8. For n ≥3, Rn ∖{0} is simply connected.
Proof. The map F : Rn ∖{0} →Sn−1 given by F(x) = x/|x| is a strong
deformation retraction (by a straight-line homotopy).
Fundamental Groups of Product Spaces
In this section we will show how to compute the fundamental group of an
arbitrary (ﬁnite) product of topological spaces in terms of the fundamental
groups of the factors. As an application, we will compute the fundamental
groups of tori.
Let X1, . . . , Xn be topological spaces, and let pi : X1 × · · · × Xn →Xi
denote projection on the ith factor. (We are avoiding our usual notation πi
for the projections here so as not to create confusion with the notation π1
for the fundamental group.) Choosing base points qi ∈Xi, we get maps
pi∗: π1(X1 × · · · × Xn, (q1, . . . , qn)) →π1(Xi, qi).
Putting these together, we deﬁne a map
p: π1(X1 × · · · × Xn, (q1, . . . , qn)) →π1(X1, q1) × · · · × π1(Xn, qn)

Fundamental Groups of Manifolds
189
by
p[f] = (p1∗[f], . . . , pn∗[f]).
(8.1)
Proposition 8.9 (Fundamental Group of a Product).
If X1, . . . ,
Xn are any topological spaces, the map p: π1(X1 ×· · ·×Xn, (q1, . . . , qn)) →
π1(X1, q1) × · · · × π1(Xn, qn) deﬁned by (8.1) is an isomorphism.
Proof. First we will show that p is surjective. Let [fi] ∈π1(Xi, qi) be
arbitrary for i = 1, . . . , n. Deﬁne a loop f in the product space by
f(s) = (f1(s), . . . , fn(s)). Since the component functions of f satisfy
fi = pi◦f, we compute p[f] = (p1∗[f], . . . , pn∗[f]) = ([p1◦f], . . . , [pn◦f]) =
([f1], . . . , [fn]).
To show injectivity, suppose f is a loop in the product space, and p[f] is
the identity element of π1(X1, q1) × · · · × π1(Xn, qn). Writing f in terms of
its component functions as f(s) = (f1(s), . . . , fn(s)), the hypothesis means
that [cqi] = pi∗[f] = [pi ◦f] = [fi] for each i. If we choose homotopies
Hi : fi ∼cqi, it follows easily that the map H : X1 × · · · × Xn × I →
X1 × · · · × Xn given by
H(x1, . . . , xn, t) = (H1(x1, t), . . . , Hn(xn, t))
is a homotopy from f to the constant loop c(q1,...,qn).
Corollary 8.10 (Fundamental Groups of Tori).
Let Tn = S1 × · · · ×
S1 be the n-dimensional torus, and let αi denote the standard loop in the
ith copy of S1:
αi(s) = (1, . . . , 1, e2πis, 1, . . . , 1).
Using q = (1, . . . , 1) as base point, the map ϕ: Zn →π1(Tn, q) given by
ϕ(k1, . . . , kn) = [α1]k1 · · · [αn]kn is an isomorphism.
Fundamental Groups of Manifolds
We conclude this chapter by proving an important theorem about funda-
mental groups of manifolds. This does not have to do with circles or spheres
per se, but it does use techniques similar to those used in the other proofs
in this chapter, so this is a convenient time to insert it.
Theorem 8.11. The fundamental group of a manifold is countable.
Proof. Let M be a manifold, and let U be a countable cover of M by
Euclidean balls. For each U, U ′ ∈U the intersection U ∩U ′ has at most
countably many components; choose a point in each such component and

190
8. Circles and Spheres
Uk−1
Uk
Uk+1
f
 k−1
n

f
 k
n

pUk
xk−1,xk
fk
xk
xk−1
f
gk
gk−1
FIGURE 8.5. Proof that a manifold has countable fundamental group.
let X denote the (countable) set consisting of all the chosen points as U, U ′
range over all the sets in U. For each U ∈U and x, x′ ∈X such that
x, x′ ∈U, choose a deﬁnite path pU
x,x′ from x to x′ in U.
Now choose any point q ∈X as base point. Let us say that a loop based
at q is special if it is a ﬁnite product of paths of the form pU
x,x′. Because
both U and X are countable sets, there are only countably many special
loops. Each special loop determines an element of π1(M, q). If we can show
that every element of π1(M, q) is obtained in this way, we will be done,
because we will have exhibited a surjective map from a countable set onto
π1(M, q).
So suppose f is any loop based at q. By the Lebesgue number lemma
there is an integer n such that f maps each subinterval [(k −1)/n, k/n]
into one of the balls in U; call this ball Uk. Let fk = f|[(k−1)/n,k/n],
reparametrized on the unit interval, so that [f] = [f1] · · · · · [fn].
Since for each k = 1, . . . , n−1, f(k/n) ∈Uk ∩Uk+1, there is some xk ∈X
that lies in the same component of Uk ∩Uk+1 as f(k/n). Choose a path gk
in Uk ∩Uk+1 from xk to f(k/n) (Figure 8.5), and set fk = gk−1 · fk · g−1
k
(taking xk = q and gk to be the constant path cq when k = 0 or n). It is
immediate that [f] = [ f1]·· · ··[ fn], because all the gk’s cancel out. But for
each k, fk is a path in Uk from xk−1 to xk, and since Uk is simply connected,
fk is path homotopic to pUk
xk−1xk. This shows that f is path homotopic to
a special loop and completes the proof.

Problems
191
Problems
8-1. Prove that the circle is not a retract of the closed disk.
8-2. Identifying the circle with the subspace S1 × {1} ⊂T2, prove that
the circle is not a deformation retract of the torus.
8-3. Prove that the fundamental group of any topological group is abelian.
[Hint: If f and g are loops based at 1 ∈G, consider the map F from
I × I into G given by F(s, t) = f(s)g(t) and use Lemma 7.12.]
8-4. Suppose U ⊂R2 is an open set and x ∈U. Show that U ∖{x} is
not simply connected. [Hint: Let S be a small circle around x, and
consider the sequence of inclusions S 	→U ∖{x} 	→R2 ∖{x}.]
8-5. Show that a topological space cannot be simultaneously a 2-manifold
and an n-manifold for some n > 2. [Hint: If n > 2, any n-manifold has
a basis of open sets in which the complement of any point is simply
connected.]
8-6. Let M be a 2-dimensional manifold with boundary. Show that the
set of boundary points of M is disjoint from the set of interior points.
Conclude that a 2-manifold with boundary is a manifold if and only
if its boundary is empty.
8-7. Let ϕ: S1 →S1 be a continuous map such that ϕ(1) = 1. Because
π1(S1, 1) is inﬁnite cyclic, there is an integer n, called the degree of
ϕ and denoted by deg ϕ, such that ϕ(γ) = γn for all γ ∈π1(S1, 1).
If ϕ: S1 →S1 is an arbitrary continuous map, we deﬁne the degree
of ϕ to be the degree of ρ ◦ϕ, where ρ: S1 →S1 is the rotation
ρ(z) = z/ϕ(1) (in complex notation), which takes ϕ(1) to 1.
(a) Show that two maps ϕ, ψ: S1 →S1 are homotopic if and only if
they have the same degree.
(b) Show that deg(ϕ◦ψ) = deg ϕ deg ψ for any two continuous maps
ϕ, ψ: S1 →S1.
(c) For each n ∈Z, compute the degrees of the nth power map
pn(z) = zn and its conjugate pn(z) = zn.
(d) Show that ϕ: S1 →S1 has an extension to a continuous map
Φ: B2 →S1 if and only if it has degree zero.
8-8. Prove the fundamental theorem of algebra: Every complex polynomial
of positive degree has a zero. [Hint: If p(z) = zn+an−1zn−1+· · ·+a0,
write pε(z) = εnp(z/ε) and show that there exists ε > 0 such that
|pε(z) −zn| < 1 when z ∈S1. If p has no zeros, prove that pε|S1 is
homotopic to pn(z) = zn, and use the results of Problem 8-7 to derive
a contradiction.]

192
8. Circles and Spheres
8-9. The Brouwer ﬁxed point theorem says that any continuous map
f : Bn →Bn has a ﬁxed point (i.e., a point x such that f(x) = x).
Prove this in the case n = 2 as follows: If f : B2 →B2 has no ﬁxed
point, deﬁne ϕ: B2 →S1 by ϕ(x) = (f(x) −x)/|f(x) −x|. Derive a
contradiction by showing that the restriction of ϕ to S1 is homotopic
to the identity. [If you crumple a map of the country that you are in
and drop it on the ground, this theorem guarantees that some point
on the map will lie exactly over the point it represents.]
8-10. Let V be a vector ﬁeld on R2, i.e., a continuous map V : R2 →R2. A
point q ∈R2 is called a singular point of V if V (q) = 0, and a regular
point if V (q) ̸= 0. A singular point is isolated if it has a neighborhood
containing no other singular points. Let RV ⊂R2 denote the set of
regular points of V . For any loop f : I →RV , deﬁne the index of V
with respect to f, denoted by Ind(V, f), to be the winding number of
the loop f : I →S1, given by
f(s) = V (f(s))
|V (f(s))|.
(a) Show that Ind(V, f) depends only on the path class of f.
(b) If q is an isolated singular point of V , show that Ind(V, fε) is
independent of ε for ε suﬃciently small, where fε(s) = q+εα(s),
and α is the standard counterclockwise loop around the unit
circle. This integer is called the index of V at q, and is denoted
by Ind(V, q).
(c) If V has ﬁnitely many singular points in the closed unit disk,
all in the interior, show that the index of V with respect to the
loop α around the unit circle is equal to the sum of the indices
of V at the interior singular points.
(d) Compute the index of each of the following vector ﬁelds at the
origin:
V1(x, y) = (x, y);
V2(x, y) = (−x, −y);
V3(x, y) = (x + y, x −y).

9
Some Group Theory
In this chapter we depart from topology for a while to discuss group theory.
Our goal, of course, is to use the group theory to solve topological problems,
and in the next chapter we will compute the fundamental groups of all
compact surfaces, and use them to show, among other things, that the
diﬀerent surfaces listed in the classiﬁcation theorem of Chapter 6 are not
homeomorphic to each other.
Before we do so, however, we need to develop some tools for constructing
and describing groups. We will discuss four such tools in this chapter: free
products of groups, free groups, presentations of groups by generators and
relations, and free abelian groups. These will all play central roles in our
computations of fundamental groups in the next chapter, and the material
on free abelian groups will also be used in the discussion of homology in
Chapter 13.
This chapter assumes that you are familiar with the basic facts of group
theory as summarized in the Appendix. If your group theory is rusty, this
would be a good time to pull out an algebra text and refresh your memory.
Free Products
There is a familiar way to create a group as a product of two or more other
groups: The direct product of groups G1, . . . , Gn (see the Appendix) is the
Cartesian product set G1 × · · · × Gn with the group structure obtained by
multiplying the entries in two n-tuples component by component.

194
9. Some Group Theory
For each i, the direct product G1 × · · · × Gn has a subgroup {1} × · · · ×
{1} × Gi × {1} × · · · × {1} isomorphic to Gi, and it is easy to verify that
elements of two distinct such subgroups commute with each other. As we
mentioned in Chapter 7, this construction yields the product in the category
of groups.
In our study of fundamental groups, we will need to build another kind
of product, in which the elements of diﬀerent groups are not assumed to
commute. This situation arises, for example, in computing the fundamental
group of the wedge X ∨Y of two spaces X and Y , deﬁned in Example
3.25. As we will see in the next chapter, the fundamental group of X ∨Y
contains subgroups isomorphic to π1(X) and π1(Y ), and any loop in X ∨Y
is equivalent to a product of loops lying in one space or the other. But in
general, path classes of loops in X do not commute with those in Y .
In this section we will introduce a more complicated product of groups
G1, . . . , Gn that includes each Gi as a subgroup, but in which elements of
the diﬀerent subgroups do not commute with each other. It is called the
“free product,” and roughly speaking, it is just the set of expressions you
can get by formally multiplying together elements of the diﬀerent groups,
with no relations assumed other than those that come from the multipli-
cation in each group Gi. It turns out (despite its name) to be the sum in
the category of groups.
Because terms such as “expressions you can get” and “multiplying ele-
ments of diﬀerent groups” are too vague to use in mathematical arguments,
the actual construction of the free product is rather involved. We begin with
some preliminary terminology.
Let {Gα}α∈A be an indexed collection of groups. The index set A can
be ﬁnite or inﬁnite; for our applications we will need only the ﬁnite case,
so you are free to think of ﬁnite collections throughout this chapter. We
will usually omit mention of A and denote the collection simply by {Gα},
with Greek letters understood to range over all elements of some implicitly
understood index set.
A word in {Gα} is a ﬁnite sequence of length m ≥0 of elements of the
disjoint union 
α Gα. In other words, a word is an ordered m-tuple of the
form (g1, . . . , gm), where each gi is an element of some Gα. (Recall that
formally, an element of the disjoint union is a pair (g, α), where α is a
“tag” to distinguish which group g came from. We will suppress the tag
in our notation, but remember that elements of groups corresponding to
diﬀerent indices have to be considered distinct, even if the groups are the
same.) The sequence of length zero, called the empty word, is denoted by
( ). Let W denote the set of all words in {Gα}. We denote the identity
element of Gα by 1α.
Deﬁne a multiplication operation in W by concatenation:
(g1, . . . , gm)(h1, . . . , hl) = (g1, . . . , gm, h1, . . . , hl).

Free Products
195
Clearly, this multiplication is associative, and has the empty word as a two-
sided identity element. However, there are two problems with this structure
as it stands: First, W is not a group under this operation because there are
no inverses; and second, the group structures of the various groups Gα have
not played a role in the deﬁnition so far.
To solve both of these problems, we deﬁne an equivalence relation on the
set of words as follows. An elementary reduction is an operation of one of
the following forms:
(g1, . . . , gi, gi+1, . . . , gm) 
→(g1, . . . , gigi+1, . . . , gm) if gi, gi+1 ∈some Gα;
(g1, . . . , gi−1, 1α, gi+1, . . . , gm) 
→(g1, . . . , gi−1, gi+1, . . . , gm).
The ﬁrst operation just multiplies together two consecutive entries, pro-
vided that they are elements of the same group, and the second deletes
any identity element that appears in a word. We say that two words are
equivalent, written W ∼W ′, if one can be transformed into the other by
a ﬁnite sequence of elementary reductions or their inverses; this is obvi-
ously an equivalence relation. The set of equivalence classes is called the
free product of the groups {Gα}, and is denoted by ∗αGα. In the case of a
ﬁnite set of groups, we just write G1 ∗· · · ∗Gn.
Lemma 9.1. Given any collection of groups {Gα}, their free product is a
group under the multiplication operation induced by multiplication of words.
Proof. First we need to check that multiplication of words respects the
equivalence relation. If V ′ is obtained from V by an elementary reduction,
then it is easy to see that V ′W is similarly obtained from V W, as is WV ′
from WV . If V ∼V ′ and W ∼W ′, it follows by induction on the number
of elementary reductions that V W ∼V ′W ′. Thus multiplication is well-
deﬁned on equivalence classes.
The equivalence class of the empty word ( ) is obviously an identity
element, and multiplication is associative on equivalence classes because it
already is on words. Finally, for any word (g1, . . . , gm), it is easy to check
that
(g1, . . . , gm)(g−1
m , . . . , g−1
1 ) ∼( ) ∼(g−1
m , . . . , g−1
1 )(g1, . . . , gm),
so the equivalence class of (g−1
m , . . . , g−1
1 ) is an inverse for that of
(g1, . . . , gm).
Henceforth, we will denote the identity element of the free product (the
equivalence class of the empty word) by 1.
For many purposes it is important to have a unique representative of each
equivalence class in the free product. We say that a word (g1, . . . , gm) is
reduced if it cannot be shortened by an elementary reduction. Speciﬁcally,
this means that no element gi is the identity of its group, and no two

196
9. Some Group Theory
consecutive elements gi, gi+1 come from the same group. It is easy to see
that any word is equivalent to a reduced word: Just perform elementary
reductions until it is impossible to perform any more. What is not so easy
to see is that the reduced word representing any given equivalence class is
unique.
Proposition 9.2. Every element of ∗αGα is represented by a unique re-
duced word.
Proof. We showed above that every equivalence class contains a reduced
word, so we need only check that two reduced words representing the same
equivalence class must be equal. This amounts to constructing a “canonical
reduction algorithm.”
Let R denote the set of reduced words. We begin by constructing a map
W × R →R,
which sends (g1, . . . , gm) ∈W and (h1, . . . , hl) ∈R to a reduced word that
we denote by (g1, . . . , gm) · (h1, . . . , hl) ∈R. We will deﬁne the map by
induction on m, the length of the word in W. For m = 0, deﬁne
( ) · (h1, . . . , hl) = (h1, . . . , hl).
For m = 1 and g ∈Gα, set
(g) · (h1, . . . , hl) =
⎧
⎪
⎪
⎪
⎨
⎪
⎪
⎪
⎩
(h2, . . . , hl),
h1 ∈Gα and gh1 = 1α;
(gh1, . . . , hl),
h1 ∈Gα and gh1 ̸= 1α;
(h1, . . . , hl),
h1 ̸∈Gα and g = 1α;
(g, h1, . . . , hl),
h1 ̸∈Gα and g ̸= 1α.
(The idea is just to multiply the two words and reduce them in the obvious
way; what is important about this deﬁnition is that there are no arbitrary
choices involved.) For m > 1, deﬁne the map recursively:
(g1, . . . , gm) · (h1, . . . , hl) = (g1) ·

(g2, . . . , gm) · (h1, . . . , hl)

= (g1) · (g2) · · · · · (gm) · (h1, . . . , hl),
where we understand the dot operation to be performed from right to left:
U · V · W = U · (V · W).
The key feature of this operation is that it takes equivalent words to the
same reduced word: If W ∼W ′, then W ·V = W ′·V for all reduced words
V . To prove this, it suﬃces to assume that W ′ is obtained from W by an
elementary reduction. There are two cases, corresponding to the two types
of elementary reduction. Suppose ﬁrst that W = (g1, . . . , gi, gi+1, . . . , gm),

Free Products
197
and W ′ = (g1, . . . , gigi+1, . . . , gm) is obtained by multiplying together two
consecutive elements gi, gi+1 from the same group Gα. Then
W · V = (g1) · · · · · (gi−1) · (gi) · (gi+1) · (gi+2) · · · · · (gm) · V.
Writing (gi+2) · · · · · (gm) · V = (h1, . . . , hl), it suﬃces to show that
(gi) · (gi+1) · (h1, . . . , hl) = (gigi+1) · (h1, . . . , hl).
Applying the deﬁnition of the dot operator twice and keeping careful track
of the various cases, you can compute
(gi) · (gi+1) · (h1, . . . , hl)
=
⎧
⎪
⎪
⎪
⎨
⎪
⎪
⎪
⎩
(h2, . . . , hl),
h1 ∈Gα, gigi+1h1 = 1α;
(gigi+1h1, . . . , hl),
h1 ∈Gα, gigi+1h1 ̸= 1α;
(h1, . . . , hl),
h1 ̸∈Gα, gigi+1 = 1α;
(gigi+1, h1, . . . , hl),
h1 ̸∈Gα, gigi+1 ̸= 1α.
On the other hand, (gigi+1) · (h1, . . . , hl) is equal to the same value by
deﬁnition. The second case, in which W contains an identity element that
is deleted to obtain W ′, follows in a similar way from the fact that (1α)·V =
V .
Now we deﬁne our canonical reduction operator r: W →R by r(W) =
W ·( ). Clearly, if W is already reduced, then r(W) = W. Moreover, by the
argument above, if W ∼W ′, then r(W) = r(W ′). Thus, if W ∼W ′ and
both are reduced words, we have W = r(W) = r(W ′) = W ′. This proves
the proposition.
For each group Gα, there is a canonical map ια : Gα →∗αGα, deﬁned by
sending g ∈Gα to the equivalence class of the word (g). Each of these maps
is a homomorphism, since (g1g2) ∼(g1)(g2) for g1, g2 ∈Gα. Each map is
also injective: If g ̸= 1α, both the words ια(g) = (g) and ια(1α) = ( ) are
reduced, and therefore cannot represent the same equivalence class because
of the preceding proposition. We usually identify Gα with its image under
the injection ια, and write the equivalence class of the word (g) simply as
g. Therefore, the equivalence class of a word (g1, g2, . . . , gm) can be written
g1g2 · · · gm; by a slight abuse of terminology, we will also call such a product
a word, and say that it is reduced if the word (g1, g2, . . . , gm) is reduced.
Multiplication in the free product is indicated by juxtaposition of such
words. Thus we have ﬁnally succeeded in making mathematical sense of
products of elements in diﬀerent groups.
Example 9.3. Let Z/⟨2⟩denote the group of integers modulo 2. The free
product Z/⟨2⟩∗Z/⟨2⟩can be described as follows. If we let β and γ denote

198
9. Some Group Theory
the nontrivial elements of the ﬁrst and second copies of Z/⟨2⟩, respectively,
each element of Z/⟨2⟩∗Z/⟨2⟩other than the identity has a unique repre-
sentation as a string of alternating β’s and γ’s. Multiplication is performed
by concatenating the strings and deleting all consecutive pairs of β’s or γ’s.
For example,
(βγβγβ)(γβγβ) = βγβγβγβγβ;
(γβγβ)(βγβγβ) = β.
This group is not abelian.
Example 9.4. Later we will need to consider the free product π1(S1, 1) ∗
π1(S1, 1). Letting α(s) = e2πis as in the preceding chapter, and letting β, γ
denote the path classes of α in the ﬁrst and second copies of π1(S1, 1),
respectively, each element of π1(S1, 1) ∗π1(S1, 1) other than the identity
has a unique expression of the form βi1γj1 · · · βimγjm, where i1 or jm may
be zero, but none of the other exponents is zero.
The free product of groups has an important characteristic property.
Theorem 9.5 (Characteristic Property of the Free Product).
For any group H and any collection of homomorphisms ϕα : Gα →H,
there exists a unique homomorphism Φ: ∗α Gα →H such that for each α
the following diagram commutes:
Gα
H.
-
ϕα
Φ
@
@@
R
∗αGα
6
ια
(9.1)
Proof. Suppose we are given a collection of homomorphisms ϕα : Gα →H.
The requirement that Φ ◦ια = ϕα implies that the desired homomorphism
Φ must satisfy
Φ(g) = ϕα(g)
if g ∈Gα,
(9.2)
where, as usual, we identify Gα with its image under ια. Since Φ is supposed
to be a homomorphism, it must satisfy
Φ(g1 · · · gm) = Φ(g1) · · · Φ(gm).
(9.3)
Therefore, if Φ and Φ both satisfy the conclusion, they must be equal
because both must satisfy (9.2) and (9.3). This proves that Φ is unique if
it exists.
To prove existence of Φ, we use (9.2) and (9.3) to deﬁne it. This is clearly
a homomorphism that satisﬁes the required properties, provided that it is

Free Groups
199
well-deﬁned. To verify that it is well-deﬁned, we need to check that it gives
the same result when applied to equivalent words. As usual, we need only
check elementary reductions. If gi, gi+1 ∈Gα, we have
Φ(gigi+1) = ϕα(gigi+1) = ϕα(gi)ϕα(gi+1) = Φ(gi)Φ(gi+1),
from which it follows that the deﬁnition of Φ is unchanged by multiply-
ing together successive elements of the same group. Similarly, Φ(1α) =
ϕα(1α) = 1 ∈H, which shows that Φ is unchanged by deleting an identity
element. This completes the proof.
Corollary 9.6. The free product is the sum in the category of groups.
Proof. The characteristic property is exactly the deﬁning property of the
sum in a category.
Corollary 9.7. The free product is the unique group (up to isomorphism)
satisfying the characteristic property.
Proof. Lemma 7.37 shows that sums in any category are unique up to
isomorphism.
In some texts, a free product is deﬁned as any group satisfying the char-
acteristic property, or as the sum in the category of groups. One must then
prove the existence of such a group by some construction such as the one
we have given before one is entitled to talk about “the” free product. Once
existence is proved, uniqueness follows automatically from category theory.
The nice thing about this uniqueness result is that no matter what speciﬁc
construction is used to deﬁne the free product (and you will ﬁnd many in
the literature), they are all the same up to isomorphism.
Free Groups
In this section we will use the free product construction to create a new
class of groups called “free groups,” consisting of all possible products of a
set of “generators,” with no relations imposed at all. We begin with a few
more deﬁnitions.
Let G be a group. A subset S ⊂G is said to generate G, and the elements
of S are called generators for G, if every element of G can be written as
a product of elements of S. Of course, any group has a set of generators,
since we can take S to be the whole group G. But it is more interesting to
ﬁnd a small set of generators when possible.
For example, a cyclic group is a group with one generator (see the Ap-
pendix). The cyclic groups are all isomorphic either to Z or to Z/⟨n⟩for
some n (Exercise A.26).

200
9. Some Group Theory
In this section we will be concerned mostly with inﬁnite cyclic groups.
Given any object α, we can form an inﬁnite cyclic group generated by
α, denoted by ⟨α⟩, as follows: ⟨α⟩is the set {α} × Z with multiplication
(α, m)(α, k) = (α, k + m). We identify α with the element (α, 1); thus we
can abbreviate (α, m) by αm, and think of ⟨α⟩as the group of all integral
powers of α with the obvious multiplication.
Now suppose we are given any set S. We deﬁne the free group on S,
denoted by ⟨S⟩, to be the free product of all the inﬁnite cyclic groups
generated by elements of S:
⟨S⟩= ∗
α∈S⟨α⟩.
There is a natural injection ι: S 	→⟨S⟩, deﬁned by sending each α ∈S to
the word α ∈⟨S⟩. Thus we can consider S as a subset of ⟨S⟩, and each
element of ⟨S⟩can be expressed as a word αn1
1 αn2
2 · · · αnm
m , where each αi is
some element of S and each ni is an integer. Multiplication is performed by
juxtaposition and combining consecutive powers of the same αi by the rule
αn
i αk
i = αn+k
i
. In case S = {α1, . . . , αn} is a ﬁnite set, we denote the free
group on S by ⟨α1, . . . , αn⟩instead of the more accurate but cumbersome
notation ⟨{α1, . . . , αn}⟩. (We will rely on the context and typographical
diﬀerences to make clear the distinction between the free group ⟨S⟩on the
elements of the set S and the inﬁnite cyclic group ⟨α⟩, which is also equal
to the free group on the singleton {α}.)
Example 9.8. The free group on the empty set, denoted by ⟨⟩, is by
convention just the trivial group {1}. The free group on a singleton {α} is
the inﬁnite cyclic group ⟨α⟩. The free group on the two-element set {β, γ}
is ⟨β, γ⟩= ⟨β⟩∗⟨γ⟩, which is the same as the group described in Example
9.4.
Theorem 9.9 (Characteristic Property of the Free Group).
Let
S be a set. For any group H and any map ϕ: S →H, there exists a unique
homomorphism ϕ: ⟨S⟩→H extending ϕ:
S
H.
-
ϕ
ϕ
@
@@
R
⟨S⟩
6
ι
(9.4)
Proof. This can be proved directly as in the proof of Theorem 9.5. Alter-
natively, recalling that the free group is deﬁned as a free product, we can
proceed as follows. There is a one-to-one correspondence between set func-
tions ϕ: S →H and collections of homomorphisms ϕα : ⟨α⟩→H for all

Presentations of Groups
201
α ∈S, by the equation
ϕα(αn) = ϕ(α)n.
Translating the characteristic property of the free product to this special
case and using this correspondence yields the result. The details are left as
an exercise.
Exercise 9.1.
Carry out the details of the proof of Theorem 9.9.
Exercise 9.2.
Prove that the free group on S is the unique group (up to
isomorphism) satisfying the characteristic property.
Presentations of Groups
It is often convenient to describe a group by giving a set of generators for
it, and listing a few rules, or “relations,” that describe how to multiply the
generators together. For example, the cyclic group of order n generated by
γ might be described as the group generated by γ with the single relation
γn = 1; all other relations in the group, such as γ3n = 1 or γk−n = γk,
follow from this one. The direct product group Z × Z might be described
as the group with two generators β, γ satisfying the relation βγ = γβ. The
free group ⟨β, γ⟩can be described as the group generated by β, γ with no
relations.
So far, this is mathematically very vague. What does it mean to say that
“all other relations follow from a given one”? In this section we develop a
way to make these notions precise.
We deﬁne a group presentation to be an ordered pair, denoted by ⟨S|R⟩,
where S is an arbitrary set and R is a set of elements of the free group ⟨S⟩.
The elements of S and R are called the generators and relators, respectively,
of the presentation. A group presentation deﬁnes a group, also denoted by
⟨S|R⟩, as the following quotient:
⟨S|R⟩= ⟨S⟩/ R,
where R is the normal closure of R in ⟨S⟩, which is the intersection of all
normal subgroups of ⟨S⟩containing R; thus R is the “smallest” normal
subgroup containing R.
Since the quotient of a group by a normal subgroup is again a group
(see the Appendix), ⟨S|R⟩is indeed a group. Each of the generators s ∈S
determines an element in ⟨S|R⟩(its coset in the quotient group), which we
usually write also as s. Each of the relators r ∈R represents a particular
product of generators and their inverses that is equal to 1 in the quotient.

202
9. Some Group Theory
Here is the intuition behind this construction. If G is any group generated
by S, there is a surjective homomorphism Φ: ⟨S⟩→G, whose existence is
guaranteed by the characteristic property of the free group. If all the words
of R are to be equal to the identity in G, then the kernel of Φ must at
least contain R, and since it is normal, it must contain R; thus by the ﬁrst
isomorphism theorem (Theorem A.13 in the Appendix), G is isomorphic
to a quotient of ⟨S⟩by a normal subgroup containing R. By dividing out
exactly R, we ensure that the only relations that hold in ⟨S|R⟩are those
that are forced by the relators in R. Thus, in a certain sense, ⟨S|R⟩is the
“largest” group generated by S in which all the products represented by
elements of R are equal to 1.
If G is a group and there exists an isomorphism ⟨S|R⟩∼= G, we say that
⟨S|R⟩is a presentation of G. At this point, the question naturally arises
whether every group has a presentation. In fact, the answer is yes, but
the result is not as satisfying as we might have hoped. Given a group G,
the set of all elements of G certainly generates G. By the characteristic
property of the free group, the identity map of G to itself has a unique
extension to a homomorphism Φ: ⟨G⟩→G. If we set R = Ker Φ, then the
ﬁrst isomorphism theorem says that G ∼= ⟨G⟩/R. Since R is normal, it is
equal to its normal closure, and therefore G has the presentation ⟨G|R⟩.
This is highly ineﬃcient, of course, since both ⟨G⟩and R are vastly larger
than G itself.
If G admits a presentation ⟨S|R⟩in which both S and R are ﬁnite sets,
we say that G is ﬁnitely presented. In this case, we usually write the presen-
tation as ⟨α1, . . . , αn | r1, . . . , rm⟩. Since the ri actually all become equal to
the identity in the group deﬁned by the presentation, it is also often con-
venient to replace the relators by the equations obtained by setting them
equal to the identity, called relations of the presentation, as in
⟨α1, . . . , αn | r1 = 1, . . . , rm = 1⟩
or even
⟨α1, . . . , αn | r1 = q1, . . . , rm = qm⟩.
We take this to be an alternative notation for ⟨α1, . . . , αn | r1q−1
1 , . . . ,
rmq−1
m ⟩.
We conclude this section by describing one important example in detail.
Proposition 9.10. The group Z×Z has the presentation ⟨β, γ | βγ = γβ⟩.
Proof. For brevity, write G = ⟨β, γ | βγ = γβ⟩= ⟨β, γ | βγβ−1γ−1⟩. As
usual, we will use the symbols β and γ to denote either the generators of
the free group ⟨β, γ⟩or their images in the quotient group G. We begin by
noting that G is abelian: The equation βγβ−1γ−1 = 1, which holds in G
by deﬁnition, immediately implies βγ = γβ, and then a simple induction

Free Abelian Groups
203
shows that any products of powers of β and γ commute with each other.
Since β and γ generate G, this suﬃces.
We will prove the proposition by deﬁning homomorphisms Φ: G →Z×Z
and Ψ: Z × Z →G and showing that they are inverses of each other. To
deﬁne Φ, we ﬁrst deﬁne Φ: ⟨β, γ⟩→Z × Z by setting Φ(β) = (1, 0) and
Φ(γ) = (0, 1); this uniquely determines Φ by the characteristic property of
the free group. Explicitly, Φ is given by
Φ(βi1γj1 · · · βimγjm) = (i1 + · · · + im, j1 + · · · + jm).
(9.5)
Because βγβ−1γ−1 ∈Ker Φ by direct computation, Φ descends to a map
Φ: G →Z × Z still given by (9.5).
In the other direction, we deﬁne Ψ: Z × Z →G by
Ψ(m, n) = βmγn.
It follows from the fact that G is abelian that Ψ is a homomorphism. A
simple computation shows that Ψ ◦Φ(β) = β, Ψ ◦Φ(γ) = γ, and Φ ◦
Ψ(m, n) = (m, n). Thus Φ and Ψ are inverses, so G ∼= Z × Z.
In some ways, a presentation gives a very simple and concrete way to
understand the properties of a group, and we will describe the fundamental
groups of surfaces in the next chapter by giving presentations. However,
you should be aware that even with a ﬁnite presentation in hand, some
very basic questions about a group may still be diﬃcult or impossible to
answer. For example, two of the most basic problems concerning group
presentations were ﬁrst posed around 1910 by topologists Heinrich Tietze
and Max Dehn, shortly after the invention of the fundamental group: The
isomorphism problem for groups is to decide, given two ﬁnite presentations,
whether the resulting groups are isomorphic; and the word problem is to
decide, given a ﬁnite presentation ⟨S|R⟩and a speciﬁc word formed from
elements of S, whether that word represents the identity element of the
group ⟨S|R⟩. It was shown in the 1950s that there is no algorithm for
solving either of these problems that is guaranteed to yield an answer for
every presentation in a ﬁnite amount of time! (See [Sti82] for references and
historical background.) These ideas form the basis for the subject called
combinatorial group theory, which is a lively research ﬁeld at the intersec-
tion of algebra, topology, and geometry.
Free Abelian Groups
There is an analogue of free groups in the category of abelian groups. In
this section, since all our groups will be abelian, we will always write the
group operation additively, and denote the identity element by 0 and the

204
9. Some Group Theory
inverse of x by −x. If G is an abelian group, g ∈G, and n ∈Z, the notation
ng means the n-fold sum g + · · · + g, and nG is the subgroup {ng : g ∈G}.
Given a nonempty set S, let Z⟨S⟩denote the set of all functions k: S →Z
such that k(s) = 0 for all but ﬁnitely many s ∈S. This is easily seen to be
an abelian group under addition, called the free abelian group on S. Just
as we did for the free vector space deﬁned in Chapter 5, we can identify
each s ∈S with the element of Z⟨S⟩that takes the value 1 on s and zero
on every other element of S, so we consider S as a subset of Z⟨S⟩, and each
element of Z⟨S⟩can be written uniquely as a ﬁnite sum of the form
n

i=1
kisi
where si are elements of S and ki are integers. When S = {s1, . . . , sn} is a
ﬁnite set, we will usually write the free abelian group on S as Z⟨s1, . . . , sn⟩.
By convention, the free abelian group on the empty set is the trivial group
{0} (we consider a “linear combination of no elements” to sum to 0).
Lemma 9.11 (Properties of Free Abelian Groups).
Let
S
be
a
nonempty set.
(a) Characteristic Property: Given any abelian group H and any
set map f : S →H, there exists a unique homomorphism f : Z⟨S⟩→
H extending f.
(b) Z⟨S⟩is isomorphic to the direct sum 
s∈S⟨s⟩of all the inﬁnite cyclic
groups generated by elements of S.
(c) If S = {s1, . . . , sn} is ﬁnite, then Z⟨s1, . . . , sn⟩is isomorphic to Zn
via the map (k1, . . . , kn) 
→k1s1 + · · · + knsn.
Exercise 9.3.
Prove Lemma 9.11.
Let G be an abelian group. By analogy with vector spaces, a ﬁnite sum
of elements of G with integer coeﬃcients is called a linear combination of
elements of G. A nonempty subset S ⊂G is said to be linearly independent
if the only linear combination of elements of S that equals zero is the one
for which all the coeﬃcients are zero. A basis for G is a linearly independent
subset that generates G. Just as in the case of vector spaces, if S is a basis
for G, every element of G can be written uniquely as a linear combination
of elements of S. For example, S is a basis for the free abelian group Z⟨S⟩.
The set of elements ei = (0, . . . , 1, . . . , 0) (with a 1 in the ith place) for
i = 1, . . . , n is a basis for Zn, which we call the standard basis.
If a group G is isomorphic to Z⟨S⟩for some set S, G is also said to be
free abelian.

Free Abelian Groups
205
Exercise 9.4.
(a) Show that an abelian group is free abelian if and only if it has a basis.
(b) Show that any two free abelian groups whose bases have the same
cardinality are isomorphic.
Lemma 9.12. If G has a ﬁnite basis, then every ﬁnite basis has the same
number of elements.
Proof. Suppose G has a basis with n elements. Then G ∼= Zn by Lemma
9.11(c), and the quotient group G/2G is easily seen to be isomorphic to
(Z/⟨2⟩)n, which has exactly 2n elements. Since the order of G/2G is inde-
pendent of the choice of basis, every ﬁnite basis must have n elements.
In view of this lemma, if G is a free abelian group with a ﬁnite basis, we
deﬁne the rank of G to be the number of elements in any ﬁnite basis. (In
fact, in that case every basis is ﬁnite—see Problem 9-6.) If G has no ﬁnite
basis, we say it has inﬁnite rank.
Proposition 9.13. Suppose G is a free abelian group of ﬁnite rank. Any
subgroup of G is free abelian of rank less than or equal to that of G.
Proof. We may assume without loss of generality that G = Zn. We will
prove the proposition by induction on n. For n = 1, it follows from the fact
that any subgroup of a cyclic group is cyclic.
Suppose the result is true for subgroups of Zn−1, and let H be any
subgroup of Zn. Identifying Zn−1 with the subgroup {(k1, . . . , kn−1, 0)} of
Zn, the inductive hypothesis guarantees that H ∩Zn−1 is free abelian of
rank m −1 ≤n −1, so has a basis {h1, . . . , hm−1}. If H ⊂Zn−1, we are
done. Otherwise, the image of H under the projection πn : Zn →Z onto
the nth factor is a nontrivial cyclic subgroup of Z. Let c ∈Z be a generator
of this subgroup, and let hm be an element of H such that πn(hm) = c.
The proof will be complete once we show that {h1, . . . , hm} is a basis for
H.
Suppose a1h1 + · · · + amhm = 0. Applying πn to this equation yields
amc = 0, so am = 0. Then a1 = · · · = am−1 = 0 because of the inde-
pendence of {h1, . . . , hm−1}, so {h1, . . . , hm} is linearly independent. Now
suppose h ∈H is arbitrary. Then πn(h) = ac for some integer a, so
h −ahm ∈H ∩Zn−1. This element can be written as a linear combination
of {h1, . . . , hm−1}, which shows that H is generated by {h1, . . . , hm}.
We will need to extend the notion of rank to ﬁnitely generated abelian
groups that are not necessarily free abelian. To that end, we say that an
element g of an abelian group G is a torsion element if ng = 0 for some
nonzero n ∈Z. If ng = n′g′ = 0, then nn′(g + g′) = 0, so the set of all
torsion elements is a subgroup Gtor of G, called the torsion subgroup. We
say that G is torsion free if the only torsion element is 0. It is easy to check
that the quotient group G/Gtor is torsion free.

206
9. Some Group Theory
Proposition 9.14. Any abelian group that is ﬁnitely generated and torsion
free is free abelian of ﬁnite rank.
Proof. Suppose G is such a group. For any linearly independent subset S ⊂
G, we will extend our notation slightly and let Z⟨S⟩denote the subgroup
of G generated by S. It is easily seen to be free abelian with S as a basis,
so this is consistent with our earlier notation.
The crux of the proof is the following claim: There exists a nonzero
integer n and a ﬁnite linearly independent set S ⊂G such that nG ⊂Z⟨S⟩.
Assuming this, the rest of the proof goes as follows. Let ϕ: G →G be
the homomorphism ϕ(g) = ng. It is injective because G is torsion free,
and the claim implies that ϕ(G) ⊂Z⟨S⟩. Thus G is isomorphic to the
subgroup ϕ(G) of the free abelian group Z⟨S⟩, so by Proposition 9.13, G
is free abelian of ﬁnite rank.
We will prove the claim by induction on the number of elements in a
generating set for G. If G is generated by one element g, the claim is true
with n = 1, because the fact that G is torsion free implies that {g} is a
linearly independent set.
Now assume that the claim is true for any torsion-free group generated
by m −1 elements, and suppose G is generated by a set T = {g1, . . . , gm}
with m elements. If T is linearly independent, we just take S = T. If not,
there is a relation of the form a1g1 + · · · + amgm = 0 with at least one of
the coeﬃcients, say am, not equal to zero. Letting G′ denote the subgroup
of G generated by {g1, . . . , gm−1}, this means that amgm ∈G′. Since G′ is
generated by m −1 elements, by induction there exist a nonzero integer n′
and a ﬁnite linearly independent set S ⊂G′ such that n′G′ ⊂Z⟨S⟩. Let
n = amn′. Since G is generated by T, for any g ∈G we have
ng = amn′(b1g1 + · · · + bmgm)
= n′(amb1g1 + · · · + ambm−1gm−1) + n′bm(amgm).
Both terms above are in n′G′ ⊂Z⟨S⟩. It follows that nG ⊂Z⟨S⟩, which
completes the proof.
Now let G be any ﬁnitely generated abelian group. Because G/Gtor is
ﬁnitely generated and torsion free, the preceding proposition implies that
it is free abelian of ﬁnite rank. Thus we can deﬁne the rank of G to be the
rank of G/Gtor.
Example 9.15. The rank of Zn is n, and the rank of any ﬁnite group
is 0 (since every element is a torsion element). The rank of a product
group of the form G = Zn × Z/⟨k1⟩× · · · × Z/⟨km⟩is n, because Gtor =
Z/⟨k1⟩× · · · × Z/⟨km⟩.
Proposition 9.16. If G is a free abelian group of ﬁnite rank and f : G →
H is a surjective homomorphism, then rank G = rank H + rank(Ker f).

Free Abelian Groups
207
Proof. Write K = Ker f. By Proposition 9.13, K is a ﬁnitely generated
free abelian group, so we can choose elements k1, . . . , kp ∈G that form a
basis for K.
Since f is surjective, it takes a set of generators for G to a set of generators
for H; thus H is ﬁnitely generated and its rank is the rank of H/Htor.
Choose a basis h1, . . . ,hq for H/Htor, and lift them to elements h1, . . . , hq ∈
H. By surjectivity, there are elements gj ∈G such that f(gj) = hj.
The set {ki, gj} is linearly independent, because a relation of the form
g = 
i miki + 
j njgj = 0 implies
0 = f(g) =

j
njf(gj) =

j
njhj.
Projecting this to the quotient group H/Htor, we obtain a relation of
the form 
j njhj = 0, which implies nj = 0 for each j. Therefore,
g = 
i miki = 0, so mi = 0.
Let Z⟨ki, gj⟩denote the subgroup of G generated by {ki, gj}. It is free
abelian of rank p + q = rank K + rank H, so from Proposition 9.13 we
conclude that rank K + rank H ≤rank G. The proof will be complete once
we show the reverse inequality.
Because Htor is a ﬁnitely generated torsion group, there is an integer
N such that Nt = 0 for every t ∈Htor. Let g ∈G be arbitrary, and let
[f(g)] denote the equivalence class of f(g) in the quotient H/Htor. Writing
[f(g)] = 
j njhj, we have [f(g −
j njgj)] = 0, so f(g −
j njgj) ∈Htor.
This implies N(g −
j njgj) ∈K, so we can write
Ng =

j
Nnjgj +

i
miki.
Letting ϕ: G →G be the homomorphism ϕ(g) = Ng as in the proof
of Proposition 9.14, we have shown that ϕ(G) ⊂Z⟨ki, gj⟩. Moreover, ϕ is
injective because G is torsion free, so by Proposition 9.13 again we conclude
that rank G ≤p + q = rank K + rank H.

208
9. Some Group Theory
Problems
9-1. Show that any free product of two or more nontrivial groups is inﬁnite
and nonabelian.
9-2. Show that the following groups have the given presentations.
(a) Z/⟨n⟩∼= ⟨β | βn = 1⟩.
(b) Z/⟨m⟩× Z/⟨n⟩∼= ⟨β, γ | βm = 1, γn = 1, βγ = γβ⟩.
9-3. The center of a group G is the set Z of elements of G that commute
with every element of G: Z = {g ∈G : gh = hg for all h ∈G}. Show
that a free group on two or more generators has center consisting of
the identity alone.
9-4. Let G1, G2, H1, H2 be groups, and let fi : Gi →Hi be group homo-
morphisms for i = 1, 2.
(a) Using the characteristic property of the free product, show that
there is a unique homomorphism f1 ∗f2 : G1 ∗G2 →H1 ∗H2
such that the following diagram commutes for i = 1, 2:
Gi
Hi,
-
fi
G1 ∗G2
H1 ∗H2
-
f1 ∗f2
6
ιi
6
ι′
i
where ιi : Gi →G1 ∗G2 and ι′
i : Hi →H1 ∗H2 are the canonical
injections.
(b) Show that Ker f1 ∗f2 = Im j1 ∗j2, where ji : Ker fi 	→Gi is
inclusion:
Ker f1 ∗Ker f2
j1∗j2
−→G1 ∗G2
f1∗f2
−→H1 ∗H2.
9-5. Show that the free abelian group on a set S is uniquely determined
up to isomorphism by the characteristic property (Lemma 9.11(a)).
9-6. Suppose G is a free abelian group of ﬁnite rank. Show that every
basis of G is ﬁnite.

10
The Seifert–Van Kampen Theorem
In this section we will develop the techniques needed to compute the fun-
damental groups of all compact surfaces, and a good many other spaces
as well. The basic tool is the Seifert–Van Kampen theorem, which gives a
formula for the fundamental group of a space that can be decomposed as
the union of two open, path connected subsets whose intersection is also
path connected.
In the ﬁrst section we state a rather general version of the theorem. Then
we examine two special cases in which the formula simpliﬁes considerably.
The ﬁrst special case is that in which the intersection of the two subsets is
simply connected: Then the theorem says that the fundamental group of
the big space is the free product of the fundamental groups of its subspaces.
As an application, we compute the fundamental groups of a wedge of spaces
and of a graph (a one-dimensional simplicial complex). The second special
case is that in which one of the two subsets is itself simply connected: Then
the fundamental group of the big space is the quotient of the fundamental
group of the non–simply connected piece by the path classes in the inter-
section. We use this formula to compute the fundamental groups of the
compact surfaces.
After these applications, we give a detailed proof of the Seifert–Van Kam-
pen theorem. Then in the last section of the chapter we revisit the classi-
ﬁcation of compact surfaces, and prove ﬁnally that the diﬀerent surfaces
on our list are all topologically distinct by showing that their fundamental
groups are not isomorphic.

210
10. The Seifert–Van Kampen Theorem
Statement of the Theorem
Here is the situation in which we will be able to compute fundamental
groups. Suppose we are given a space X that is the union of two open
subsets U, V ⊂X, and suppose we can compute the fundamental groups
of U, V , and U ∩V , each of which is path connected. As we will see below,
any loop in X can be written as a product of loops, each of which lies in
either U or V ; such a loop can be thought of as representing an element of
the free product π1(U)∗π1(V ). But any loop in U ∩V will represent only a
single element of π1(X), even though it represents two distinct elements of
the free product (one in π1(U) and one in π1(V )). Thus the fundamental
group of X can be thought of as the quotient of this free product modulo
some relations coming from π1(U ∩V ) that express this redundancy.
Let us set the stage for the precise statement of the theorem. Let X be
any topological space, let U, V ⊂X be open subsets whose union is X and
whose intersection is nonempty, and choose any base point q ∈U ∩V . The
four inclusion maps
j@
@@
R
U
U ∩V
i



V
l



X
k
@
@@
R
induce fundamental group homomorphisms
j∗@
@@
R
π1(U, q)
π1(U ∩V, q)
i∗



π1(V, q)
l∗



π1(X, q).
k∗
@
@@
R
Now insert the free product group π1(U, q) ∗π1(V, q) into the middle of
the picture, and let ιU : π1(U, q) 	→π1(U, q) ∗π1(V, q) and ιV : π1(V, q) 	→
π1(U, q) ∗π1(V, q) be the canonical injections. By the characteristic prop-
erty of the free product, k∗and l∗induce a homomorphism Φ: π1(U, q) ∗
π1(V, q) →π1(X, q) such that the right half of the following diagram com-

Statement of the Theorem
211
mutes:
π1(U, q)
i∗








?
ιU
k∗
@
@
@
@
@
@
@@
R
π1(V, q)
j∗
@
@
@
@
@
@
@@
R
π1(U ∩V, q)
π1(U, q) ∗π1(V, q)
-
F
π1(X, q).
-
Φ
6
ιV
l∗








(10.1)
Finally, we deﬁne a map F : π1(U ∩V, q) →π1(U, q) ∗π1(V, q) by setting
F(γ) = (i∗γ)−1(j∗γ). (F is not a homomorphism.) Let F(π1(U ∩V, q))
denote the normal closure of the image of F in π1(U, q) ∗π1(V, q).
Theorem 10.1 (Seifert–Van Kampen). Let X be a topological space.
Suppose U, V ⊂X are open subsets whose union is X, and suppose U, V ,
and U ∩V are path connected. Then, for any q ∈U ∩V , the homomor-
phism Φ deﬁned by (10.1) is surjective, and its kernel is F(π1(U ∩V, q)).
Therefore,
π1(X, q) ∼= π1(U, q) ∗π1(V, q)

F(π1(U ∩V, q)).
(10.2)
When the fundamental groups in question are ﬁnitely presented, the
theorem has a useful reformulation in terms of generators and relations.
Corollary 10.2. In addition to the hypotheses of the Seifert–Van Kampen
theorem, assume that the fundamental groups of U, V , and U ∩V have the
following ﬁnite presentations:
π1(U, q) ∼= ⟨α1, . . . , αm | ρ1, . . . , ρr⟩;
π1(V, q) ∼= ⟨β1, . . . , βn | σ1, . . . , σs⟩;
π1(U ∩V, q) ∼= ⟨γ1, . . . , γp | τ1, . . . , τt⟩.
Then π1(X, q) has the presentation
π1(X, q)
∼= ⟨α1, . . . , αm, β1, . . . , βn | ρ1, . . . , ρr, σ1, . . . , σs, u1 = v1, . . . , up = vp⟩,

212
10. The Seifert–Van Kampen Theorem
where for each a = 1, . . . , p, ua is an expression for i∗γa ∈π1(U, q) in terms
of the generators {α1, . . . , αm}, and va similarly expresses j∗γa ∈π1(V, q)
in terms of {β1, . . . , βn}.
The proofs of these two theorems are rather technical, so we will postpone
them until later in the chapter. Before proving them, we will illustrate their
use by computing a number of fundamental groups.
It is worth remarking here that the Seifert–Van Kampen theorem can
be generalized to a covering of X by any number, ﬁnite or inﬁnite, of path
connected open sets containing the base point. This generalization can be
found in [Sie92] or [Mas89].
Applications
All of our applications of the Seifert–Van Kampen theorem will be in special
cases in which one of the sets U, V , or U ∩V is simply connected.
First Special Case: Simply Connected Intersection
The ﬁrst special case of the Seifert–Van Kampen theorem we will con-
sider is that in which U ∩V is simply connected. In that case, the group
F(π1(U ∩V, q)) is trivial, so the following corollary is immediate.
Corollary 10.3. Assume the hypotheses of the Seifert–Van Kampen the-
orem, and suppose in addition that U ∩V is simply connected. Then Φ is
an isomorphism between π1(U, q) ∗π1(V, q) and π1(X, q).
As our ﬁrst application, we will compute the fundamental group of
a wedge of spaces. Recall from Example 3.25 that the wedge of spaces
X1, . . . , Xn with base points qj ∈Xj is the space X1∨· · ·∨Xn deﬁned as the
quotient of 
j Xj by the equivalence relation generated by q1 ∼· · · ∼qn.
A point q in a topological space X is said to be a nondegenerate base
point if q has a neighborhood that admits a strong deformation retraction
onto q and {q} is closed in X. For example, any base point in a manifold is
nondegenerate, because any Euclidean ball neighborhood admits a strong
deformation retraction onto any point. (In more advanced treatments of
homotopy theory a slightly more restrictive deﬁnition of nondegenerate
base point is used, but this one will suﬃce for our purposes.)
Observe that inclusion of Xj into 
j Xj followed by projection onto the
quotient induces continuous injective maps ιj : Xj 	→X1 ∨· · · ∨Xn. If
each base point qj is nondegenerate, then these are closed maps and thus
embeddings. Identifying each Xj with its image under ιj, we will consider
Xj as a subspace of X1∨· · ·∨Xn. We let ∗denote the point in X1∨· · ·∨Xn
that is the equivalence class of the base points q1, . . . , qn.

Applications
213
Lemma 10.4. Suppose qi ∈Xi is a nondegenerate base point for i =
1, . . . , n. Then ∗is a nondegenerate base point in X1 ∨· · · ∨Xn.
Proof. For each i, choose a neighborhood Ui of qi that admits a strong
deformation retraction Hi : Ui×I →Ui onto {qi}. Deﬁne a map H : 
i Ui×
I →
i Ui by letting H = Hi on Ui×I. The restriction of the quotient map
π to the saturated open set 
i Ui is a quotient map to a neighborhood U
of ∗. Since π ◦H respects the identiﬁcations made by π, it descends to the
quotient and yields a strong deformation retraction of U onto {∗}. To see
that {∗} is closed in X1 ∨· · · ∨Xn, we need only observe that its inverse
image under π is {q1, . . . , qn}, which is closed in the disjoint union because
its intersection {qi} with Xi is closed in Xi by hypothesis. Thus {∗} is
closed.
Proposition 10.5. Let X1, . . . , Xn be spaces with nondegenerate base
points qj ∈Xj. The map
Φ: π1(X1, q1) ∗· · · ∗π1(Xn, qn) →π1(X1 ∨· · · ∨Xn, ∗)
induced by ιj∗: π1(Xj, qj) →π1(X1 ∨· · · ∨Xn, ∗) is an isomorphism.
Proof. First consider the wedge of two spaces X1∨X2. We would like to use
Corollary 10.3 to the Seifert–Van Kampen theorem with U = X1, V = X2,
and U ∩V = {q}. The trouble is that these spaces are not open in X1 ∨X2,
so the corollary does not apply directly. To remedy this, we replace them
by slightly “thicker” spaces using the nondegenerate base point condition.
Choose neighborhoods Wi in which qi is a strong deformation retract,
and let U = π(X1 ⨿W2), V = π(X2 ⨿W1), where π: X1 ⨿X2 →X1 ∨X2 is
the quotient map (Figure 10.1). Since X1 ⨿W2 and X2 ⨿W1 are saturated
open sets in X1 ⨿X2, the restriction of π to each of them is a quotient map
and U and V are open in the wedge.
The key fact is that the three inclusion maps
{∗} 	→U ∩V,
X1 	→U,
X2 	→V
are all homotopy equivalences, because each subspace on the left-hand side
above is a strong deformation retract of the corresponding right-hand side.
For U ∩V , this follows immediately from the preceding lemma. For U,
choose a strong deformation retraction H2 : W2 × I →W2 of W2 onto q2,
and deﬁne G1 : X1 ⨿W2 × I →X1 ⨿W2 to be the identity on X1 × I and
H2 on W2 ×I; it descends to a strong deformation retraction of U onto X1.
A similar construction shows V ≃X2.

214
10. The Seifert–Van Kampen Theorem
X1
X2
X1 ∨X2
W1
W2
q1
q2
∗
U
V
π
FIGURE 10.1. Computing the fundamental group of a wedge.
Because U ∩V is contractible, Corollary 10.3 implies that the inclusion
maps U 	→X1 ∨X2 and V 	→X1 ∨X2 induce an isomorphism
π1(U, ∗) ∗π1(V, ∗) →π1(X1 ∨X2, ∗).
Moreover, the injections ι1 : X1 	→U and ι2 : X2 	→V , which are homotopy
equivalences, induce isomorphisms π1(X1, q1) →π1(U, ∗) and π1(X2, q2) →
π1(V, ∗). Composing these isomorphisms proves the proposition in the case
n = 2. The case of n > 2 spaces follows by induction, because Lemma 10.4
guarantees that the hypotheses of the proposition are satisﬁed by X1 and
X2 ∨· · · ∨Xn.
Example 10.6. The preceding proposition shows that the bouquet S1 ∨
· · ·∨S1 of n circles has fundamental group isomorphic to Z∗· · ·∗Z, which is
a free group on n generators. In fact, it shows more: Since the isomorphism
is induced by inclusion of each copy of S1 into the bouquet, we can write
explicit generators of this free group. If αi denotes the standard loop in the
ith copy of S1, then the fundamental group of the bouquet is just the free
group ⟨[α1], . . . , [αn]⟩.
As a second application, we will compute the fundamental group of a
ﬁnite graph. Let Γ be a ﬁnite connected graph, and choose a vertex v as
base point. A maximal tree in Γ is a subgraph that is a tree and is not
contained in any larger tree. The vertex v is contained in a (nonunique)
maximal tree: Just start with a single edge containing v and keep adding
edges until it is impossible to add another edge and still obtain a tree. Let
T ⊂Γ be such a maximal tree.

Applications
215
w1
w′
1
w2
w′
2
w3
w′
3
v
FIGURE 10.2. Generators for the fundamental group of a graph.
We will construct a set of generators for the fundamental group of Γ
as follows. Let ⟨w1, w′
1⟩, . . . , ⟨wn, w′
n⟩be the edges of Γ that are not in T
(Figure 10.2). For each i, by maximality of T there is a reduced cycle in
T ∪⟨wi, w′
i⟩that does not lie in T. This cycle must therefore traverse the
edge ⟨wi, w′
i⟩, which implies that both of the vertices wi and w′
i also belong
to edges in T. Thus we can choose paths gi and hi in T from v to wi and
w′
i, respectively. Let fi denote the loop in Γ obtained by ﬁrst following gi
from v to wi, then traversing ⟨wi, w′
i⟩, and then following h−1
i
from w′
i back
to v. Note that the path class [fi] is independent of the choices of gi and hi,
because any two paths in T with the same endpoints are path homotopic.
Theorem 10.7 (Fundamental Group of a Finite Graph). The fun-
damental group of a ﬁnite connected graph Γ based at a vertex v is the free
group on the path classes [f1], . . . , [fn] constructed above.
Proof. We prove the theorem by induction on n. If n = 0, then Γ is a tree
and hence simply connected, so there is nothing to prove.
For n = 1, we must show that Γ is the inﬁnite cyclic group generated
by [f1]. By assumption, there is a reduced cycle (v0, . . . , vm) in Γ (Figure
10.3(a)). If vi = vj for some i ̸= j other than v0 = vm, we can replace the
cycle by the shorter one (vi, . . . , vj). So we may assume that no vertex is
repeated in this cycle except v0 = vm. This cycle must traverse the edge
⟨w1, w′
1⟩, because otherwise it would be a reduced cycle in T. The subgraph
C ⊂Γ consisting of the vertices {v0, . . . , vm} and the intervening edges is
homeomorphic to S1 because it is isomorphic as a simplicial complex to
the complex Km of Example 5.7(d). We will show that inclusion C ⊂Γ is
a homotopy equivalence.
Let K be the union of all the edges in Γ∖C together with their vertices.
Each component Ki of K is a connected subgraph of Γ contained in T,
and is therefore a tree (since a reduced cycle in Ki would also be one
in T). Moreover, each such component shares exactly one vertex yi with

216
10. The Seifert–Van Kampen Theorem
y1
y2
y3 w1
w′
1
C
K1
K2
K3
(a) n = 1.
x1
x2
x3
xn
(b) n > 1.
FIGURE 10.3. Proof that the fundamental group of a graph is free.
C: If Ki ∩C contained two vertices yi, y′
i, it would be possible to ﬁnd a
reduced cycle in T by following a reduced edge path in Ki from yi to y′
i
followed by the reduced edge path in C from y′
i to yi that does not pass
through ⟨w1, w′
1⟩. (There must be at least one vertex in common because
Γ is connected.)
Now deﬁne a strong deformation retraction of Γ onto C as follows: On
each Ki, it is a strong deformation retraction of Ki onto yi, which exists by
Problem 7-13; and on C it is the identity. The resulting map is continuous
by the gluing lemma, and shows that Γ ≃S1.
It remains to show that the path class [f1] is a generator of π1(Γ, v). Let
z be any vertex in C. The path a that starts at z and traverses each edge
of C in order at constant speed is clearly path homotopic to the standard
generator of S1 ≈C (or its inverse). Choosing any path b from z to v
yields an isomorphism Φb : π1(Γ, z) →π1(Γ, v) as in Theorem 7.11. Thus a
generator of π1(Γ, v) is Φb[a] = [b−1 · a · b]. Since b−1 · a · b is a path that
goes from v to w1, traverses ⟨w1, w′
1⟩, and returns to v, it is homotopic to
f1. (Remember that the path class of f1 is independent of which paths we
choose from v to w1 and w′
1.) This completes the proof in the case n = 1.
Now suppose n > 1, and assume that the theorem is true whenever
there are fewer than n edges in the complement of a maximal tree. We
will apply the Seifert–Van Kampen theorem in the following way. For each
i = 1, . . . , n, choose a point xi in the interior of the edge ⟨wi, w′
i⟩(Figure
10.3(b)). Let U = Γ∖{x1, . . . , xn−1} and V = Γ∖{xn}. Both U and V are
open in Γ, and just as before it is easy to construct deformation retractions
to show that U ∩V ≃T, U ≃T ∪⟨wn, w′
n⟩, and V ≃Γ ∖Int⟨wn, w′
n⟩. By
the inductive hypothesis, π1(V, v) = ⟨[f1], . . . , [fn−1]⟩and π1(U, v) = ⟨[fn]⟩.
Since U ∩V is simply connected, Corollary 10.3 shows that π1(Γ, v) is
isomorphic to the free product of these two free groups, which is the free
group on [f1], . . . , [fn] as claimed.

Applications
217
Second Special Case: One Simply Connected Set
The other special case of the Seifert–Van Kampen theorem we will use is
that in which one of the open sets, say U, is simply connected. In that case,
diagram (10.1) simpliﬁes considerably. Because the top group π1(U, q) is
trivial, both the homomorphisms i∗and k∗are trivial, and the free product
in the middle reduces to π1(V, q). Moreover, the homomorphism Φ is just
equal to l∗, and the map F is just equal to j∗, so the entire diagram collapses
to
π1(U ∩V, q)
j∗
−→π1(V, q)
l∗
−→π1(X, q).
The conclusion of the theorem reduces immediately to the following corol-
lary.
Corollary 10.8. Assume the hypotheses of the Seifert–Van Kampen the-
orem, and suppose in addition that U is simply connected. Then inclusion
l: V 	→X induces an isomorphism
π1(X, q) ∼= π1(V, q)

j∗π1(U ∩V, q),
where j∗π1(U ∩V, q) is the normal closure of j∗π1(U ∩V, q) in π1(V, q). If
the fundamental groups of V and U ∩V have ﬁnite presentations
π1(V, q) ∼= ⟨β1, . . . , βn | σ1, . . . , σs⟩,
π1(U ∩V, q) ∼= ⟨γ1, . . . , γp | τ1, . . . , τt⟩,
then π1(X, q) has the presentation
π1(X, q) ∼= ⟨β1, . . . , βn | σ1, . . . , σs, v1, . . . , vp⟩,
where va is an expression for j∗γa ∈π1(V, q) in terms of {β1, . . . , βm}.
We will give two applications of this corollary. The ﬁrst is to give another
proof that Sn is simply connected when n ≥2.
Another proof of Theorem 8.7.
As in the previous proof, we take Sn =
U ∪V with U = Sn ∖{N} and V = Sn ∖{S}, both of which are simply
connected because they are homeomorphic to Rn. Moreover, U ∩V is path
connected because it is homeomorphic to Rn ∖{0}. Corollary 10.8 to the
Seifert–Van Kampen theorem says that for any point q ∈U ∩V , π1(Sn, q)
is isomorphic to a quotient of π1(V, q) by a certain subgroup. But this
quotient is trivial because π1(V, q) is itself trivial.
The next proposition will allow us to compute the fundamental groups
of all compact surfaces. Now it will become clear why we chose similar
notations for surface presentations and group presentations.

218
10. The Seifert–Van Kampen Theorem
ai
ai
0
q
v0
g
P
c
M
π
ai
v
q
g
FIGURE 10.4. Proof of Proposition 10.9.
Proposition 10.9. Let M be a 2-manifold determined by a polygonal
surface presentation ⟨a1, . . . , an | W⟩with one face, in which all ver-
tices are identiﬁed to a single point. Then π1(M) has the presentation
⟨a1, . . . , an | W⟩.
Proof. First we set up some notation (see Figure 10.4). Let P be a regular
polygon in the plane with 2n sides, centered at the origin, and let π: P →
M denote the quotient map determined by the given presentation. Set
U = Int P and V = P ∖{0}, and let U = π(U), V = π(V ) ⊂M. Since
U and V are saturated open sets, the restrictions of π to U and V are
quotient maps, and their images U, V are open in M. Moreover, U, V , and
U ∩V are all path connected because they are images of path connected
sets in P. Choose a base point q ∈U ∩V lying on the line segment from 0
to the vertex v0 on the y-axis, and let q = π(q) ∈U ∩V . Finally, let v ∈M
denote the single vertex (the image of all the vertices of P). In general, we
will use symbols without tildes to denote sets, points, or paths in P, and
the same symbols with tildes to denote their images in M.
The restriction of π to U is a one-to-one quotient map and therefore a
homeomorphism. Since U is convex, it is simply connected, and therefore
U is simply connected as well. Thus we will be able to use Corollary 10.2
once we ﬁnd presentations for the fundamental groups of V and U ∩V . The
details are a bit involved, but the basic idea is just that V is homotopy

Applications
219
equivalent to a bouquet of circles, so π1(V , q) is a free group on the n
generators determined by a1, . . . , an; and U ∩V is homotopy equivalent to
a circle, so j∗π1(U ∩V , q) is the inﬁnite cyclic group generated by the word
W in these generators.
Consider ﬁrst V . Observe that its preimage V ⊂P is homotopy equiva-
lent to ∂P, by the straight-line homotopy H that moves each point radially
outward to the boundary. The map π × Id: P × I →M × I is a quotient
map by Lemma 4.35 (or just by the closed map lemma). Since V × I is a
saturated open subset of P × I, the restriction of π × Id to it is a quotient
map. Because π ◦H respects the identiﬁcations of this quotient map, it
descends to a strong deformation retraction H of V onto π(∂P):
V × I
V .
-
H
V × I
V
-
H
?
π × Id
?
π
On ∂P, π identiﬁes the edges in pairs and identiﬁes all the vertices to
a point, so π(∂P) is homeomorphic to a bouquet of n circles, one for each
label ai. (To verify this, you can, for example, construct quotient maps from
2n disjoint intervals to S1 ∨· · · ∨S1 and to π(∂P), both of which make the
same identiﬁcations.) Therefore, π1(V , q) is a free group on n generators.
We need to identify these generators explicitly. For each i, let ai denote
a path in M that traverses the single edge labeled ai (the image under π of
two edges of P) in the indicated direction. Since all vertices of P project to
v, ai is a loop based at v. From Example 10.6, π1(S1 ∨· · · ∨S1, v) is freely
generated by [a1], . . . , [an]. The isomorphism π1(S1 ∨· · ·∨S1, v) →π1(V , v)
induced by inclusion takes these generators to themselves, thought of as
loops in V , so π1(V , v) is the free group ⟨[a1], . . . , [an]⟩.
We are really interested in the base point q, not v. Let g be the radial
straight-line path from q to v0, let g = π ◦g, a path from q to v, and
consider the loops a′
i based at q, deﬁned by
a′
i = g · ai · g−1.
These are just the images of the loops ai under the isomorphism from
π1(V , v) to π1(V , q) provided by the path g−1 as in Theorem 7.11, so we
conclude that π1(V , q) is the free group ⟨[a′
1], . . . , [a′
n]⟩.
Next we turn to U ∩V . Since π is one-to-one on U ∩V , U ∩V is home-
omorphic to U ∩V = Int P ∖{0}. Let C be the circle centered at 0 and
passing through q, and let C be its image in M. (We may assume that q
is chosen close enough to 0 that C is contained in the interior of P.) A de-
formation retraction of Int P ∖{0} onto C is easily constructed by moving
each point radially inward or outward toward C at constant speed. Thus

220
10. The Seifert–Van Kampen Theorem
π1(U ∩V , q) is inﬁnite cyclic, generated by the path class of any loop that
goes around C once. Let c be a loop that goes counterclockwise around C,
and let c = π ◦c, a loop in U ∩V based at q. Then π1(U ∩V , q) is the
inﬁnite cyclic group ⟨[c]⟩.
Now Corollary 10.8 to the Seifert–Van Kampen theorem says that
π1(M, q) ∼= ⟨[a′
1], . . . , [a′
n] | b⟩, where b is an expression for j∗[c] ∈π1(V , q)
in terms of the generators [a′
1], . . . , [a′
n]. So to complete the proof, we need
only ﬁnd such an expression.
The key observation is that g−1·c·g, a loop based at v, is path homotopic
in V to the loop 
W obtained from W by replacing each ai by ai. To see this,
we ﬁrst work upstairs in P: Let H be the strong deformation retraction of
V onto ∂P, and set
F(s, t) = H(g−1 · c · g(s), t).
The map F is a homotopy from g−1 · c· g to a path that goes once around
∂P in the clockwise direction, and it descends to a homotopy in V from
g−1 · c · g to 
W. It follows that
c ∼g · g−1 · c · g · g−1 ∼g · 
W · g−1 ∼
W ′,
where 
W ′ is obtained from W by replacing each ai by a′
i; the last equiva-
lence follows by inserting g−1 · g between each pair of symbols in the word

W.
Thus we have shown that the generator [c] of π1(U ∩V , q) is mapped by
inclusion to [
W ′] ∈π1(V , q), where [
W ′] is obtained from W by replacing
each ai by [a′
i]. By Corollary 10.2, therefore, π1(M, q) has the presentation
⟨[a′
1], . . . , [a′
n] | [
W ′]⟩; relabeling the symbols ai instead of [a′
i] yields the
presentation given in the statement of the proposition.
Example 10.10. Using the results of this section, we have the following
presentations for the fundamental groups of compact, connected surfaces:
(a) π1(S2) ∼= ⟨⟩(the trivial group).
(b) π1(T2 # · · · # T2)
∼= ⟨β1, γ1, . . . , βn, γn | β1γ1β−1
1 γ−1
1
· · · βnγnβ−1
n γ−1
n
= 1⟩.
(c) π1(P2 # · · · # P2) ∼= ⟨β1, . . . , βn | β2
1 · · · β2
n = 1⟩.
In particular, for the torus this gives π1(T2) ∼= ⟨β, γ | βγ = γβ⟩, which
agrees with the result we derived earlier. In the case of the projective plane,
this gives π1(P2) ∼= ⟨β | β2 = 1⟩∼= Z/⟨2⟩.

Proof of the Theorem
221
Proof of the Theorem
In this section we prove the Seifert–Van Kampen theorem (Theorem 10.1)
and its corollary about ﬁnite presentations (Corollary 10.2).
Proof of Theorem 10.1. Because we will be considering paths and their ho-
motopy classes in various spaces, for this proof we will reﬁne our notation
to specify explicitly where homotopies are assumed to lie. If a and b are
paths in X that happen to lie in one of the subsets U, V , or U ∩V , we will
use the notation
a ∼
U b,
a ∼
V b,
a ∼
U∩V b,
a ∼
X b
to indicate that a is path homotopic to b in U, V , U ∩V , or X, respectively.
We write [a]U for the path class of a in π1(U, q), and similarly for the other
sets. Thus, for example, if a is a loop in U ∩V , the homomorphisms induced
by the inclusions i: U ∩V 	→U and k: U 	→X can be written
i∗([a]U∩V ) = [a]U,
k∗([a]U) = [a]X.
We will have to consider two diﬀerent types of products: path class mul-
tiplication within any one fundamental group, and word multiplication in
the free product group. As usual, we will denote path and path class mul-
tiplication by a dot, as in
[a]U · [b]U = [a · b]U.
To emphasize the distinction between the two products, we denote multi-
plication in the free product group by an asterisk, so, for example,
[a]U ∗[b]U ∗[c]V = [a · b]U ∗[c]V ∈π1(U, q) ∗π1(V, q).
Then the map Φ: π1(U, q) ∗π1(V, q) →π1(X, q) can be written
Φ([a1]U ∗[a2]V ∗· · · ∗[am−1]U ∗[am]V )
= k∗[a1]U · l∗[a2]V · · · · · k∗[am−1]U · l∗[am]V
= [a1]X · [a2]X · · · · · [am−1]X · [am]X
= [a1 · a2 · · · · · am−1 · am]X.
(10.3)
Let N denote the normal closure of F(π1(U ∩V, q)) in π1(U, q)∗π1(V, q).
We need to prove three things: (1) Φ is surjective; (2) N ⊂Ker Φ; and (3)
Ker Φ ⊂N.

222
10. The Seifert–Van Kampen Theorem
a
 i+1
n

a
 i
n

a
 i−1
n

ai
ai+1
hi+1
hi
hi−1
U
V
q
a
FIGURE 10.5. Proof that Φ is surjective.
Step 1: Φ is surjective. Let a: I →X be any loop in X based at q. By
the Lebesgue number lemma, we can choose n large enough that a maps
each subinterval [(i −1)/n, i/n] either into U or into V . (This is why it is
important that the sets U and V be open.) Letting ai denote the restriction
of a to [(i −1)/n, i/n] (reparametrized so that its parameter interval is I),
the path class of a in X factors as
[a]X = [a1 · · · · · an]X.
The problem with this factorization is that the paths ai are not loops in
general. To remedy this, for each i = 1, . . . , n −1, choose a path hi from
q to a(i/n) (Figure 10.5). If a(i/n) ∈U ∩V , choose hi to lie entirely in
U ∩V ; otherwise, choose it to lie in whichever set U or V contains a(i/n).
(This is why the sets U, V , and U ∩V must all be path connected.) Then
set ai = hi−1 · ai · h−1
i
(where we let h0 and hn be the constant loop cq),
so that each ai is a loop based at q and lying entirely in either U or V . It
follows easily that a also factors as
[a]X = [a1 · · · · · an]X.
Now consider the element
γ = [a1]U ∗[a2]V ∗· · · ∗[an]V ∈π1(U, q) ∗π1(V, q),

Proof of the Theorem
223
where we choose either U or V for each ai depending on which set contains
its image. Then as in (10.3) above,
Φ(γ) = [a1 · · · · · an]X = [a]X.
This proves that Φ is surjective.
Step 2: N ⊂Ker Φ. If we can show that F(π1(U ∩V, q)) is contained in
Ker Φ, then its normal closure N will be contained in Ker Φ as well because
Ker Φ is normal.
Let [a]U∩V ∈π1(U ∩V, q) be arbitrary. Then
Φ ◦F([a]U∩V ) = Φ((i∗[a]U∩V )−1 ∗(j∗[a]U∩V ))
= Φ([a−1]U ∗[a]V )
= [a−1 · a]X
= 1.
Step 3: Ker Φ ⊂N. This is the crux of the proof. Let
γ = [a1]U ∗[a2]V ∗· · · ∗[ak]V ∈π1(U, q) ∗π1(V, q)
be an arbitrary element of the free product, and suppose that Φ(γ) = 1.
Using (10.3) again, this means that
[a1 · · · · · ak]X = 1,
which is equivalent to
a1 · · · · · ak ∼
X cq.
We need to show that γ ∈N.
Let H : I ×I →X be the path homotopy from a1· · · · ·ak to cq in X. By
the Lebesgue number lemma again, we can subdivide I × I into squares of
side 1/n so that H maps each square Sij = [(i−1)/n, i/n]×[(j −1)/n, j/n]
either into U or into V .
Let vij denote the image under H of the vertex (i/n, j/n); and let aij
denote the restriction of H to the horizontal line segment [(i −1)/n, i/n] ×
{j/n}, and bij the restriction to the vertical segment {i/n}×[(j−1)/n, j/n],
both suitably reparametrized on I (see Figure 10.6).
The restriction of H to the bottom edge of I ×I, where t = 0, is equal to
the path product a1 · · · · · ak. By taking n to be a suﬃciently large power
of 2, we can ensure that the endpoints of the paths ai in this product are

224
10. The Seifert–Van Kampen Theorem
q
H
ai,j−1
aij
bi−1,j
bij
a1n
. . .
. . .
. . .
. . .
ain
ann
Sij
a10
ai0
an0
FIGURE 10.6. Proof that Ker Φ ⊂N.
of the form i/n, so the path obtained by restricting H to the bottom edge
of the square can also be written
H0 ∼a1 · · · · · ak ∼(a10 · · · · · ap0) · · · · · (ar0 · · · · · an0).
In the free product, this means that
γ = [a10 · · · · · ap0]U ∗· · · ∗[ar0 · · · · · an0]V .
We would like to factor this in the free product as [a10]U ∗[a20]U ∗· · · and
so forth. But these paths are not loops based at q, so we cannot yet use this
relation directly. This is easy to ﬁx as in Step 1: For each i and j, choose a
path hij from q to vij, staying in U ∩V if vij ∈U ∩V , and otherwise in U
or V ; if vij happens to be the base point q, choose hij to be the constant
loop cq. Then deﬁne loops
aij = hi−1,j · aij · h−1
ij ,
bij = hi,j−1 · bij · h−1
ij ,
(10.4)
each of which lies entirely in U or V . Then γ can be factored as
γ = [a10]U ∗[a20]U ∗· · · ∗[an0]V .
(10.5)
The main idea of the proof is this: We will show that modulo N, the
expression (10.5) for γ can be replaced by the corresponding expression
obtained by restricting H to the top edge of the ﬁrst row of squares:
γ ≡[a11]U ∗· · · ∗[an1]V
(mod N).

Proof of the Theorem
225
Repeating this argument, we move up to the next row, and so forth by
induction, until we obtain
γ ≡[a1n]U ∗· · · ∗[ann]V
(mod N).
But the entire top edge of I × I is mapped by H to the point q, so each
ain is equal to the constant loop cq, and this last product is equal to the
identity. This shows that γ ∈N, completing the proof.
Thus we need to prove the following inductive step: Assuming by induc-
tion that
γ ≡[a1,j−1]U ∗· · · ∗[an,j−1]V
(mod N),
(10.6)
we need to show that γ is equivalent modulo N to the same expression
with j −1 replaced by j.
First we observe the following simple fact: Suppose a is a loop in U ∩V .
Then [a]U and [a]V are in the same coset in the free product modulo N,
because
[a]V ∗N = [a]U ∗([a]−1
U ∗[a]V ) ∗N = [a]U ∗F([a]U∩V ) ∗N = [a]U ∗N.
Since N is normal, this also implies x ∗[a]U ∗y ∗N = x ∗[a]U ∗N ∗y =
x ∗[a]V ∗N ∗y = x ∗[a]V ∗y ∗N for any x, y in the free product. Thus,
as long as we are computing modulo N and a is a loop in U ∩V , we can
freely interchange [a]U with [a]V wherever either appears.
Consider a typical square Sij, and suppose for deﬁniteness that H maps
Sij into V . The boundary of Sij, traversed clockwise starting at the lower
left corner, is mapped to the path (bi−1,j · aij) · (b−1
ij · a−1
i,j−1). By Lemma
7.12, this means that
ai,j−1 ∼
V bi−1,j · aij · b−1
ij .
(10.7)
Using the deﬁnition (10.4) of the loops aij and bij, (10.7) yields
ai,j−1 = hi−1,j−1 · ai,j−1 · h−1
i,j−1
∼
V hi−1,j−1 · bi−1,j · aij · b−1
ij · h−1
i,j−1
∼
V
bi−1,j · aij · b−1
ij ,
(10.8)
since the interior factors of hij and hi−1,j and their inverses cancel out.
Now start with the expression (10.6) for γ. For each factor [ai,j−1]U,
check whether the square Sij above it is mapped into U or V . If it is

226
10. The Seifert–Van Kampen Theorem
mapped into V , then ai,j−1 must map into U ∩V , and we can replace this
factor by [ai,j−1]V modulo N. Correct each factor whose square maps into
U similarly.
By (10.8), we can replace each such factor [ai,j−1]V by [bi−1,j]V ∗[aij]V ∗
[bij]−1
V , and similarly for the factors in U. Thus
γ ≡[b0,j]U ∗[a1j]U ∗[b1j]−1
U ∗· · · ∗[bn−1,j]V ∗[anj]V ∗[bnj]−1
V
(mod N)
≡[a1j]U ∗· · · ∗[anj]V
(mod N).
Here we have used the facts that the interior bij factors all cancel each
other out (replacing [bij]U by [bij]V when necessary), and b0j and bnj are
both equal to the constant loop cq. This completes the inductive step and
thus the proof.
Proof of Corollary 10.2. To simplify the notation, let A and B denote the
free groups ⟨α1, . . . , αm⟩and ⟨β1, . . . , βn⟩, respectively, and write R =
{ρ1, . . . , ρr}, S = {σ1, . . . , σs}, and G = {u−1
1 v1, . . . , u−1
p vp}, all considered
as subsets of A ∗B. (Note that the relators τi in U ∩V do not enter into
either the statement of the corollary or its proof.) Then π1(U, q) ∼= A/ R
and π1(V, q) ∼= B/ S by hypothesis. We will consider these isomorphisms
as identiﬁcations, so Φ is a map from (A/ R) ∗(B/ S) to π1(X, q). Let
π: A ∗B →(A/ R) ∗(B/ S) denote the homomorphism induced by the
projections A →A/ R and B →B/ S as in Problem 9-4.
The Seifert–Van Kampen theorem says that Φ is surjective and has kernel
equal to F(π1(U ∩V, q)), which clearly contains π(G) by our choice of
the set G. In fact, it is equal to π(G): To see this, we need only verify
that π(G) includes all of F(π1(U ∩V, q)), which is to say every element of
the form (i∗γ)−1(j∗γ) for γ ∈π1(U ∩V, q). Consider the quotient group

(A/ R)∗(B/ S)

/π(G). By deﬁnition of G, each element of the form u−1
i vi
projects to 1 in this quotient, which is to say that ui and vi project to
the same element. Given any γ ∈π1(U ∩V, q), express it as a word in the
generators γ1, . . . , γp; then i∗γ and j∗γ will be expressed by the same word,
but with γi replaced by ui in one case and vi in the other. This shows that
i∗γ and j∗γ project to the same element in the quotient, which means that
(i∗γ)−1(j∗γ) ∈π(G).
The composition
A ∗B
π→(A/ R) ∗(B/ S)
Φ→π1(X, q)
is also surjective. The corollary will follow from the ﬁrst isomorphism the-
orem (Theorem A.13) once we show that its kernel is exactly R ∪S ∪G.
Clearly, R and S are contained in Ker(Φ◦π). Also, π(G) ⊂F(π1(U ∩V, q)
by our choice of G, and thus π(G) ⊂Ker Φ, which means that G ∈Ker(Φ◦

Distinguishing Manifolds
227
π) as well. Therefore, the kernel of Φ ◦π is a normal subgroup containing
R ∪S ∪G, so R ∪S ∪G ⊂Ker(Φ ◦π).
To prove the reverse inclusion, suppose w ∈A ∗B is a word such that
Φ ◦π(w) = 1. This means that π(w) ∈Ker Φ = π(G) = π(G). (The last
equality follows because the homomorphic image of a normal subgroup
under a surjective map is normal; see Exercise A.25 in the Appendix.) In
other words, π(w) = π(g), where g is some element of G. This just means
that wg−1 ∈Ker π, which by Problem 9-4 is equal to R ∗S (thought of as
a subgroup of A ∗B). This can be rewritten as w = hg for some h ∈R ∗S,
g ∈G. Since clearly R ∪S ∪G must contain R ∗S and G, this means that
w ∈R ∪S ∪G, and the proof is complete.
Distinguishing Manifolds
Now we are ﬁnally in a position to ﬁll the gap in our classiﬁcation of surfaces
by showing that the diﬀerent surfaces on our list are actually topologically
distinct. We will do so by showing that their fundamental groups are not
isomorphic. Even this is not completely straightforward, because it involves
solving the isomorphism problem for certain ﬁnitely presented groups. But
in this case we can reduce the problem to a much simpler problem involving
abelian groups.
Given a group G, the commutator subgroup of G, denoted by [G, G], is the
normal closure of the set of all elements of the form αβα−1β−1 for α, β ∈G.
Clearly, the quotient group G/[G, G] is always abelian, and the commutator
subgroup is trivial if and only if G itself is abelian. This quotient group
is denoted by Ab(G) and called the abelianization of G. It is clear that
isomorphic groups have isomorphic abelianizations. Ab(G) is the “largest”
abelian quotient of G, or equivalently the largest abelian homomorphic
image of G, in the sense that any other homomorphism into an abelian
group factors through the abelianization, as the following characteristic
property shows.
Theorem 10.11 (Characteristic Property of Abelianizations).
For any abelian group H and any homomorphism ϕ: G →H, there exists
a unique homomorphism ϕ: Ab(G) →H such that the following diagram
commutes:
G
H
-
ϕ
Ab(G).
?
π
ϕ



Exercise 10.1.
Prove Theorem 10.11.
It is relatively easy to compute the abelianizations of our surface groups.

228
10. The Seifert–Van Kampen Theorem
Theorem 10.12. The fundamental groups of compact surfaces have the
following abelianizations:
Ab(π1(S2)) = {1};
Ab(π1(T2 # · · · # T2

 !
"
n
)) ∼= Z2n;
Ab(π1(P2 # · · · # P2

 !
"
n
)) ∼= Zn−1 × Z/⟨2⟩.
Proof. The case of the sphere is obvious, so consider ﬁrst an orientable
surface of genus n, and let
G = ⟨β1, γ1, . . . , βn, γn | β1γ1β−1
1 γ−1
1
· · · βnγnβ−1
n γ−1
n ⟩
be the fundamental group. Deﬁne a map ϕ: Ab(G) →Z2n as follows. Let
ei = (0, . . . , 1, . . . , 0) ∈Z2n (1 in the ith place), and set
ϕ(βi) = ei,
ϕ(γi) = ei+n.
Thought of as a map from the free group ⟨{βi, γi}⟩into Z2n, this sends
the element β1γ1β−1
1 γ−1
1
· · · βnγnβ−1
n γ−1
n
to (0, . . . , 0), so it descends to
a homomorphism from G to Z2n. By the characteristic property of the
abelianization, it also descends to a homomorphism (still denoted by ϕ)
from Ab(G) to Z2n.
To go back the other way, deﬁne ψ: Z2n →Ab(G) by
ψ(ei) =

[βi],
1 ≤i ≤n,
[γi−n],
n + 1 ≤i ≤2n,
where the brackets on the right-hand side denote the equivalence class in
Ab(G), and extend it to be a homomorphism. It is easy to check that ϕ
and ψ are inverses of each other.
Next consider the connected sum of projective planes, and let H =
⟨β1, . . . , βn | β2
1 · · · β2
n⟩. Write f for the nontrivial element of Z/⟨2⟩, and
deﬁne ϕ: Ab(H) →Zn−1 × Z/⟨2⟩by
ϕ(βi) =

ei,
1 ≤i ≤n −1;
f −en−1 −· · · −e1,
i = n.
As before, ϕ(β2
1 · · · β2
n) = (0, . . . , 0) by direct computation (noting that
f+f = 0), so ϕ descends to Ab(H). The homomorphism ψ: Zn−1×Z/⟨2⟩→
Ab(H) deﬁned by
ψ(ei) = [βi],
ψ(f) = [β1 · · · βn]
is easily veriﬁed to be an inverse for ϕ.

Distinguishing Manifolds
229
Corollary 10.13. Any compact, connected surface is homeomorphic to ex-
actly one of the surfaces S2, T2 # · · · # T2, or P2 # · · · # P2.
Proof. First note that the sphere cannot be homeomorphic to a connected
sum of tori or projective planes, because one has trivial fundamental group
and the other does not. Next, if M is a connected sum of projective planes,
then Ab(π1(M)) contains a nontrivial torsion element, whereas the abelian-
ized fundamental groups of connected sums of tori are torsion free. There-
fore, no connected sum of projective planes can be homeomorphic to a
connected sum of tori. If M is a connected sum of n tori, then its abelian-
ized fundamental group has rank 2n. Thus the genus (i.e., the number of
tori in the connected sum) can be recovered from the fundamental group,
so the genus of an orientable surface is a topological invariant. Similarly,
a connected sum of n projective planes has abelianized fundamental group
of rank n −1, so once again the genus is a topological invariant.
Now we can tie up the loose ends regarding the combinatorial invariants
we discussed at the end of Chapter 6. Recall that a compact 2-manifold is
said to be orientable if it admits an oriented presentation.
Corollary 10.14. A connected sum of projective planes is not orientable.
Proof. By the argument in Chapter 6, if a manifold admits an oriented
presentation, then it is homeomorphic to a sphere or a connected sum of
tori. The preceding corollary showed that a connected sum of projective
planes is not homeomorphic to any of these surfaces.
Corollary 10.15. The Euler characteristic of a surface presentation is a
topological invariant.
Proof. Suppose P and Q are polygonal surface presentations such that
|P| ≈|Q|. Each of these presentations can be transformed into one of the
standard ones by elementary transformations, and since the surfaces rep-
resented by diﬀerent standard presentations are not homeomorphic, both
presentations must reduce to the same standard one. Since the Euler char-
acteristic of a presentation is unchanged by elementary transformations,
the two presentations must have had the same Euler characteristic to be-
gin with.
Because of this corollary, we can deﬁne the Euler characteristic of a
compact surface M, denoted by χ(M), to be the Euler characteristic of
any presentation of that surface.

230
10. The Seifert–Van Kampen Theorem
Problems
10-1. Compute the fundamental group of each of the following spaces. (To
“compute” a fundamental group means to give a presentation of the
group together with a speciﬁc loop representing each generator.)
(a) A closed disk with two points removed.
(b) The projective plane with two points removed.
(c) The connected sum of n tori with one point removed.
(d) The connected sum of n tori with two points removed.
10-2. Give a purely algebraic proof that the groups ⟨α, β | αβαβ−1⟩and
⟨ρ, γ | ρ2γ2⟩are isomorphic. [Hint: Look at the Klein bottle for inspi-
ration.]
10-3. Let n be an integer greater than 2. Construct a polygonal presentation
whose geometric realization has a fundamental group that is cyclic of
order n.
10-4. Suppose M and N are compact 2-manifolds. Show that any two con-
nected sums of M and N are homeomorphic.
10-5. Compute the fundamental group of the complement of the three co-
ordinate axes in R3. [Hint: This space is homotopy equivalent to the
2-sphere with six points removed.]
10-6. If M is a connected manifold of dimension at least 3 and q ∈M,
show that π1(M ∖{q}) ∼= π1(M).
10-7. Let M and N be connected n-manifolds, n ≥3. Prove that the fun-
damental group of M # N is isomorphic to π1(M) ∗π1(N).
10-8. Let P be the polyhedron of a ﬁnite simplicial complex K, and assume
that P is connected. Show that the fundamental group of P has a
presentation with the same number of generators as π1(K(1)) and
one relation for each 2-simplex in K. [Hint: First treat the case of
a 2-dimensional complex by induction on the number of 2-simplices.
Then use a similar argument to show that inclusion K(j) 	→K(j+1)
induces a fundamental group isomorphism for j ≥2.]
10-9. Let Γ be a ﬁnite connected graph. The Euler characteristic of Γ is
χ(Γ) = V −E, where V is the number of vertices and E is the number
of edges. Show that the fundamental group of Γ is a free group on
1−χ(Γ) generators. Conclude that χ(Γ) is a homotopy invariant, i.e.,
that homotopy equivalent graphs have the same Euler characteristic.
[Hint: First show by induction on the number of edges that the Euler
characteristic of a ﬁnite tree is 1.]

Problems
231
0
2
4
2n −2
. . .
FIGURE 10.7. The space Xn of Problem 10-10.
10-10. Let Xn be the union of n circles of radius 1 centered at the points
{0, 2, 4, . . . , 2n −2} in C, which are pairwise tangent to each other
along the x-axis (Figure 10.7). (Note that X2 is homeomorphic to
the ﬁgure eight space.) Prove that π1(Xn, 1) is a free group on n
generators, and describe explicit loops representing the generators.
10-11. Show that a connected, compact surface M is nonorientable if and
only if it contains a subset homeomorphic to the M¨obius band.
10-12. Let X ⊂R3 be the union of the unit 2-sphere with the line segment
{(0, 0, z) : −1 ≤z ≤1}. Compute π1(X, N), where N = (0, 0, 1) is
the north pole, giving explicit generator(s).
10-13. Show that abelianization deﬁnes a functor from GROUP to AB. (You
have to decide what the induced homomorphisms are.)
10-14. Given a group G, show that Ab(G) is the unique group that satisﬁes
the characteristic property expressed in Theorem 10.11.
10-15. If G1 and G2 are groups, show that Ab(G1 ∗G2) ∼= Ab(G1)⊕Ab(G2).
Conclude as a corollary that the abelianization of a free group on n
generators is free abelian of rank n.

11
Covering Spaces
So far we have developed two general techniques for computing fundamental
groups. The ﬁrst is homotopy equivalence, which can often be used to show
that one space has the same fundamental group as a simpler one. This was
used in Chapter 7, for example, to show that every contractible space is
simply connected, and that the fundamental group of the punctured plane
is inﬁnite cyclic. The second is the Seifert–Van Kampen theorem, which
was used in Chapter 10 to compute the fundamental groups of spheres and
compact surfaces.
The only other fundamental group we have computed is that of the circle,
for which we used a technique that at ﬁrst glance might seem to be rather
ad hoc. The strategy for computing π1(S1, 1) in Chapter 8 was to use the
properties of the exponential quotient map ε to show that any loop based
at 1 in the circle lifts to a path in R that ends at an integer; this integer
is called the winding number of the loop, and diﬀerent loops are path
homotopic if and only if they have the same winding number. Another way
to express this result is that lifting provides a one-to-one correspondence
between the ﬁber of ε over 1 and the fundamental group of the circle.
The main ingredients in the proof were the three “lifting properties”
of the circle: the path lifting property (Lemma 8.3), the homotopy lifting
property (Lemma 8.4), and the unique lifting property (Lemma 8.2). These,
in turn, followed from the basic fact that every point in the circle has an
evenly covered neighborhood.
In this chapter we introduce a far-reaching generalization of these ideas,
and show how the same techniques can be applied to a broad class of
topological spaces. This brings us to the last major subject in the course:

234
11. Covering Spaces

X
X
p
q
FIGURE 11.1. An evenly covered neighborhood of q.
covering spaces and covering maps. A covering map is a particular type
of quotient map that has many of the same properties as the exponential
quotient map. A careful study of covering maps will enable us to compute
and analyze many more fundamental groups.
Deﬁnitions and Basic Properties
Let 
X and X be topological spaces, and let p: 
X →X be a continuous
map. A subset U ⊂X is said to be evenly covered by p if U is connected
and open, and each component of p−1(U) is an open set that is mapped
homeomorphically onto U by p (Figure 11.1). We usually visualize p−1(U)
as a “stack of pancakes” that are projected down onto U by p. It is easy
to see that any connected open subset of an evenly covered set is evenly
covered.
A covering map is a continuous surjective map p: 
X →X such that 
X
is path connected and locally path connected, and every point q ∈X has
an evenly covered neighborhood. If p: 
X →X is a covering map, we call

X a covering space of X, and X the base of the covering.
(Some authors deﬁne covering spaces more generally, omitting the re-
quirement that 
X be locally path connected or path connected, or even
sometimes omitting any connectivity requirement at all. In that case vari-

Deﬁnitions and Basic Properties
235
ous connectivity hypotheses have to be added to the theorems below. We
have chosen to include these hypotheses in the deﬁnition of covering maps,
because most of the interesting results require them, such as the lifting
criterion, the covering group structure theorem, and the classiﬁcation of
covering spaces, and this frees us from having to remember which connec-
tivity hypotheses are necessary for which theorems. In any case, connected
manifolds and most interesting spaces built from them will always satisfy
the hypotheses.)
Example 11.1. The exponential quotient map ε: R →S1 given by ε(x) =
e2πix is a covering map; this is the content of Lemma 8.5.
Example 11.2. The nth power map pn : S1 →S1 given by pn(z) = zn is
also a covering map. For any z0 ∈S1, the set U = S1 ∖{−z0} has preimage
equal to {z ∈S1 : zn ̸= −z0}, which has n components, each of which is an
open arc mapped homeomorphically by pn onto U.
Example 11.3. Deﬁne E : Rn →Tn by
E(x1, . . . , xn) = (ε(x1), . . . , ε(xn)),
where ε is the exponential quotient map of Example 11.1. Since a product
of covering maps is a covering map (Problem 11-2), E is a covering map.
Example 11.4. Deﬁne a map π: Sn →Pn (n ≥1) by sending each point
x in the sphere to the line through the origin and x, thought of as a point
in Pn. Then π is a covering map (Problem 11-1), and the ﬁber over each
point of Pn is a pair of antipodal points {x, −x}.
Exercise 11.1.
Let Xn be the union of n circles in C as described in
Problem 10-10. Deﬁne a map p: X3 →X2 by letting A, B, and C denote
the circles centered at 0, 2, and 4, respectively (see Figure 11.2), and deﬁning
p(z) =
⎧
⎪
⎨
⎪
⎩
z,
z ∈A;
2 −(z −2)2,
z ∈B;
4 −z,
z ∈C.
(In words, p is the identity on A, wraps B twice around itself, and reﬂects
C onto A). Show that p is a covering map.
Lemma 11.5 (Elementary Properties of Covering Maps).
Every
covering map is a local homeomorphism, an open map, and a quotient map.
A one-to-one covering map is a homeomorphism.
Exercise 11.2.
Prove Lemma 11.5.
It is important to realize that a surjective local homeomorphism may not
be a covering map, as the next example shows.

236
11. Covering Spaces
A
B
C
FIGURE 11.2. Two views of the map of Exercise 11.1.
Example 11.6. Let 
X be the interval (0, 2) ⊂R, and deﬁne f : 
X →S1 by
f(x) = e2πix (Figure 11.3). Then f is a local homeomorphism (because it
is the restriction of the covering map ε), and is clearly surjective. However,
f is not a covering map, as is shown in the following exercise.
Exercise 11.3.
Prove that the map f in the preceding example is not
a covering map by showing that the point 1 ∈S1 has no evenly covered
neighborhood.
Recall from Chapter 8 that a local section of a continuous map is a
continuous right inverse deﬁned on some open subset.
Lemma 11.7 (Existence of local sections). Let p: 
X →X be a cov-
ering map. Given any evenly covered open set U ⊂X, any q ∈U, and
any q0 in the ﬁber over q, there exists a local section σ: U →
X such that
σ(q) = q0.
Proof. Let U0 be the component of p−1(U) containing q0. Since the restric-
tion of p to U0 is a homeomorphism, we can just take σ = (p|U0)−1.
Proposition 11.8. For any covering map p: 
X →X, the cardinality of
the ﬁbers p−1(q) is the same for all ﬁbers.
Proof. If U is any evenly covered open set in X, each component of p−1(U)
contains exactly one point of each ﬁber. Thus, for any q, q′ ∈U, there are
one-to-one correspondences
p−1(q) ↔{components of p−1(U)} ↔p−1(q′),
which shows that the number of components is constant on U. It follows
that the set of points q′ ∈X such that p−1(q′) has the same cardinality as
p−1(q) is open.

Deﬁnitions and Basic Properties
237

X
f
FIGURE 11.3. A surjective local homeomorphism that is not a covering
map.
Now choose any point q ∈X, and let A be the set of points in X whose
ﬁbers have cardinality equal to that of p−1(q). Then A is open by the above
argument, and X ∖A is open because it is a union of open sets (one for
each cardinality not equal to that of p−1(q)). Since X is connected and A
is not empty, A must be equal to X.
If p: 
X →X is a covering map, the cardinality of any ﬁber is called
the number of sheets of the covering. For example, the nth power map of
Example 11.2 is an n-sheeted covering; the map π: Sn →Pn of Example
11.4 is a two-sheeted covering; and the exponential quotient map ε: R →S1
has countably many sheets.
Lifting Properties
The key technical tools for working with covering spaces are the following
three lifting properties, which are straightforward generalizations of the
ones we proved for the circle in Chapter 8. In fact, the proofs for the circle
apply almost verbatim to these more general propositions. We sketch the
proofs in streamlined form here; if you remember the arguments given in
Chapter 8, you can safely skip these proofs.
If p: 
X →X is a covering map and ϕ: B →X is any continuous map,
a lift of ϕ is a continuous map ϕ: B →
X such that p ◦ϕ = ϕ:
B
X.
-
ϕ
ϕ




X
?
p

238
11. Covering Spaces
Proposition 11.9 (Unique Lifting Property).
Let p: 
X →X be a
covering map. Suppose B is connected, ϕ: B →X is continuous, and
ϕ1, ϕ2 : B →
X are lifts of ϕ that agree at some point of B. Then ϕ1 ≡ϕ2.
Proof. As in the proof of Lemma 8.2, it suﬃces to show that S = {b ∈B :
ϕ1(b) = ϕ2(b)} is open and closed in B.
For any b ∈S, let U ⊂X be an evenly covered neighborhood of ϕ(b),
and let Uα be the component of p−1(U) containing ϕ1(b) = ϕ2(b). On the
neighborhood V = ϕ−1
1 (Uα) ∩ϕ−1
2 (Uα) of b, ϕ = p ◦ϕ1 = p ◦ϕ2. Since p is
injective on Uα, this means ϕ1 = ϕ2 on V , so S is open.
On the other hand, for b ̸∈S, if U is an evenly covered neighborhood of
ϕ(b), there are disjoint components U1, U2 of p−1(U) containing ϕ1(b), ϕ2(b)
such that p is a homeomorphism from each Ui to U. Letting V = ϕ−1
1 (U1)∩
ϕ−1
2 (U2), we conclude that ϕ1 ̸= ϕ2 on V , which shows that S is closed.
Proposition 11.10 (Path Lifting Property). Let p: 
X →X be a cov-
ering map. Suppose f : I →X is any path, and q0 ∈
X is any point in the
ﬁber of p over f(0). Then there exists a unique lift f : I →
X of f such
that f(0) = q0.
Proof. By the Lebesgue number lemma, n can be chosen large enough
that p maps each subinterval [k/n, (k + 1)/n] into an evenly covered open
subset of X. Starting with f(0) = q0, f is deﬁned inductively by choosing
an evenly covered neighborhood Uk containing f[k/n, (k + 1)/n], a local
section σk : Uk →
X such that σk(f(k/n)) = f(k/n), and setting f = σk ◦f
on [k/n, (k + 1)/n]. Because p ◦f = (p ◦σk) ◦f = f, this is indeed a lift,
and it is unique by the unique lifting property.
Proposition 11.11 ([[Homotopy]] Lifting Property).
Let p: 
X →X
be a covering map. Suppose f0, f1 : I →X are path homotopic, and
f0, f1 : I →
X are lifts of f0 and f1 such that f0(0) = f1(0). Then f0 ∼f1.
Proof. If H : f0 ∼f1 is a path homotopy, by the Lebesgue number lemma
we can choose n large enough that H maps each square of side 1/n into
an evenly covered open set. Labeling the squares Sij = [i/n, (i + 1)/n] ×
[j/n, (j + 1)/n], we deﬁne a lift H of H square by square along the bottom
row, then along the next row, and so on by induction as in the proof of
Lemma 8.3. On each square Sij, set H = σ ◦H, for an appropriate local
section σ chosen so that the new deﬁnition of H matches the previous one
at the corner point (i/n, j/n). On a line segment where two such deﬁnitions
overlap, both the old and new deﬁnitions are lifts of the path obtained by
restricting H to that segment, starting at the same point. Thus they are
equal by the unique lifting property.
On the left-hand and right-hand edges of I × I, where s = 0 or s = 1, H
is a lift of the constant loop and therefore constant. The restriction H0 to

Covering Maps and the Fundamental Group
239
the bottom edge where t = 0 is a lift of f0 starting at f0(0), and therefore is
equal to f0; and similarly H1 = f1. Thus H is the required path homotopy
between f0 and f1.
The next result is an immediate corollary of the homotopy lifting prop-
erty.
Corollary 11.12 (The Monodromy Theorem).
Let p: 
X →X be a
covering map. Suppose f0 and f1 are path homotopic paths in X, and f0,
f1 are lifts of them starting at the same point. Then f0(1) = f1(1).
Covering Maps and the Fundamental Group
Our next theorem characterizes the fundamental group homomorphism in-
duced by a covering map.
Theorem 11.13 (Injectivity Theorem).
Let p: 
X →X be a covering
map. For any point q ∈
X, the induced homomorphism p∗: π1( 
X, q) →
π1(X, p(q)) is injective.
Proof. Suppose [f] ∈π1( 
X, q) is in the kernel of p∗. This means that
p∗[f] = [cq], where q = p(q), or in other words, p ◦f ∼cq in X. By
the homotopy lifting property, therefore, any lifts of p ◦f and cq that start
at the same point must be path homotopic in 
X. Now, f is a lift of p ◦f
starting at q, and the constant loop cq is a lift of cq starting at the same
point; therefore, f ∼cq in 
X, which means that [f] = 1.
This theorem shows that the fundamental group of a covering space can
be identiﬁed with a subgroup of the fundamental group of the base. We
call this the subgroup induced by the covering.
Example 11.14. Let p: X3 →X2 be the covering map of Exercise 11.1,
and choose 1 as base point in both X3 and X2. To compute the subgroup
induced by p, we need to compute the action of p on the generators of
π1(X3, 1). Let a, b, c be loops that go once counterclockwise around each
circle A, B, and C, starting at 1, 1, and 3, respectively; and let b1 and b2
be the lower and upper halves of b, so b1 is a path from 1 to 3, b2 is a path
from 3 to 1, and b ∼b1· b2. Using the result of Problem 10-10, π1(X3, 1) is
the free group on [a], [b], and [b1 · c · b−1
1 ], and π1(X2, 1) is the free group
on [a] and [b]. The images of these generators under p∗are [a], [b]2, and
[b] · [a]−1 · [b]−1, so the subgroup induced by p is the subgroup of ⟨[a], [b]⟩
generated by these three elements.
As our ﬁrst signiﬁcant application of the theory we give a general solution
to the lifting problem for covering maps: This is the problem of deciding,
given a continuous map ϕ: Y →X, whether ϕ admits a lift ϕ to a covering

240
11. Covering Spaces
space 
X of X. The following theorem reduces this topological problem to
an algebraic problem.
Theorem 11.15 (Lifting Criterion). Suppose p: 
X →X is a covering
map. Let Y be a connected and locally path connected space, and let ϕ: Y →
X be a continuous map. Given any points y0 ∈Y and q0 ∈
X such that
p(q0) = ϕ(y0), ϕ has a lift ϕ: Y →
X satisfying ϕ(y0) = q0 if and only if
the subgroup ϕ∗π1(Y, y0) of π1(X, ϕ(y0)) is contained in p∗π1( 
X, q0).
Proof. The necessity of the algebraic condition is easy to prove (and, in
fact, does not require any connectivity assumptions about Y ). If ϕ satis-
ﬁes the conditions in the statement of the theorem, the following diagram
commutes:
π1(Y, y0)
π1(X, ϕ(y0)).
-
ϕ∗
ϕ∗






π1( 
X, q0)
?
p∗
Therefore, ϕ∗π1(Y, y0) = p∗ϕ∗π1(Y, y0) ⊂p∗π1( 
X, q0).
To prove the converse, we will “lift ϕ along paths” using the path lifting
property. If ϕ does exist, it will have the following property: For any point
y ∈Y and any path f from y0 to y, ϕ◦f is a lift of ϕ◦f starting at q0, and
ϕ(y) is equal to the terminal point of this path. We use this observation to
deﬁne ϕ: Namely, for any y ∈Y , choose a path f from y0 to y, let 
ϕ ◦f be
the (unique) lift of the path ϕ ◦f to a path in 
X starting at q0, and set
ϕ(y) = 
ϕ ◦f(1).
We need to show two things: (1) ϕ is well-deﬁned, independently of the
choice of the path f; and (2) ϕ is continuous. Then it is immediate from
the deﬁnition that p ◦ϕ(y) = p ◦
ϕ ◦f(1) = ϕ ◦f(1) = ϕ(y), so ϕ is a lift
of ϕ.
Claim 1: ϕ is well-deﬁned. Suppose f and f ′ are two paths from y0 to
y (Figure 11.4). Then f ′ · f −1 is a loop based at y0, so
ϕ∗[f ′ · f −1] ∈ϕ∗π1(Y, y0) ⊂p∗π1( 
X, q0).
This means that [ϕ ◦(f ′ · f −1)] = [p ◦g] for some loop g in 
X based at q0.
Thus we have the following path homotopy in X:
p ◦g ∼ϕ ◦(f ′ · f −1) = (ϕ ◦f ′) · (ϕ ◦f)−1,

Covering Maps and the Fundamental Group
241
Y
y0
y
f
f ′
ϕ
ϕ
p
ϕ(y0)
ϕ ◦f
ϕ(y)
p ◦g
ϕ ◦f ′
X

X
g
q0

ϕ ◦f
ϕ(y)

ϕ ◦f ′
FIGURE 11.4. Proof that ϕ is well-deﬁned.
which implies
(p ◦g) · (ϕ ◦f) ∼(ϕ ◦f ′).
By the monodromy theorem, the lifts of these two paths starting at q0 have
the same terminal points. Since the lift of p ◦g is g, which starts and ends
at q0, this implies

ϕ ◦f ′(1) = g · 
ϕ ◦f(1) = 
ϕ ◦f(1),
so ϕ is well-deﬁned.
Claim 2: ϕ is continuous. Before proving this, we will show that ϕ has
one important property of a continuous map: It takes path connected sets
to path connected sets. Let V ⊂Y be path connected, and y1, y2 ∈V be
arbitrary. There is a path f in Y from y0 to y1, and a path g in V from
y1 to y2 (Figure 11.5); by deﬁnition, ϕ maps the path f · g to the lift of
(ϕ ◦f)· (ϕ ◦g). In particular, the lift of ϕ ◦g is a path from ϕ(y1) to ϕ(y2)
that is contained in ϕ(V ). This proves that ϕ(V ) is path connected.
To prove that ϕ is continuous, it suﬃces to show that each point in Y
has a neighborhood on which ϕ is continuous. Let y ∈Y be arbitrary, let
U be an evenly covered neighborhood of ϕ(y), and let U be the component
of p−1(U) containing ϕ(y) (Figure 11.6). If V is the path component of
ϕ−1(U) containing y, the argument above shows that ϕ(V ) is a connected

242
11. Covering Spaces
Y
y0
y1
y2
f
g
V
ϕ

X
q0
ϕ(V )
ϕ(y1)
ϕ(y2)
FIGURE 11.5. Proof that ϕ takes path connected sets to path connected
sets.
subset of p−1(U), and must therefore be contained in U. Since Y is locally
path connected, V is open and thus is a neighborhood of y. Let σ: U →U
be the local section of p taking ϕ(y) to ϕ(y), so p ◦σ is the identity on U.
The following equation holds on V :
p ◦ϕ = ϕ = p ◦σ ◦ϕ.
Both ϕ and σ ◦ϕ map V into U, where p is injective, so this equation
implies ϕ = σ ◦ϕ on V , which is a composition of continuous maps.
The following corollaries are immediate.
Corollary 11.16. If p: 
X →X is a covering map and Y is a simply
connected and locally path connected space, every continuous map ϕ: Y →
X has a lift to 
X. Given any point y0 ∈Y , the lift can be chosen to take
y0 to any point in the ﬁber over ϕ(y0).
Corollary 11.17. Suppose p: 
X →X is a covering map and 
X is simply
connected. For any connected and locally path connected space Y , a con-
tinuous map ϕ: Y →X has a lift to 
X if and only if ϕ∗is the trivial
homomorphism for any base point y0 ∈Y . If this is the case, then the lift
can be chosen to take y0 to any point in the ﬁber over ϕ(y0).
Example 11.18. Consider the n-sheeted covering of the circle given by
the nth power map pn : S1 →S1. It is easy to check that the subgroup of
π1(S1, 1) induced by pn is the cyclic subgroup generated by [α]n. Thus, for

Covering Maps and the Fundamental Group
243
y
V
Y
ϕ
ϕ
σ
p
ϕ(y)
U

X
ϕ(y)
U
X
FIGURE 11.6. Proof that ϕ is continuous.
any integer m, there is a continuous map f making the diagram
S1
S1
-
pm
f




S1
?
pn
commute if and only if m = nk for some integer k. If this is the case, the
lift sending 1 to 1 is obviously f = pk.
Dependence on Base Points
It is important to remember that in general, the subgroup induced by a
covering depends not only on the covering but also on the choice of base
point q ∈
X. As the next theorem shows, the subgroup may change when
we change base point, but it can change only in a very limited way.
Theorem 11.19 (Conjugacy Theorem).
Let p: 
X →X be a covering
map. For any q ∈X, as q varies over the ﬁber p−1(q), the set of subgroups
p∗π1( 
X, q) ⊂π1(X, q) is exactly one conjugacy class.
Proof. First we will show that given any q, q ′ ∈p−1(q), the subgroups
p∗π1( 
X, q) and p∗π1( 
X, q ′) are conjugate. Let g be a path in 
X from q to

244
11. Covering Spaces
q
q ′
g
q
g

X
X
f
p
p ◦f
FIGURE 11.7. Proof of the conjugacy theorem.
q ′, and let g = p ◦g, which is a loop in X based at q (Figure 11.7). We
have four maps
π1(X, q)
π1(X, q),
-
Φg
π1( 
X, q)
π1( 
X, q ′)
-
Φg
?
p∗
?
p∗
(11.1)
where Φg[f] = [g−1] · [f] · [g], and Φg is deﬁned similarly. This diagram
commutes, because
p∗Φg[f] = p∗[g−1 · f · g]
= [p ◦(g−1 · f · g)]
= [(p ◦g−1) · (p ◦f) · (p ◦g)]
= [g−1] · p∗[f] · [g]
= Φgp∗[f].
This means that Φg maps the subgroup p∗π1( 
X, q) into p∗π1( 
X, q ′), so
we can replace the bottom two groups in (11.1) by the image groups under

Covering Maps and the Fundamental Group
245
p∗to obtain
p∗π1( 
X, q)
p∗π1( 
X, q ′).
-
Φg
π1( 
X, q)
π1( 
X, q ′)
-
Φg
?
p∗
?
p∗
(11.2)
Now, in this diagram, both vertical maps are isomorphisms, and the top
map is an isomorphism by Theorem 7.11. This means that the bottom map
Φg is an isomorphism as well. But Φg is exactly the map that sends any
subgroup onto its conjugate by [g]−1, so this shows that p∗π1( 
X, q) and
p∗π1( 
X, q ′) are conjugate subgroups.
Conversely, let q ∈p−1(q), and suppose H is any subgroup of π1(X, q)
conjugate to p∗π1( 
X, q). This means that there is some element [g] ∈
π1(X, q) such that H = Φg(p∗π1( 
X, q)). If we let g be the lift of g start-
ing at q, and q ′ = g(1), the above construction shows that p∗π1( 
X, q ′) =
Φg(p∗π1( 
X, q)) = H.
There is an important special case in which the subgroup p∗π1( 
X, q) does
not depend on the choice of base point. We say that the covering p: 
X →X
is normal if p∗π1( 
X, q) is a normal subgroup of π1(X, p(q)) for each q ∈
X.
This means, in particular, that for any ﬁxed q ∈X the subgroup p∗π1( 
X, q)
is independent of the choice of base point q in the ﬁber over q, because the
only subgroup conjugate to a normal subgroup is itself. In fact, as the next
lemma shows, as long as the induced subgroup is normal for one choice of
q ∈
X, it is normal for all of them.
Lemma 11.20. Let p: 
X →X be a covering map, and suppose the sub-
group induced by p is normal for one point q ∈
X. Then p is normal.
Proof. Let q, q ′ be two points of 
X, and let q = p(q), q′ = p(q ′). Let g be
a path from q to q ′, and set g = p ◦g, which is a path from q to q′. If we
replace q by q′ in the bottom right corner of diagram (11.1), the diagram
still commutes, and the top and bottom rows are still isomorphisms. It
follows from the commutativity of the diagram that Φg takes p∗(π1( 
X, q))
to p∗(π1( 
X, q ′)). Since an isomorphism takes normal subgroups to normal
subgroups, the result follows.
Next we show that there is a natural right action of the fundamental
group of the base on the ﬁber of any covering space. Recall from Chapter
3 that given an action of a group Γ on a set F, the orbit of a point x ∈F
is the set of all images of x under elements of the group (for a right action,
this is the set {x·γ : γ ∈Γ}), and the action is said to be transitive if each
orbit is all of F.

246
11. Covering Spaces
g(1)
f(1)
q
g
f
p
f
q
g
FIGURE 11.8. Proof that the fundamental group acts on the ﬁber.
Theorem 11.21 (Action of the Fundamental Group on a Fiber).
Suppose p: 
X →X is a covering map and q ∈X. There is a transitive
right action of π1(X, q) on the ﬁber p−1(q), given by q · [f] = f(1), where
f is the lift of f starting at q ∈p−1(q).
Proof. If q is any point in the ﬁber over q, any path f starting at q has a
lift to a path f starting at q by the path lifting property. The monodromy
theorem guarantees that the endpoint f(1) depends only on the path class
of f; therefore, q · [f] is well-deﬁned.
To see that this is a group action, we need to check two things:
(a) q · [cq] = q;
(b) (q · [f]) · [g] = q · ([f] · [g]).
For (a), just observe that the constant loop cq is the unique lift of cq starting
at q, and therefore q · [cq] = cq(1) = q. To prove the composition property
(b), suppose f and g are two loops based at q. Let f be the lift of f starting
at q, so that q · [f] = f(1). Now, if g is the lift of g starting at f(1), then
by deﬁnition, (q · [f])· [g] = g(1) (Figure 11.8). On the other hand, f · g is

The Covering Group
247
clearly the lift of f · g starting at q. This means that
q · ([f] · [g]) = q · [f · g]
= ( f · g)(1)
= g(1).
Finally, to prove that the action is transitive, just note that any two
points q, q ′ in the ﬁber over q are joined by a path f because 
X is path
connected. Setting f = p ◦f, it is immediate that f is the lift of f starting
at q, and therefore q · [f] = q ′.
Corollary 11.22. Let p: 
X →X be a covering map, and suppose 
X is
simply connected. The number of sheets of the covering is equal to the car-
dinality of the fundamental group of X.
Proof. Choose a base point q ∈X and a point q in the ﬁber over q, and
consider the map π1(X, q) →p−1(q) given by [f] 
→q · [f]. It is surjective
because the action of the fundamental group is transitive. To show that it
is injective, suppose that q · [f] = q · [g]. This means that the lifts f and
g starting at q end at the same point. Since 
X is simply connected, f ∼g,
and therefore [f] = p∗[ f] = p∗[g] = [g].
Example 11.23. Since π: Sn →Pn is a two-sheeted covering and Sn
is simply connected, Corollary 11.22 shows that π1(Pn) is a two-element
group, which must therefore be isomorphic to Z/⟨2⟩.
Corollary 11.24. If X is a simply connected space, any covering map
p: 
X →X is a homeomorphism.
Proof. The injectivity theorem shows that 
X is also simply connected.
Thus Corollary 11.22 shows that the cardinality of the ﬁbers is 1, so p is a
one-to-one covering map and therefore a homeomorphism.
The Covering Group
In this section we introduce the group of covering transformations of a
covering space, and explore its relation to the fundamental groups of the
base and the covering space.

248
11. Covering Spaces
Suppose p: 
X →X is a covering map. A homeomorphism ϕ: 
X →
X is
called a covering transformation if p ◦ϕ = p:

X

X
-
ϕ
X.
p@@
R
p


	
Covering transformations are also variously known as deck transformations
or automorphisms of the covering.
Let Cp( 
X) denote the set of all covering transformations of 
X with re-
spect to p. It is easy to verify that the composition of two covering transfor-
mations, the inverse of a covering transformation, and the identity map of

X are all covering transformations; thus Cp( 
X) is a group, called the cov-
ering group or the automorphism group of the covering. It acts on 
X (on
the left) in a natural way, and the deﬁnition of covering transformations
implies that each orbit is a subset of a single ﬁber.
Example 11.25. For the covering ε: R →S1, the integral translations
x 
→x + k for k ∈Z are easily seen to be covering transformations. More
generally, for any integers (k1, . . . , kn), the translation (x1, . . . , xn) 
→(x1+
k1, . . . , xn +kn) is a covering transformation of E : Rn →Tn. We will prove
below that these are all of them.
Example 11.26. If π: Sn →Pn is the covering map of Example 11.4,
then the antipodal map A(x) = −x is a covering transformation. We will
see shortly that Cπ(Pn) is the two-element group {Id, A}.
Proposition 11.27 (Properties of the Covering Group).
Let
p: 
X →X be a covering map.
(a) If two covering transformations agree at one point, they are identical.
(b) The covering group acts freely and continuously on 
X: If ϕ(q) = q
for some q ∈
X, then ϕ = Id 
X.
(c) For any q ∈X, each covering transformation permutes the points of
the ﬁber p−1(q).
(d) For any evenly covered open set U ⊂X, each covering transformation
permutes the components of p−1(U).
Proof. Note that a covering transformation ϕ is, in particular, a lift of p:

X
X.
-
p
ϕ





X
?
p

The Covering Group
249
Thus (a) follows from the unique lifting property. The covering group
acts continuously because each covering transformation is continuous by
deﬁnition; the fact that it acts freely follows from (a) by comparing ϕ
with the identity. Part (c) follows from the fact that if q ∈p−1(q), then
p(ϕ(q)) = p(q) = p, so ϕ takes the ﬁber over q to itself; since the same is
true of ϕ−1, ϕ acts as a permutation of the ﬁber. To prove (d), let U be an
evenly covered open set, and let Uα be a component of p−1(U). Since ϕ(Uα)
is a connected subset of p−1(U), it must be contained in a single compo-
nent; applying the same argument to ϕ−1 shows that ϕ(Uα) is exactly a
component.
Example 11.28. Consider again the covering group of ε: R →S1. Let
ϕ ∈Cε(R) be arbitrary. If we set n = ϕ(0), then both ϕ and the translation
x 
→x + n are covering transformations taking 0 to n, and are therefore
equal by Proposition 11.27(a). Thus the covering group of ε: R →S1 is
equal to Z acting on R by integral translations. By a similar argument,
the covering group of E : Rn →Tn is Zn acting by translations, and the
covering group of π: Sn →Pn is equal to the cyclic group of order 2
generated by the antipodal map.
Because of Proposition 11.27, the action of the covering group on 
X
is completely determined by the action on any ﬁber. However, unlike the
action of the fundamental group on a ﬁber that we deﬁned in Theorem
11.21, the action of the covering group on ﬁbers is not transitive in general.
It is often useful to have a criterion for deciding when two points in a ﬁber
are in the same orbit.
Proposition 11.29 (Orbit Criterion). Let p: 
X →X be a covering
map.
(a) If q, q ′ ∈
X are two points in the same ﬁber p−1(q), there exists
a covering transformation taking q to q ′ if and only if the induced
subgroups p∗π1( 
X, q) and p∗π1( 
X, q ′) are equal.
(b) Cp( 
X) acts transitively on each ﬁber if and only if p is a normal
covering.
Proof. If there exists ϕ such that ϕ(q) = q ′, then ϕ∗: π1( 
X, q) →π1( 
X, q ′)
is an isomorphism, so p∗π1( 
X, q) = p∗ϕ∗π1( 
X, q) = p∗π1( 
X, q ′). Con-
versely, if the two subgroups are equal, then the lifting criterion yields a
lift p: 
X →
X satisfying p ◦p = p and p(q) = q ′. Reversing the roles of
q and q ′, we get a lift p ′ satisfying p ′(q ′) = q. To show that p and p ′
are inverses of each other, note that p ′ ◦p and Id 
X are lifts of p taking q
to itself, and thus are equal by the unique lifting property, and similarly
p ◦p ′ = Id 
X. Therefore, p is the required covering transformation.
Now suppose p is normal. This means that for any q, q ′ in the same ﬁber,
p∗π1( 
X, q) = p∗π1( 
X, q ′), so by part (a) there is a covering transformation

250
11. Covering Spaces
taking q to q ′. Conversely, if Cp( 
X) acts transitively on the ﬁber p−1(q),
the groups p∗π1( 
X, q) coincide for all q ∈p−1(q), which is to say that p is
normal.
The next theorem is the central result concerning the relationship be-
tween covering spaces and fundamental groups. It gives an explicit formula
for the covering group in terms of the fundamental groups of the covering
space and the base, and can be used to compute the fundamental groups
of certain spaces from properties of their coverings. For normal coverings,
the theorem simply says that the covering group is isomorphic to the quo-
tient of the fundamental group of the base by the subgroup induced by the
covering. The statement for general groups is somewhat more complicated,
and involves the following algebraic notion: If G is a group and H ⊂G
is a subgroup, the normalizer of H in G, denoted by N(H), is the set of
all elements γ ∈G such that γ−1Hγ = H. The normalizer N(H) is easily
seen to be a subgroup of G; it is in fact the largest subgroup in which H is
normal.
Theorem 11.30 (Covering Group Structure Theorem).
Suppose
p: 
X →X is a covering map and q ∈
X. The covering group Cp( 
X) is
isomorphic to the quotient
N(p∗π1( 
X, q))
p∗π1( 
X, q)
.
The isomorphism is induced by the map α: N(p∗π1( 
X, q)) →Cp( 
X) that
sends [f] to the unique covering transformation ϕ taking q to q · [f].
Before we give the proof of this important theorem, which is rather tech-
nical, let us derive some immediate consequences to illustrate its utility.
Corollary 11.31 (Normal Case).
If p: 
X →X is a normal covering,
q ∈
X, and q = p(q), then Cp( 
X) ∼= π1(X, q)/p∗π1( 
X, q).
Corollary 11.32 (Simply Connected Case).
If p: 
X →X is a cov-
ering map and 
X is simply connected, then for any q ∈
X the map α of
Theorem 11.30 is an isomorphism from π1(X, q) to Cp( 
X), where q = p(q).
Example 11.33. Since the covering group of ε: R →S1 is inﬁnite cyclic
and R is simply connected, Corollary 11.32 yields another proof that the
fundamental group of the circle is inﬁnite cyclic. In fact, if you look back
carefully at the proof in Chapter 8, you will see that this is really the same
proof we gave there, decorated with some fancier terminology.
Example 11.34. Because the covering group of π: Sn →Pn is the two-
element group {Id, A}, Corollary 11.32 gives another proof that π1(Pn) ∼=
Z/⟨2⟩.

The Covering Group
251
Proof of the covering group structure theorem.
Write H = p∗π1( 
X, q) ⊂
π1(X, q). We will show that α: N(H) →Cp( 
X) is a surjective homomor-
phism whose kernel is H; by the ﬁrst isomorphism theorem, this proves the
result.
Let [g] ∈N(H) be arbitrary, and let q ′ = q · [g] as deﬁned in Theorem
11.21. Recall that q ′ is the terminal point of the lift g of g starting at q.
The key claim is that there exists a covering transformation ϕ ∈Cp( 
X)
such that ϕ(q) = q ′.
By the orbit criterion, to prove the claim it suﬃces to show that
p∗π1( 
X, q ′) = p∗π1( 
X, q). Let Φg : π1( 
X, q) →π1( 
X, q ′) be the isomor-
phism determined by the path g as in Theorem 7.11. From the commu-
tative diagram (11.2) in the proof of the conjugacy theorem, we conclude
that
p∗π1( 
X, q ′) = p∗Φgπ1( 
X, q)
= Φgp∗π1( 
X, q)
= [g]−1 · H · [g] = H
= p∗π1( 
X, q).
Thus there exists a covering transformation ϕ such that ϕ(q) = q ′; it is
necessarily unique by Proposition 11.27(a). Deﬁne α[g] = ϕ.
To show that α is a homomorphism, let [g1], [g2] ∈N(H), and write
α[gi] = ϕi, so that ϕi is a covering transformation satisfying ϕi(q) = gi(1).
Let ϕ12 = α[g1 · g2], so ϕ12(q) = 
g1 · g2(1). We need to show that ϕ12 =
ϕ1 ◦ϕ2. It suﬃces to show that these two covering transformations agree
at one point, so let us show that ϕ12(q) = ϕ1 ◦ϕ2(q), or equivalently

g1 · g2(1) = ϕ1(g2(1)).
Now, the lift g2 of g2 is a path in 
X starting at q. Because p ◦ϕ1 = p,
the image ϕ1 ◦g2 of g2 under ϕ1 is also a lift of g2, but this one starts at
ϕ1(q) = g1(1) (Figure 11.9). Thus the path product g1 · (ϕ1 ◦g2) makes
sense, and is the lift of g1 · g2 starting at q. In summary,
ϕ12(q) = 
g1 · g2(1)
= g1 · (ϕ1 ◦g2)(1)
= ϕ1 ◦g2(1)
= ϕ1(ϕ2(q)),
which was to be proved.
To show that α is surjective, let ϕ ∈Cp( 
X) be arbitrary, let q ′ = ϕ(q),
and let g be a path in 
X from q to q ′. Then g = p◦g is a loop in X. Moreover,

252
11. Covering Spaces
ϕ1

X
X
q
q
g1
g2
g1
g2
ϕ1 ◦g2
FIGURE 11.9. Proof that α is a homomorphism.
the orbit criterion shows that p∗π1( 
X, q) = p∗π1( 
X, q ′) because q and
q ′ are in the same orbit. On the other hand, from (11.2), p∗π1( 
X, q ′) =
Φgp∗π1( 
X, q). Thus Φgp∗π1( 
X, q) = p∗π1( 
X, q), which is to say that [g] ∈
N(H), and the construction above gives α[g] = ϕ.
Finally, we need to show that Ker α = H. Let [g] ∈N(H), let g be the lift
of g starting at q, and write ϕ = α[g]. Then ϕ is the identity transformation
if and only if ϕ(q) = g(1) = q, which means that g is a loop in 
X; so ϕ is
the identity if and only if [g] = [p ◦g] = p∗[g] for some [g] ∈π1( 
X, q), i.e.,
[g] ∈H.

Problems
253
Problems
11-1. Prove that for any n ≥1 the map π: Sn →Pn deﬁned in Example
11.4 is a covering map.
11-2. Show that a ﬁnite product of covering maps is a covering map: If
pi : 
Xi →Xi are covering maps for i = 1, . . . , n, then so is the map
p1 × · · · × pn : 
X1 × · · · × 
Xn →X1 × · · · × Xn.
11-3. Suppose p: 
X →X is a covering map.
(a) If 
X is an n-manifold and X is Hausdorﬀ, show that X is an
n-manifold.
(b) If X is an n-manifold, show that 
X is an n-manifold.
11-4. Suppose p: 
X →X is a covering map and X is a compact manifold.
Show that 
X is compact if and only if p is a ﬁnite-sheeted covering.
11-5. Let S be the following subset of C2:
S = {(z, w) : w2 = z, w ̸= 0}.
(It is the graph of the two-valued complex square root “function”
described in Chapter 1, with the origin removed.) Show that the
projection π1 : C2 →C onto the ﬁrst coordinate restricts to a two-
sheeted covering map p: S →C ∖{0}.
11-6. Show that there is a two-sheeted covering of the Klein bottle by the
torus.
11-7. Let 
M, M, and N be connected manifolds of dimension n and suppose
p: 
M →M is a k-sheeted covering map. Show that there exists a k-
sheeted covering of M # N by the connected sum of 
M with k copies
of N. [Hint: Choose the ball to be cut out of M to lie inside an evenly
covered neighborhood.]
11-8. Show that every nonorientable compact surface of genus n has a two-
sheeted covering by an orientable one of genus n−1. [Hint: Use Prob-
lem 11-7 and induction.]
11-9. Show that a proper local homeomorphism between connected, path
connected, and locally compact Hausdorﬀspaces is a covering map.
11-10. A continuous map f : S1 →S1 is said to be odd if f(−z) = −f(z) for
all z ∈S1, and even if f(z) = f(−z) for all z ∈S1. Show that every
odd map has odd degree, as follows.

254
11. Covering Spaces
(a) Let p2 : S1 →S1 be the two-sheeted covering map of Exam-
ple 11.2. If f is odd, show that there exists a continuous map
g: S1 →S1 such that deg f = deg g and the following diagram
commutes:
S1
S1.
-
g
S1
S1
-
f
?
p2
?
p2
(b) If deg f is even, show that g lifts to a map g: S1 →S1 such that
p2 ◦g = g.
(c) Show that g ◦p2 and f are both lifts of g ◦p2 that agree at
either (1, 0) or (−1, 0), so they are equal everywhere; derive a
contradiction.
11-11. Show that every even map f : S1 →S1 has even degree.
11-12. Prove the ham sandwich theorem: If two pieces of bread and one piece
of ham are placed arbitrarily in space, all three pieces can be cut in
half with a single slice of the knife. (If you do not like ham, you may
wish to substitute tofu.) More precisely, given three disjoint, bounded,
connected open subsets U1, U2, U3 ⊂R3, there exists a plane that
simultaneously bisects all three, in the sense that the plane divides
R3 into two half spaces H+ and H−such that for each i, Ui ∩H+
has the same volume as Ui ∩H−. [Hint: For any ω ∈S2, show that
there are unique real numbers (λ1, λ2, λ3) such that the plane through
λiω and orthogonal to ω bisects Ui. If there does not exist a plane
bisecting all three sets, deﬁne a map F : S2 →S1 by
F(ω) =
(λ1 −λ2) + i(λ2 −λ3)

(λ1 −λ2)2 + (λ2 −λ3)2 .
Show that F is continuous, and F ◦ιS1 contradicts the result of Prob-
lem 11-10, where ιS1 : S1 	→S2 is the inclusion map. You may assume
that there is a volume function Vol assigning a nonnegative real num-
ber to each open set in R3 and satisfying the following properties:
The volume of a set is unchanged by translations or rotations; the
volumes of balls, cylinders, and rectangular solids are given by the
usual formulas; and if U ⊂V then Vol(U) ≤Vol(V ).]
11-13. Let p: X3 →X2 be the covering map of Exercise 11.1.
(a) Determine the covering group Cp(X3).
(b) Determine whether p is a normal covering.

Problems
255
FIGURE 11.10. The covering map of Problem 11-14.
(c) For each of the following maps f : S1 →X2, determine whether
f has a lift to X3 taking 1 to 1.
i. f(z) = z.
ii. f(z) = z2.
iii. f(z) = 2 −z.
iv. f(z) = 2 −z2.
11-14. Let X4 be the union of four circles described in Problem 10-10, and let
p: X4 →X2 be the covering map indicated schematically in Figure
11.10. Answer the questions of Problem 11-13 for this covering.
11-15. Let E be the ﬁgure eight space of Example 7.21, and let X be the
union of the x-axis with inﬁnitely many unit circles centered at {2πk+
i : k ∈Z}. Let p: X →E be the map that sends each circle in X onto
the upper circle in E by translating in the x-direction and sends the
x-axis onto the lower circle by x 
→ieix −i. You may accept without
proof that p is a covering map.
(a) Identify the subgroup p∗π1(X, 0) of π1(E, 0) in terms of the gen-
erators for π1(E, 0).
(b) Compute the covering group Cp(X).
(c) Determine whether p is a normal covering.
11-16. This problem shows that the hypothesis that Y is locally path con-
nected is necessary for the lifting criterion (Theorem 11.15) to hold.
Let X be the topologist’s sine curve (Example 4.10), and let Y be
the union of X with a path in the plane from (1, sin 1) to (0, 1) that
intersects X only at those two points.
(a) Show that Y is simply connected.

256
11. Covering Spaces
(b) Show that there is a map f : Y →S1 that has no lift to R.
11-17. Suppose X is a compact polyhedron and p: 
X →X is a covering
map.
(a) Show that X and 
X admit triangulations such that p is induced
by a simplicial map. [Hint: Use barycentric subdivision.]
(b) Suppose K, K are ﬁnite complexes such that |K| = X, |K| = 
X,
and p is induced by a simplicial map from K to K. If p is an
n-sheeted covering, show that χ(K) = nχ(K).

12
Classiﬁcation of Coverings
The main thrust of the preceding chapter was to learn about fundamental
groups by studying covering maps. In this chapter we reverse the process
and explore what there is to be learned from the fundamental group about
the existence and uniqueness of covering spaces. The key idea is provided
by the conjugacy theorem of the preceding chapter: Each covering space of
X determines a conjugacy class of subgroups in the fundamental group of
X.
We begin with the uniqueness question. In the ﬁrst section of the chapter
we deﬁne isomorphisms of covering spaces, and show that two covering
spaces are isomorphic if and only if they induce the same conjugacy class
of subgroups.
Then we address the existence question. The ultimate goal is to show that
for a suﬃciently nice space X (any connected manifold, for example), every
conjugacy class of subgroups of π1(X, q) corresponds to some covering. This
is accomplished in several stages. First we show that X has a unique simply
connected covering space, called its “universal covering space.” Then we
show how to construct coverings as quotients of a given space by certain
group actions. The d´enouement is the last theorem of the chapter, which
puts together all the preceding results to give a complete classiﬁcation of all
coverings of X up to isomorphism: They are in one-to-one correspondence
with conjugacy classes of subgroups of the fundamental group of X. We
illustrate the theory by determining the universal covering spaces of all the
compact surfaces and classifying all the coverings of the torus.

258
12. Classiﬁcation of Coverings

X1

X2
X
ϕ
p1
p2
q1
f(1)
f
q2
g
q
f
q
FIGURE 12.1. Proof that a covering homomorphism is surjective.
Covering Homomorphisms
In this section we examine the question of how to tell when two covering
spaces are “the same.” As usual, we consider two coverings the same if they
are related by a suitable isomorphism. We begin by deﬁning some terms.
Let X be a space, and let p1 : 
X1 →X, p2 : 
X2 →X be two coverings of
X. A covering homomorphism from p1 to p2 is a continuous map ϕ: 
X1 →

X2 such that p2 ◦ϕ = p1:

X1

X2
-
ϕ
X.
p1@@
R
p2


	
A covering homomorphism that is also a homeomorphism is said to be an
isomorphism of coverings. It is easy to see that in this case the inverse map
is also a covering homomorphism. We say two coverings are isomorphic if
there is an isomorphism between them; this is an equivalence relation on
the set of coverings of X. Note that an isomorphism from a covering to
itself is just a covering transformation.
An interesting feature of covering homomorphisms is that they are them-
selves covering maps, as the following lemma shows.
Lemma 12.1. Let p1 : 
X1 →X and p2 : 
X2 →X be coverings of X, and
let ϕ be a covering homomorphism from p1 to p2. Then ϕ is a covering
map.
Proof. First we show that ϕ is surjective. Let q ∈
X2 be arbitrary. Choose
some q1 ∈
X1, and let q2 = ϕ(q1) ∈
X2, q = p1(q1) = p2(q2) ∈X (Figure
12.1). There is a path g in 
X2 from q2 to q. Let f = p2 ◦g, which is a

Covering Homomorphisms
259
ϕ
p1
p2
p−1
1 (V )
p−1
2 (V )
ϕ−1(U)
Uα
U
V
q
q
FIGURE 12.2. An evenly covered neighborhood of q.
path in X starting at q, and let f be the unique lift of f to a path in

X1 starting at q1. Consider now the path ϕ ◦f in 
X2. Its initial point is
ϕ ◦f(0) = ϕ(q1) = q2, and it satisﬁes p2 ◦ϕ ◦f = p1 ◦f = f, so ϕ ◦f is
the lift of f to 
X2 starting at q2. By the unique lifting property, this means
that ϕ ◦f = g, so
ϕ( f(1)) = g(1) = q,
which shows that ϕ is surjective.
To show that ϕ is a covering map, let q ∈
X2 be arbitrary; let q = p2(q) ∈
X; let U1, U2 ⊂X be neighborhoods of q that are evenly covered by p1
and p2, respectively; and let V be the component of U1 ∩U2 containing q.
Thus V is a neighborhood of q that is evenly covered by both p1 and p2.
Let U be the component of p−1
2 (V ) containing q. We need to show that
the components of ϕ−1(U) are mapped homeomorphically onto U by ϕ.
Consider the restrictions of p1 and ϕ to the “stack of pancakes” p−1
1 (V )
(Figure 12.2). Since U is both open and closed in p−1
2 (V ), it follows that
ϕ−1(U) is both open and closed in p−1
1 (V ), and is thus a union of compo-
nents. On any such component Uα, the following diagram commutes:
p2


	
U
ϕ
@@
R
Uα
V.
?
p1

260
12. Classiﬁcation of Coverings
Since p1 and p2 are homeomorphisms in this diagram, so is ϕ.
The key to determining when two covering spaces are isomorphic is to de-
cide when there are covering homomorphisms between them. This question
is answered by the following theorem.
Theorem 12.2 (Covering Homomorphism Criterion).
Suppose
p1 : 
X1 →X and p2 : 
X2 →X are two coverings of X, and q1 ∈
X1,
q2 ∈
X2 are base points such that p1(q1) = p2(q2) = q ∈X. There exists
a covering homomorphism from p1 to p2 taking q1 to q2 if and only if
p1∗π1( 
X1, q1) ⊂p2∗π1( 
X2, q2).
Proof. A covering homomorphism from p1 to p2 can also be viewed as a
lift of p1:

X1
X.
-
p1
ϕ




X2
?
p2
(12.1)
Thus both the necessity and the suﬃciency of the subgroup condition follow
from the lifting criterion (Theorem 11.15).
Example 12.3. Let pn : S1 →S1 be the nth power map deﬁned in Exam-
ple 11.2. The subgroup of π1(S1, 1) induced by pn is the cyclic subgroup
generated by [α]n (Example 11.18). By the covering homomorphism crite-
rion, there is a homomorphism from pm to pn if and only if m is divisible
by n; the homomorphism in that case is just pm/n.
Example 12.4. Consider the following two coverings of T2: E : R2 →T2 is
the covering of Example 11.3 (the product of two copies of ε: R →S1); and
p: S1 × R →T2 is given by p(z, y) = (z, ε(y)). Writing π1(T2) ∼= ⟨β⟩× ⟨γ⟩,
we see that E∗π1(R2) is trivial, while p∗π1(S1 × R) = ⟨β⟩× {1}. Therefore,
there exists a covering homomorphism from E to p. (Why do the base
points not matter?) It is easy to check that ϕ(x, y) = (ε(x), y) is such a
homomorphism.
The following theorem completely solves the uniqueness question for cov-
ering spaces up to isomorphism.
Theorem 12.5 (Covering [[Isomorphism]] Theorem).
Two coverings
p1 : 
X1 →X and p2 : 
X2 →X are isomorphic if and only if for some
q ∈X and base points q1 ∈p−1
1 (q) and q2 ∈p−1
2 (q), the induced subgroups
p1∗π1( 
X1, q1) and p2∗π1( 
X2, q2) are conjugate in π1(X, q). If this is the
case, these subgroups are conjugate for every such q, q1, and q2.

The Universal Covering Space
261
Proof. If there exists an isomorphism ϕ: 
X1 →
X2, choose q1 ∈
X1 ar-
bitrarily and set q2 = ϕ(q1). The covering homomorphism criterion ap-
plied to ϕ and ϕ−1 guarantees that the two subgroups p1∗π1( 
X1, q1) and
p2∗π1( 
X2, q2) are contained in each other, so they are equal. Thus by the
conjugacy theorem (Theorem 11.19), the subgroups associated with any
other choices of base points in the same ﬁbers are conjugate.
Conversely, suppose the two subgroups are conjugate for some choice of q,
q1, and q2. By the conjugacy theorem, we can change to a new base point
q ′
2 ∈
X2 such that p2∗π1( 
X2, q ′
2) = p1∗π1( 
X1, q1). Then by the covering
homomorphism criterion there exist homomorphisms ϕ from p1 to p2 and
ψ from p2 to p1, with ϕ(q1) = q ′
2 and ψ(q ′
2) = q1. The composite map
ψ ◦ϕ is a covering transformation of p1 that ﬁxes q1, so it is the identity.
Similarly, ϕ ◦ψ is the identity, so ϕ is the required isomorphism.
The Universal Covering Space
When the results of the preceding section are applied to simply connected
covering spaces, they yield some extremely useful results.
Proposition 12.6 (Properties of Simply Connected Coverings).
(a) Let p: 
X →X be a covering map with

X simply connected. If
p1 : 
X1 →X is any covering, there exists a covering map p: 
X →
X1
such that the following diagram commutes:
p1


	

X1
p
@@
R

X
X.
?
p
(b) Any two simply connected coverings of the same space are isomorphic.
Proof. Since the trivial subgroup is contained in every other subgroup,
part (a) follows from the covering homomorphism criterion and the fact
that every covering homomorphism is a covering map. Part (b) follows
immediately from the covering isomorphism theorem.
Part (a) of this proposition says that a simply connected covering space
covers every other covering space of X. Because of this, any covering of X
by a simply connected space 
X (which is unique by (b)) is called a universal
covering, and 
X is called the universal covering space of X.
Example 12.7. The universal covering space of the n-torus is Rn, because
we constructed a covering map E : Rn →Tn in Example 11.3. The universal
covering space of Pn is Sn, by the covering map π of Example 11.4.

262
12. Classiﬁcation of Coverings
As the next theorem shows, every “reasonable” space, including every
manifold, has a universal covering space. We say that a space X is lo-
cally simply connected if it admits a basis of simply connected open sets.
Clearly, a locally simply connected space is locally path connected, because
simply connected sets are path connected. Any manifold is locally simply
connected, because it has a basis of Euclidean balls.
Theorem 12.8 (Existence of the Universal Covering Space).
Ev-
ery connected and locally simply connected topological space (in particular,
every connected manifold) has a universal covering space.
Proof. To get an idea how to proceed, suppose for a moment that X does
have a universal covering p: 
X →X. The key fact is that once we choose
base points q0 ∈
X and q0 = p(q0) ∈X, the ﬁber p−1(q) over any q ∈X
is in one-to-one correspondence with path classes from q0 to q. To see why,
deﬁne a map E from the set of such path classes to p−1(q) by sending [f]
to the terminal point of the lift of f starting at q0. Since lifts of homotopic
paths have the same terminal point by the monodromy theorem, E is well-
deﬁned. E is surjective, because given any q in the ﬁber over q, there is a
path f from q0 to q, and then p ◦f is a path from q0 to q whose lift ends
at q. Injectivity of E follows from the fact that 
X is simply connected: If
f1, f2 are two paths from q0 to q whose lifts f1, f2 end at the same point,
then f1 and f2 are path homotopic, and therefore so are f1 = p ◦f1 and
f2 = p ◦f2.
Now let X be any space satisfying the hypotheses of the theorem, and
choose any base point q0 ∈X. Guided by the observation in the preceding
paragraph, we deﬁne 
X to be the set of path classes of paths in X starting
at q0, and deﬁne p: 
X →X by p[f] = f(1), which is well-deﬁned because
path homotopic paths have the same terminal point. We will prove that 
X
has the required properties in a series of steps.
Step 1: Topologize 
X. We deﬁne a topology on 
X by constructing a basis.
For any [f] ∈
X and any simply connected open set U ⊂X containing f(1),
deﬁne the set [f · U] ⊂
X by
[f · U] = {[f · a] : a is a path in U starting at f(1)}.
Let B denote the collection of all such sets [f · U]; we will show that B is a
basis. First, since X is locally simply connected, for any [f] ∈
X there exists
a simply connected open set U containing f(1), and clearly [f] ∈[f · U].
Thus the union of all the sets in B is 
X.
To check the intersection condition, suppose [h] ∈
X is in the intersection
of two basis sets [f ·U], [g·V ] ∈B. This means that h ∼f ·a ∼g·b, where
a is a path in U and b is a path in V (Figure 12.3). Let W be a simply
connected neighborhood of h(1) contained in U ∩V (such a neighborhood
exists because X has a basis of simply connected open sets). If [h·c] is any
element of [h· W], then [h· c] = [f · a· c] ∈[f · U] because a· c is a path in

The Universal Covering Space
263
U
V
W
X
q0
f
g
h
a
b
c
FIGURE 12.3. Proof that the collection of sets [f · U] is a basis.
U. Similarly, [h·c] = [g·b·c] ∈[g·V ]. Thus [h·W] is a basis set contained
in [f · U] ∩[g · V ], which proves that B is a basis. From now on, we endow

X with the topology generated by B.
Step 2: 
X is path connected. Let [f] ∈
X be arbitrary. We will show
that there is a path in 
X from q0 to [f], where q0 = [cq0].
For any 0 ≤t ≤1, deﬁne ft : I →X by
ft(s) = f(ts),
so ft is a path in X from q0 to f(t). Then deﬁne f : I →
X by
f(t) = [ft].
Clearly, f(0) = [f0] = q0, and f(1) = [f1] = [f]. So we need only show that
f is continuous; for this it suﬃces to show that the inverse image under f
of any basis open set [h · U] ⊂
X is open. Let t0 ∈I be a point such that
f(t0) ∈[h · U] (Figure 12.4). This means that ft0 ∼h · c for some path c
lying in U, and in particular that f(t0) = ft0(1) ∈U. For any 0 ≤t ≤1,
deﬁne a path ft0t by
ft0t(s) = f(t0 + s(t −t0)).
This path just follows f from f(t0) to f(t), so ft0 · ft0t is easily seen to be
path homotopic to ft.

264
12. Classiﬁcation of Coverings
f
h
c
q0
X
U
f(t)
f(t0)
FIGURE 12.4. Proof that 
X is path connected.
By continuity of f, there is some δ > 0 such that f(t0 −δ, t0 + δ) ⊂U.
If t ∈(t0 −δ, t0 + δ), then
ft ∼ft0 · ft0t ∼h · c · ft0t,
from which it follows that
f(t) = [ft] = [h · c · ft0t] ∈[h · U].
This shows that f −1[h·U] contains the set (t0−δ, t0+δ), so f is continuous.
Step 3: p is a covering map. Let U ⊂X be any simply connected open
set. We will show that U is evenly covered.
Choose any point q1 ∈U. We begin by showing that p−1(U) is the
disjoint union of the sets [f·U] as [f] varies over all the distinct path classes
from q0 to q1. It is obvious from the deﬁnition of p that p[f · U] ⊂U, so

[f][f · U] ⊂p−1(U). Conversely, if [g] ∈p−1(U), then g(1) = p[g] ∈U, so
there is a path b in U from g(1) to q1, and [g] = [g · b · b−1] ∈[(g · b) · U].
This proves that p−1(U) = 
[f][f · U].
This shows, in particular, that p is continuous: X has a basis of simply
connected open sets, and the inverse image under p of any such set is a
union of basis sets and therefore open. And p is clearly surjective, because
each q ∈X is equal to p[g] for any path g from q0 to q.
Next we show that p is a homeomorphism from each set [f · U] to U. It
is surjective because for each q ∈U there is a path a from f(1) to q in U,
so q = p[f ·a] ∈p[f ·U]. To see that it is injective, let [g], [g′] ∈[f ·U], and
suppose p[g] = p[g′], or in other words, g(1) = g′(1) (Figure 12.5). Then by
deﬁnition of [f · U], g ∼f · a and g′ ∼f · a′ for some paths a, a′ in U from
f(1) to g(1). Since U is simply connected, a ∼a′ and therefore [g] = [g′].
Finally, p is an open map because it takes basis open sets to open sets, and
therefore p: [f · U] →U is a homeomorphism.

The Universal Covering Space
265
q0
f
g
g′
a
a′
X
U
FIGURE 12.5. Proof that p is injective on [f · U].
Each set [f ·U] is open by deﬁnition, and each is path connected because
it is homeomorphic to the path connected set U. It follows that 
X is locally
path connected. To complete the proof that p is a covering map, we need
to show that for any two paths f and f ′ from q0 to q1, the sets [f · U] and
[f ′ · U] are either equal or disjoint. If they are not disjoint, there exists
[g] ∈[f · U] ∩[f ′ · U], so g ∼f · a ∼f ′ · a′ for paths a, a′ in U from q1
to g(1). Since U is simply connected, a ∼a′, which implies f ∼f ′ and
therefore [f · U] = [f ′ · U].
Step 4: 
X is simply connected. Suppose F : I →
X is any loop based at
q0. Let f = p ◦F, so F is a lift of f. If we write f(t) = [ft] as in Step 3,
then p ◦f(t) = p[ft] = ft(1) = f(t), so f is also a lift of f starting at q0.
By the unique lifting property, F = f. Since F is a loop,
[cq0] = q0 = F(1) = f(1) = [f1] = [f],
so f is null homotopic. By the homotopy lifting property, this means that
F is null homotopic as well.
A careful study of this proof shows that it does not really need the full
strength of the hypothesis that X is locally simply connected. Each time we
use the fact that a loop in a small open set U ⊂X is null homotopic, all we
really need to know is that it is null homotopic in X. For this reason, it is
traditional to make the following deﬁnition: A space X is semilocally simply
connected if it admits a basis of open sets U with the property that every
loop in U is null homotopic in X. It can be shown that a connected, locally
path connected space admits a universal covering space if and only if it is
semilocally simply connected (see [Mas89] or [Sie92]). Since our motivation

266
12. Classiﬁcation of Coverings
for studying the fundamental group is to understand manifolds, we have
no need for this extra generality.
Once you have understood the proof of the existence of the universal
covering space of a space X, you should forget the complicated construction
of 
X in terms of path classes, and just think of 
X as a simply connected
space with a covering map to X. The uniqueness theorem tells us that all
the relevant properties of 
X can be derived from these facts.
Proper Group Actions
The next step in classifying coverings is to start with a space Y and develop
a technique for constructing spaces covered by Y . In the next section we will
apply this to the universal covering space in order to derive a classiﬁcation
theorem for coverings of a given space X.
To get an idea how to construct spaces covered by Y , let us suppose
p: 
X →X is a normal covering. (The restriction to normal coverings will
not be a limitation in the end: For reasons that will soon become apparent,
the construction in this section will produce only normal coverings, but in
the next section we will be able to use them to produce all coverings of a
given space.)
As we observed in the previous chapter, the covering group Cp( 
X) acts
continuously and freely on 
X (on the left). The orbit criterion (Proposition
11.29) says that Cp( 
X) acts transitively on each ﬁber when p is normal, so
the identiﬁcations made by p are exactly those determined by the equiva-
lence relation x ∼y if and only if y = ϕ(x) for some ϕ ∈Cp( 
X). Since p
is a quotient map by Lemma 11.5, X is homeomorphic to the orbit space
determined by the left action of Cp( 
X) on 
X (see Chapter 3).
Now let Y be any space, and suppose we are given a left action by a group
Γ on Y . Our aim in this section is to describe conditions under which the
quotient map π: Y →Y/Γ onto the orbit space is a covering map whose
covering group is Γ. Note that this construction can produce only normal
coverings, because Γ acts transitively on the ﬁbers of any orbit space by
deﬁnition.
Not every group action yields a covering map, of course. Clearly, the
action must be continuous and free (Proposition 11.27(b)). Moreover, every
point of a covering space Y has a neighborhood (one of the “pancakes” over
an evenly covered open set) whose images under the covering group are all
disjoint, which places a strong restriction on the actions we can consider.
A simple condition that will guarantee that a group action has the req-
uisite properties in all cases of interest to us is the following. A continuous
action of a topological group Γ on a space Y is said to be proper if the map
Γ × Y →Y × Y given by (g, y) 
→(y, g · y) is a proper map, i.e., if the
inverse image of any compact set under this map is compact.

Proper Group Actions
267
Proper actions have the following useful alternative characterizations, at
least for discrete group actions on locally compact Hausdorﬀspaces, the
only type we will be concerned with. For any g ∈Γ and any subset K ⊂Y ,
we let g · K = {g · y : y ∈K}.
Proposition 12.9. For a discrete group Γ acting on a locally compact
Hausdorﬀspace Y , the following are equivalent:
(a) Γ acts properly.
(b) For any compact set K ⊂Y , K ∩(g·K) = ∅for all but ﬁnitely many
g ∈Γ.
(c) For every y, y′ ∈Y , there exist neighborhoods U of y and U ′ of y′
such that U ∩(g · U ′) = ∅for all but ﬁnitely many g ∈Γ.
Proof. We will show (a) =⇒(b) =⇒(c) =⇒(a). Assume ﬁrst that the
action of Γ is proper, and let Φ: Γ × Y →Y × Y denote the proper map
Φ(g, y) = (y, g · y). Given any compact set K ⊂Y , the set
Φ−1(K × K) = {(g, y) ∈Γ × Y : y ∈K, g · y ∈K}
is compact. Thus its projection onto Γ is compact and therefore ﬁnite. But
this projection includes all g ∈Γ such that K ∩(g· K) ̸= ∅, so this proves
(a) =⇒(b).
Now suppose (b) holds. Because Y is locally compact Hausdorﬀ, any
points y, y′ ∈Y have precompact neighborhoods U and U ′, respectively. Let
K be the compact set U∪U ′. Then the set of g ∈Γ such that K∩(g·K) = ∅
is ﬁnite, which implies (c).
Finally, if (c) holds, let L be an arbitrary compact subset of Y × Y . For
any (y, y′) ∈L, choose neighborhoods U of y and U ′ of y′ as in (c), so U ×U ′
is a neighborhood of (y, y′). The set of such product neighborhoods as (y, y′)
ranges over L is an open cover of L, so ﬁnitely many such neighborhoods
U1 × U ′
1, . . . , Um × U ′
m cover L. For each i, the set Si = {g ∈Γ : Ui ∩
(g−1 · U ′
i) ̸= ∅} is ﬁnite. Let S = S1 ∪· · · ∪Sm and K = π1(L) ⊂Y . Then
it is straightforward to check that Φ−1(L) is contained in the compact set
S×K. Since Y is Hausdorﬀ, L is closed in Y ×Y ; and since Φ is continuous,
Φ−1(L) is a closed subset of a compact set and thus compact.
Corollary 12.10. If a discrete group Γ acts freely and properly on a locally
compact Hausdorﬀspace Y , every point y ∈Y has a neighborhood U such
that U ∩(g · U) = ∅unless g = 1.
Proof. Taking y = y′ in Proposition 12.9(c), we obtain neighborhoods U
and U ′ of y such that U ∩(g · U ′) = ∅except for ﬁnitely many group
elements 1, g1, . . . , gm ∈Γ. Since the action is free and Y is Hausdorﬀ, for

268
12. Classiﬁcation of Coverings
each gi there are disjoint neighborhoods Wi of y and W ′
i of gi · y. Let
U = U ∩U ′ ∩W1 ∩(g−1
1 · W ′
1) ∩· · · ∩Wm ∩(g−1
m · W ′
m).
We will show that U has the required properties.
First consider g = gi for some i. If y ∈U ⊂g−1
i · W ′
i, then gi · y ∈W ′
i,
which is disjoint from Wi and therefore from U. Thus U ∩(gi· U) = ∅. On
the other hand, if g ∈Γ is not the identity and not one of the gi’s, then
for any y ∈U ⊂U ′, we have g · y ∈g · U ′, which is disjoint from U and
therefore also from U.
A group action possessing the property expressed in this corollary, or that
expressed in part (c) of Proposition 12.9, or something closely related to
these (depending on whom you read) has traditionally been called properly
discontinuous. This is a particularly unfortunate term, because the group
actions we are interested in are all continuous, so one is forced to speak of a
“continuous properly discontinuous action.” We will avoid the problem by
working only with proper actions, which have many important applications
in topology and geometry, and are quite suﬃcient as long as we conﬁne our
attention to locally compact Hausdorﬀspaces.
Theorem 12.11. Let Y be a connected, locally path connected, locally com-
pact Hausdorﬀspace (for example, a connected manifold), and suppose a
discrete group Γ acts continuously, freely, and properly on Y . Then Y/Γ is
Hausdorﬀ, the quotient map π: Y →Y/Γ is a normal covering map, and
Cπ(Y ) = Γ, considered as a group of homeomorphisms of Y .
Proof. Clearly, π is surjective and continuous. In fact, it is an open map,
for the following reason: If U ⊂Y is open, then π−1(π(U)) is the union of
all sets of the form g · U as g ranges over Γ. This is a union of open sets
and therefore open, so π(U) is open.
To show that π is a covering map, let y ∈Y , and choose a neighborhood
U of y as in Corollary 12.10. Let V ⊂U be the component of U containing
y; clearly, V still has the property that its images under Γ are disjoint. Let
V = π(V ), which is open in Y/Γ because π is an open map.
Now, π−1(V ) is the union of the disjoint connected open sets g · V for
g ∈Γ, so to show that π is a covering it remains only to show that π is
a homeomorphism from each such set onto V . Because for each g ∈Γ,
g: V →g · V is a homeomorphism and the diagram
V
g · V
-
g
V
π@@
R
π


	
commutes, it suﬃces to show that π: V →V is a homeomorphism. It is
surjective, continuous, and open; and it is injective because π(v) = π(v′) for

Proper Group Actions
269
v, v′ ∈V implies v′ = g·v for some g ∈Γ, so v = v′ because V ∩(g· V ) = ∅
when g ̸= 1. This proves that π is a covering map.
If g ∈Γ, then x 
→g·x is a covering transformation, since π(g·x) = π(x)
by deﬁnition; thus Γ ⊂Cπ(Y ). By construction, Γ acts transitively on each
ﬁber, so π is a normal covering. If ϕ is any covering transformation, choose
y ∈Y and let y′ = ϕ(y). Then there is some g ∈Γ such that g · y = y′;
since ϕ and x 
→g · x are covering transformations that agree at a point,
they are equal. Thus Γ is the full covering group.
To show that the quotient space is Hausdorﬀ, let Φ(g, y) = (y, g·y) as in
the proof of Proposition 12.9. Since Φ is proper, it is closed by Proposition
4.32, so Φ(Γ × Y ) is a closed subset of Y × Y . Let x, x′ ∈Y/Γ be distinct
points. Choosing y, y′ ∈Y such that π(y) = x and π(y′) = x′, the fact
that x ̸= x′ means that (y, y′) ̸∈Φ(Γ × Y ). Therefore, (y, y′) has a product
neighborhood U × U ′ ⊂Y × Y that is disjoint from Φ(Γ × Y ). Since π
is open, π(U) and π(U ′) are neighborhoods of x and x′, respectively. Any
point z ∈π(U) ∩π(U ′) would satisfy z = π(v) = π(v′) for some v ∈U
and v′ ∈U ′. But this would mean that v′ = g · v for some g ∈Γ, so
(v, v′) = (v, g · v) ∈Φ(Γ × Y ), which contradicts the fact that U × U ′ is
disjoint from the image of Φ. Thus π(U) ∩π(U ′) = ∅, which shows that
Y/Γ is Hausdorﬀ.
Corollary 12.12. Let 
M be a connected n-manifold on which a dis-
crete group Γ acts continuously, freely, and properly. Then 
M/Γ is an
n-manifold, and the quotient map π: 
M →
M/Γ is a normal covering
map.
Proof. We know from Theorem 12.11 that π is a normal covering map and

M/Γ is Hausdorﬀ, and therefore it is a manifold by Problem 11-3(a).
Example 12.13 (Lens Spaces). By identifying R4 with C2 in the obvi-
ous way, we can consider S3 as the following subset of C2:
S3 = {(z1, z2) ∈C2 : |z1|2 + |z2|2 = 1}.
Fix a pair of relatively prime integers 1 ≤m < n, and deﬁne an action of
Z/⟨n⟩on S3 by
k · (z1, z2) =

e2πik/nz1, e2πikm/nz2

.
It can easily be checked that this action is free, and it is proper because
Z/⟨n⟩is a ﬁnite group (Problem 12-6). The orbit space S3/(Z/⟨n⟩) is thus
a compact 3-manifold whose universal covering space is S3 and whose fun-
damental group is isomorphic to Z/⟨n⟩. This manifold, denoted by L(n, m),
is called a lens space.

270
12. Classiﬁcation of Coverings
A particularly important example of a free proper action arises when
we consider a topological group G and a discrete subgroup Γ (that is,
a subgroup that is a discrete subspace). Recall from Chapter 3 that left
translation deﬁnes a left action of Γ on G whose quotient is the coset space
G/Γ.
Proposition 12.14. Let Γ be a discrete subgroup of a connected, locally
path connected, locally compact Hausdorﬀtopological group G. Then Γ acts
freely and properly on G by left translations, so the quotient map π: G →
G/Γ is a normal covering map.
Proof. As we observed in Example 3.35(e), G acts freely on itself, so the
restriction of this action to Γ is certainly free. We will show that the action
is proper by showing that it satisﬁes property (b) of Proposition 12.9.
Let K ⊂G be any compact set. If γ ∈Γ is an element such that K ∩
γK ̸= ∅, then there exist g1, g2 ∈K such that g1 = γg2, which is to say
γ ∈KK−1 = {g1g−1
2
: g1, g2 ∈K}. This set KK−1 is compact because it
is the image of K × K under the continuous map from G × G to G given
by (g1, g2) 
→g1g−1
2 . Because Γ is discrete, there can be only ﬁnitely many
elements of Γ in KK−1.
Corollary 12.15. Suppose G and H are connected, locally path connected,
locally compact Hausdorﬀtopological groups, and ϕ: G →H is a surjective
continuous homomorphism with discrete kernel. If ϕ is an open or closed
map, then it is a normal covering map.
Proof. Let Γ = Ker ϕ. By the preceding proposition, the quotient map
π: G →G/Γ is a normal covering map. The assumption that ϕ is either
open or closed implies that it is a quotient map, and by the ﬁrst isomor-
phism theorem the identiﬁcations made by ϕ are precisely those made by
π. Thus the result follows from the uniqueness of quotient spaces.
Example 12.16 (Coverings of the Torus).
For any integers a, b, c, d
such that ad −bc ̸= 0, consider the map p: T2 →T2 given by p(z, w) =
(zawb, zcwd). This is easily seen to be a surjective continuous homomor-
phism, and it is a closed map by the closed map lemma. Once we show that
it has discrete kernel, it will follow from the preceding corollary that it is
a normal covering map.
Let A denote the invertible linear transformation of R2 whose matrix is
 a b
c d

. Then we have a commutative diagram
T2
T2
-
p
R2
R2
-
A
?
E
?
E
(12.2)

Proper Group Actions
271
where E(x, y) = (e2πix, e2πiy) is the universal covering map of the torus.
To identify Ker p, note that
p ◦E(x, y) = (1, 1) ⇐⇒E ◦A(x, y) = (1, 1)
⇐⇒A(x, y) ∈Z2
⇐⇒(x, y) ∈A−1(Z2),
where A−1(Z2) denotes the additive subgroup {A−1(m, n) : (m, n) ∈Z2}
of R2. Because E is surjective, this shows that Ker p = E ◦A−1(Z2).
Since A−1 has rational entries, it follows easily that each element of Ker p
has ﬁnite order in T2. Moreover, since Z2 is generated (as a group) by the
two elements (1, 0) and (0, 1), Ker p is generated by their images under
E ◦A−1. An abelian group that is generated by ﬁnitely many elements of
ﬁnite order is easily seen to be ﬁnite; in particular, it is discrete.
Application: Universal Coverings of Higher Genus Surfaces
As another application of the theory of proper group actions, we will show
that the unit disk B2 ⊂C is the universal covering space of all the ori-
entable surfaces of genus n ≥2. The construction is rather involved, so
we will describe the main steps and leave some of the details for you to
work out. Some of these steps can be done a bit more straightforwardly if
you know a little about Riemannian metrics and their geodesics, but we
will not assume any such knowledge. We will, however, assume a passing
acquaintance with complex analysis, at least enough to understand what
it means for a function to be complex analytic.
We begin by describing a special metric on the disk. For z1, z2 ∈B2,
deﬁne
d(z1, z2) = cosh−1

1 +
2|z1 −z2|2
(1 −|z1|2)(1 −|z2|2)

.
This is a metric, called the hyperbolic metric. (The only property of a
metric that is not straightforward to check is the triangle inequality; a way
to prove it is indicated in Problem 12-8.)
The disk with this metric, called the hyperbolic disk, is one model of
non-Euclidean plane geometry. The “straight lines” in this geometry, called
hyperbolic geodesics, are the intersections with the disk of Euclidean circles
and lines meeting the unit circle orthogonally (Figure 12.6). (A line segment
through the origin can be thought of as the limiting case of a circular arc as
the radius goes to inﬁnity.) It is easy to check that “two points determine a
line”: That is, given any two points in the disk, there is a unique hyperbolic
geodesic passing through both points.

272
12. Classiﬁcation of Coverings
0
FIGURE 12.6. Hyperbolic geodesics.
The most interesting feature of the hyperbolic metric is that it is pre-
served by a transitive group action. Let α and β be complex numbers with
|α|2 −|β|2 > 0, and deﬁne
ϕ(z) = αz + β
βz + α.
(12.3)
A straightforward calculation shows that ϕ is continuous, takes the
disk to itself, and preserves the hyperbolic metric in the sense that
d(ϕ(z1), ϕ(z2)) = d(z1, z2) for all z1, z2 ∈B2. Any such map is called a
M¨obius transformation of the disk, and the set M of all such maps is a
group under composition, called the M¨obius group of the disk. It can be
identiﬁed with the group of matrices of the form
 α β
β α

and so is a topo-
logical group acting continuously on B2.
M¨obius transformations take geodesics to geodesics, as can be seen by
substituting ϕ(z) for z in the equation deﬁning a circle or line intersecting
the boundary of the disk orthogonally, and noting that it reduces to another
equation of one of the same types. In fact, the same computation shows
that a M¨obius transformation takes the intersection of the disk with any
Euclidean circle or line to another set of one of the same forms.
One special case worth noting is that any rotation of the disk z 
→eiθz
is a M¨obius transformation with α = eiθ/2 and β = 0, so the hyperbolic
metric is invariant under rotations. In fact, any M¨obius transformation that
takes the origin to itself must be of this form, because (12.3) reduces to
ϕ(z) = (α/α)z in that case. Observe also that the hyperbolic distance from
the origin to z depends only on |z|, so any metric ball Br(0) about the origin
is actually a Euclidean disk centered at 0, and its boundary is a Euclidean
circle. Since M¨obius transformations preserve hyperbolic distance and take
circles to circles, it follows that every metric ball is a Euclidean disk. (Its
Euclidean center may not be the same as its hyperbolic center, however).
It also follows that the hyperbolic metric generates the Euclidean topology.

Proper Group Actions
273
The left action of M on the disk deﬁned by (12.3) is transitive because
any z0 ∈B2 is carried to 0 by the M¨obius transformation
ϕ(z) = z −z0
1 −z0z .
(12.4)
In fact, more is true: Given any two pairs of points z0, z1 and z′
0, z′
1 such
that d(z0, z1) = d(z′
0, z′
1), there is a unique M¨obius transformation taking
z0 to z′
0 and z1 to z′
1 (and therefore taking the geodesic segment joining
z0, z1 to the one joining z′
0, z′
1). To prove this, let ψ = ρ ◦ϕ, where ϕ is
the transformation (12.4) and ρ is a rotation moving ϕ(z1) to the positive
x-axis, so that ψ takes z0 to 0 and z1 to some λ > 0. Similarly, there is
a transformation ψ′ taking z′
0 to 0 and z′
1 to λ′ > 0. Since M¨obius trans-
formations preserve distances, λ and λ′ are at the same distance from 0
along the positive x-axis and therefore must be equal, so ψ′−1 ◦ψ is the
transformation we seek. It is unique because if γ is any M¨obius transfor-
mation taking z0 to z′
0 and z1 to z′
1, the composition ψ′ ◦γ ◦ψ−1 ﬁxes 0
and therefore must be a rotation, and since it also ﬁxes λ, it must be the
identity, which implies γ = ψ′−1 ◦ψ.
Each M¨obius transformation ϕ is complex analytic with nowhere van-
ishing derivative. Multiplication by the complex derivative ϕ′(z0) deﬁnes
a linear map from C to C, which can be interpreted geometrically as
the action of ϕ on tangent vectors to curves: For any diﬀerentiable pa-
rametrized curve f : (−ε, ε) →B2 with f(0) = z0, the chain rule gives
(ϕ ◦f)′(0) = ϕ′(z0)f ′(0). Thus ϕ acts on tangent vectors by multiplying
them by the nonzero complex number ϕ′(z0), and since all tangent vectors
are rotated through the same angle, every M¨obius transformation is con-
formal, meaning it preserves angles between tangent vectors. (We will also
be considering angles between geodesics, by which we always mean angles
between their tangent vectors.) In particular, if ϕ(z) = eiθz is rotation
through an angle θ, then ϕ′(0) = eiθ rotates tangent vectors through the
same angle. It follows that the only M¨obius transformation that ﬁxes the
origin and ﬁxes the direction of a tangent vector at the origin is the iden-
tity. In fact, a M¨obius transformation that ﬁxes any point and a tangent
direction at that point must be the identity, because conjugation with a
transformation taking the ﬁxed point to 0 yields a transformation that ﬁxes
0 and a tangent direction at 0.
Now let M be a compact orientable surface of genus n ≥2. We will show
that there is a discrete subgroup Γ ⊂M acting freely and properly on B2
such that M is homeomorphic to B2/Γ. It follows from Theorem 12.11 that
the universal covering space of M is B2.
Recall from Chapter 6 the standard polygonal presentation of M as a
quotient of a polygonal region with 4n sides whose edges are identiﬁed in
pairs. We will realize M as a quotient of a compact region in B2 bounded
by a geodesic polygon, that is, the union of ﬁnitely many geodesic segments.
We begin by constructing a 4n-sided geodesic polygon whose edges have

274
12. Classiﬁcation of Coverings
θ ≈π −π/2n.
θ ≈0.
θ = π/2n.
θ
P
FIGURE 12.7. Geodesic polygons with interior angles 0 < θ < π −π/2n.
equal lengths and meet at equal angles (a regular geodesic polygon). Start
with 4n points (z0, z1, . . . , z4n = z0) equally spaced on some circle about
the origin. Because the hyperbolic metric is invariant under rotations, the
geodesic segments joining zj and zj+1 for j = 0, . . . , 4n −1 all have the
same length and meet at equal angles, so their union is a regular geodesic
polygon. As the radius of the circle goes to zero, these geodesics approach
line segments through the origin, and deﬁne small regular geodesic polygons
whose interior angles are very close to what they would be in the Euclidean
case, namely π −π/2n (see Figure 12.7). As the points get farther from
the origin, the arcs become nearly tangent to each other, deﬁning geodesic
polygons with interior angles very near zero. By continuity, somewhere in
between there is a polygon whose interior angles are exactly θ = π/2n.
(Note that this does not work when n = 1, so we cannot construct a
covering of the torus in this manner.)
Let P be the compact subset of B2 consisting of this regular geodesic
polygon together with the bounded component of its complement. Choose
one vertex v0, and label the edges a1, b1, a−1
1 , b−1
1 , . . . , an, bn, a−1
n , b−1
n
in
counterclockwise order starting from v0. (See Figure 12.8, but ignore the
vertex labels other than v0 for now.) For each edge pair aj, a−1
j , there is
a unique M¨obius transformation αj that takes the edge labeled a−1
j
onto
the one labeled aj, with the initial vertex of one going to the initial vertex
of the other. Similarly, let βj be the transformation taking bj to b−1
j
and
respecting the initial and terminal vertices. Let Γ ⊂M be the subgroup
generated by {αj, βj : j = 1, . . . , 4n}. We will call the generators αj, βj,
and their inverses edge pairing transformations.
One important property of the edge pairing transformations is easy to
verify: If σ is any edge pairing transformation, then P ∩σ(P) consists of
exactly one edge of P. To see why, suppose σ takes an edge e to another
edge e′. Then clearly, P ∩σ(P) contains e′. Note that the complement of any
geodesic in B2 has exactly two components, which we may call the sides of
the geodesic. Because P is connected and lies on one side of each of its edges,
the same is true of σ(P). Using conformality and following what σ does to a
vector that is perpendicular to e and points into P, it is easy to check that

Proper Group Actions
275
a1
b1
a−1
1
b−1
1
v0
v1
v2
v3
v4
α1
β1
FIGURE 12.8. Edge pairing transformations.
σ(P) lies on the opposite side of e′ from P, and therefore P ∩σ(P) consists
of exactly the edge e′. Because P is obviously homeomorphic to a regular
Euclidean polygon, the quotient of P by the identiﬁcations determined by
the edge pairing transformations is homeomorphic to M. Let p: P →M
denote the quotient map.
Theorem 12.17. The group Γ is discrete and acts freely and properly on
B2, and the quotient B2/Γ is homeomorphic to M. The restriction of this
quotient map to P is p.
Proof. The ﬁrst thing we will prove is that the edge pairing transformations
satisfy the same relation as the generators of the fundamental group of M:
α1 ◦β1 ◦α−1
1
◦β−1
1
◦· · · ◦αn ◦βn ◦α−1
n
◦β−1
n
= Id .
(12.5)
Actually, it will be more convenient to prove the equivalent identity ob-
tained by inversion:
βn ◦αn ◦β−1
n
◦α−1
n
◦· · · ◦β1 ◦α1 ◦β−1
1
◦α−1
1
= Id .
(12.6)
To simplify the notation, let us write the sequence of transformations on
the left-hand side of (12.6) as σ4n ◦· · · ◦σ2 ◦σ1.
By deﬁnition, σ1 = α−1
1
takes v0, the initial vertex of the edge labeled
a1, to the initial vertex of the edge labeled a−1
1 . If we label the vertices in

276
12. Classiﬁcation of Coverings
V0
V1
V2
V3
V4
α
β
α−1
β−1
θ
2θ
3θ
4θ
FIGURE 12.9. Images of a vector V0 under edge pairing transformations.
counterclockwise order starting from v0 as v0, v3, v2, v1, v4 as in Figure 12.8,
it is easy to check one step at a time that σj takes vj−1 to vj for j = 1, . . . , 4.
Since v4 is also the initial vertex of the edge labeled a2, we can continue
by induction to number all the remaining vertices v5 through v4n = v0 in
such a way that σj(vj−1) = vj. In particular, σ4n ◦· · ·◦σ2 ◦σ1(v0) = v0. To
show that this composition is the identity, it suﬃces to show that it ﬁxes
a tangent direction at v0.
For any vertex vj, we will measure angles of vectors at vj from the edge
adjacent to vj in the counterclockwise direction (so we measure from a1 at
v0, from b−1
1
at v1, etc.). Positive angles will always be understood to mean
counterclockwise rotation from that edge. Let θ = π/2n be the measure of
the interior angles of P.
Let V0 be a nonzero vector that makes an angle of 0 at v0 (see Figure
12.9), and for j = 1, . . . , 4n let Vj be the image of V0 under σj ◦· · · ◦σ1,
so that σj takes Vj−1 to Vj. We will prove the following claim: For each j,
the angle of Vj at vj is jθ. For j = 0 this is immediate from the deﬁnition
of V0. For j = 1, note that σ1 = α−1
1
takes a1 to a−1
1 , and therefore takes
V0 to a vector V1 that points in the direction of a−1
1 , which makes an angle
θ with b−1
1 . Next, since M¨obius transformations preserve angles, the image
V2 of V1 under σ2 = β−1
1
makes an angle θ with b1, which is the same as
an angle 2θ with a−1
1 . A similar analysis shows that the angles of V3 and
V4 are 3θ and 4θ, respectively, and the claim is then proved for all j by

Proper Group Actions
277
induction. In particular, the angle of V4n is 4nθ = 2π, so V4n points in the
same direction as V0. This completes the proof of (12.5).
Now we have to prove that Γ is discrete and acts freely and properly
on B2. It seems to be impossible to prove this by directly analyzing the
action of Γ, so instead we resort to a rather circuitous trick due originally
to Poincar´e. We will construct “by hand” a covering space of M that ought
to be its universal covering space, as a union of inﬁnitely many copies of
P—one for each element of π1(M)—with “adjacent” copies glued together
by the identiﬁcations determined by the edge pairing transformations. Only
later will we show that this space is homeomorphic to B2, and therefore is
simply connected and so is in fact the universal covering space.
Let G be the abstract group with presentation ⟨α1, β1, . . . , αn, βn |
α1β1α−1
1 β−1
1
· · · αnβnα−1
n β−1
n ⟩, which is isomorphic to π1(M). Let ∼be
the equivalence relation on G × P generated by all relations of the form
(g, σ(z)) ∼(gσ, z), where σ is an edge pairing transformation and both z
and σ(z) are points in ∂P. Give G the discrete topology, and let 
M denote
the quotient space G × P/∼. We will denote the equivalence class of (g, z)
in 
M by [g, z], and the quotient map by π: G × P →
M.
Left translation in the G factor deﬁnes a natural continuous action of G
on G × P. This respects the identiﬁcations made by π, so it descends to a
continuous action of G on 
M, satisfying g′ · [g, z] = [g′g, z]. This action is
free, because (g′g, z) ∼(g, z) only when g′ = 1.
The subset P = π({1} × P) = {[1, z] : z ∈P} of 
M is homeomorphic
to P (why?), and 
M is the union of the sets g · P = {[g, z] : z ∈P} as g
ranges over G. Each of these sets is a homeomorphic copy of P in 
M, and
the copies g· P and g′· P intersect in an edge precisely when g and g′ diﬀer
by a single edge pairing transformation. Since there are only ﬁnitely many
such transformations, this means in particular that each set g· P intersects
only ﬁnitely many others.
Because ∼identiﬁes only points (g, z) with z ∈∂P, the ﬁber of π over
any point [g0, z0] for z0 ∈Int P consists of exactly one point (g0, z0) ∈
G × P. If z0 is in ∂P but is not a vertex, then z0 lies on one edge, and
there is exactly one edge pairing transformation σ that identiﬁes that edge
with another edge; thus the ﬁber over [g0, z0] is exactly two points (g0, z0)
and (gσ−1, σ(z0)). If z0 is a vertex of P, then by the argument at the
beginning of the proof there is a sequence of edge pairing transformations
σ1, . . . , σ4n (possibly a cyclic permutation of the sequence we considered
earlier) such that the points zj = σj ◦· · · ◦σ1(z0) are the vertices of P, so
the ﬁber over [g0, z0] consists of the 4n points (g0σ−1
1 , z1), (g0σ−1
1 σ−1
2 , z2),
. . . , (g0σ−1
1
· · · σ−1
4n , z4n) = (g0, z0).

278
12. Classiﬁcation of Coverings
There is a natural continuous map p: 
M →M given by p[g, z] = p(z),
obtained from p ◦π2 by passing to the quotient:

M
M.
-
p
G × P
P
-
π2
?
π
?
p
Clearly, p is surjective, because p( P) = M. It is a quotient map for the
following reason: If U ⊂
M is an open set that is saturated with respect to
p, then π−1(U) ⊂G×P is open and saturated with respect to p◦π = p◦π2,
and since p ◦π2 is a quotient map, it follows that p(U) = p ◦π(π−1(U)) =
p ◦π2(π−1(U)) is open. You can check that the ﬁbers of p are precisely the
orbits of G in 
M, so we can identify M with the orbit space 
M/G. We wish
to show that p is actually a covering map.
To show that p is a covering, by Theorem 12.11 it suﬃces to show that

M is connected, locally path connected, locally compact, and Hausdorﬀ,
and that the action of G on 
M is proper. [[Connectedness]] is easy: If σ is an
edge pairing transformation taking edge e to edge e′, then the connected
sets P and σ · P have the points [1, σ(z)] = [σ, z] in common for z ∈e, so
P ∪(σ · P) is connected. By induction, any set of the form P ∪(σ1 · P) ∪
· · · ∪(σm · · · σ1)· P is connected. Since 
M is the union of all such sets, and
they all have points of P in common, 
M is connected.
To prove the other properties of 
M, we ﬁrst need to introduce some more
maps. Let τ : G →Γ be the homomorphism that sends each generator αi
or βi to itself (thought of as an element of Γ), which is well-deﬁned because
(12.5) holds in Γ. The map G × P →B2 deﬁned by (g, z) 
→τ(g)z is
continuous and respects the identiﬁcations made by ∼, so it descends to a
continuous map δ: 
M →B2 given by δ[g, z] = τ(g)z. It takes the action of
G on 
M over to the action of Γ on B2, in the sense that
δ(g · x) = τ(g) ◦δ(x).
(12.7)
The most important feature of 
M is that every x ∈
M has a neighborhood
U with the following properties:
(i) U is mapped homeomorphically by δ onto a closed hyperbolic ball
Bε(δ(x)) ⊂B2.
(ii) δ(U) = Bε(δ(x)).
(iii) U intersects the sets g · P for only ﬁnitely many g ∈G.
We will call any such set U a regular hyperbolic neighborhood of x.

Proper Group Actions
279
From the existence of regular hyperbolic neighborhoods it follows imme-
diately that
• 
M is locally compact and locally path connected, because each regular
hyperbolic neighborhood has these properties.
• 
M is Hausdorﬀ: Let x, x′ ∈
M, and let U, U ′ be regular hyperbolic
neighborhoods of them. If x′ ̸∈U, then shrinking U a bit if necessary
we may assume x′ ̸∈U, so that U and U ′ ∖U are disjoint neigh-
borhoods of x and x′. On the other hand, if x′ ∈U, then the inverse
images under δ|U of disjoint neighborhoods of δ(x) and δ(x′) are open
sets separating x and x′.
• The action of G on 
M is proper: With x, x′, U, and U ′ as above,
there can be at most ﬁnitely many g ∈G such that U ∩(g· U ′) ̸= ∅,
because U and U ′ intersect only ﬁnitely many of the sets g · P.
Thus, to complete the proof that p is a covering map, we need only prove
the existence of a regular hyperbolic neighborhood of each point.
Let x = [g0, z0] be an arbitrary point of 
M. The ﬁber over x consists of
ﬁnitely many points of the form (gj, zj), where zj = σj ◦· · ·◦σ1(z0) for some
(possibly empty) sequence of edge transformations σ1, . . . , σj and gj =
g0σ−1
1
· · · σ−1
j . (The ﬁber contains one, two, or 4n such points depending
on whether z0 is an interior point, an edge point, or a vertex.) Choose ε > 0
smaller than half the distance from z0 to any edge that does not contain
z0. Let W ⊂G × P be the union of the sets {gj} × (Bε(zj) ∩P), and let
U = π(W). Because W is a saturated open set, U is a neighborhood of x
in 
M. Similarly, W is the union of the sets {gj}×(Bε(zj)∩P), a saturated
closed set, so π(W) = U. Clearly, U intersects g · P for only ﬁnitely many
g.
To complete the proof that U is a regular hyperbolic neighborhood, we
need to show that δ is a homeomorphism from U to Bε(z0) taking U to
Bε(z0). Since the diagram
g · U
Bε(δ(g · x))
-
δ
U
Bε(δ(x))
-
δ
?
g
?
τ(g)
commutes for each g ∈G and the vertical maps are homeomorphisms, it
suﬃces to prove this for x = [1, z0] ∈P. We consider three cases.
Case I: z0 ∈Int P. In this case, U ⊂P, and it is immediate from the
deﬁnitions that δ is one-to-one on U, δ(U) = Bε(z0), and δ(U) = Bε(z0).
Since U is the image under π of a compact set, it is compact, so δ: U →
Bε(z0) is a homeomorphism by the closed map lemma.

280
12. Classiﬁcation of Coverings
z0
z1
{1} × P
{σ−1} × P
P
δ
FIGURE 12.10. Hyperbolic neighborhood of an edge point.
Case II: z0 ∈∂P, but z0 is not a vertex. Let e0 denote the edge con-
taining z0. By our choice of ε, Bε(z0) ∩P contains the entire portion of
Bε(z0) lying on one side of e0 (Figure 12.10). There is one edge pairing
transformation σ that takes e0 to another edge e1, and thus takes z0 to
z1 = σ(z0) ∈e1. As a M¨obius transformation of B2, σ takes Bε(z0) home-
omorphically onto Bε(z1). Since Bε(z0) ∩P and σ−1(Bε(z1) ∩P) lie on
opposite sides of e0, Bε(z0) = (Bε(z0) ∩P) ∪σ−1(Bε(z1) ∩P). Then
δ(U) = δ(W) = (Bε(z0) ∩P) ∪σ−1(Bε(z1) ∩P) = Bε(z0).
The restriction of δ to U is one-to-one, takes U onto Bε(z0), and as before
is a homeomorphism by the closed map lemma.
Case III: z0 is a vertex of P. Then δ(U) = δ(W) is the union of the sets
δ({σ−1
1
· · · σ−1
j } × (Bε(zj) ∩P)) = σ−1
1
◦· · · ◦σ−1
j (Bε(zj) ∩P),
where z1, . . . , z4n are the vertices of P. To see what these sets are, look back
at the proof of (12.5); from that analysis, it follows that σ−1
1 ◦· · ·◦σ−1
j
maps
zj to z0 and maps Bε(zj) ∩P to the sector of Bε(z0) lying between the
geodesics passing through z0 at angles −jθ and (−j + 1)θ (Figure 12.11).
These sectors ﬁt together to make up the entire closed ball Bε(z0), and
δ maps U bijectively to Bε(z0). As above, it is a homeomorphism by the
closed map lemma.

Proper Group Actions
281
P
δ(U)
FIGURE 12.11. Hyperbolic neighborhood of a vertex point.
This completes the proof of the existence of hyperbolic neighborhoods
and thus the proof that p: 
M →M is a covering map. To ﬁnish the proof of
the theorem, we will show that δ: 
M →B2 is also a covering map. Since B2
is simply connected, this implies that δ is a homeomorphism. The theorem
follows from this, as we now show.
First, τ : G →Γ is a group isomorphism: It is surjective because it takes
generators of G to generators of Γ; and it is injective because if τ(g) = Id,
then for any x ∈
M we have δ(g · x) = τ(g)δ(x) = δ(x), which implies
g·x = x and therefore g = 1 because G acts freely. It follows that the action
of Γ on B2 is equivalent to that of G on 
M under the homeomorphism δ, and
the quotient map B2 →B2/Γ is equivalent to the covering map p: 
M →M.
Therefore, the action of Γ on B2 is free and proper, and the restriction of
the covering map to P is p◦δ−1|P = p. To see that Γ is a discrete subgroup
of M, suppose γi →γ in Γ. By continuity γiz →γz for any z ∈B2, and
setting gi = τ −1(γi), g = τ −1(γ), and x = δ−1(z) we obtain gi · x →g · x.
Since the gi’s are covering transformations, this can happen only if gi = g
(and therefore γi = γ) for all suﬃciently large i.
To show that δ is a covering, we need the following additional fact about
regular hyperbolic neighborhoods: There exists some r > 0 such that every
point x ∈
M has a regular hyperbolic neighborhood Ux whose closure is
mapped homeomorphically by δ onto Br(δ(x)). To prove this, let K ⊂
M
denote the union of P together with its images σi · P under the 4n edge
pairing transformations σi. Since K is compact, so is its image δ(K) ⊂B2,
and it is easy to see that δ(K) contains a neighborhood of P. As U ranges
over regular hyperbolic neighborhoods of points in K, the sets δ(U) form
an open cover of δ(K). Let c be a Lebesgue number for this cover, and
choose r < c small enough that for each z ∈P the hyperbolic ball Br(z)
is contained in δ(K). This means that for every z ∈P, there is a regular

282
12. Classiﬁcation of Coverings
P
P
U
δ(U)
x
x0
Ux0
δ(x0)
δ(x)
FIGURE 12.12. Finding regular hyperbolic balls of ﬁxed radius.
hyperbolic neighborhood U of some point x ∈K such that Br(z) ⊂δ(U).
For each x0 ∈P, choose a regular hyperbolic neighborhood U of some
x ∈K such that Br(δ(x0)) is contained in δ(U) (Figure 12.12), and let
Ux0 = (δ|U)−1(Br(δ(x0)); then δ: U x0 →Br(δ(x0)) is the restriction of a
homeomorphism and hence is itself a homeomorphism. Since δ is injective
on P and δ(x0) ∈δ(Ux0), Ux0 is the desired neighborhood of x0. For any
other x ∈
M, there is some g ∈G such that g · x ∈P, so we can set
Ux = g−1 · Ug·x.
We can now prove that δ is a covering map. First we need to show that
it is surjective. If it were not, the image set δ(
M) would have a boundary
point z0 ∈B2. There is some point z ∈δ(
M) whose distance from z0 is
less than r/2. But then z = δ(x) for some x ∈
M, and δ(Ux) = Br(z),
which is a neighborhood of z0. This contradicts the assumption that z0 is
a boundary point of the image.
For any z0 ∈B2, we will show that Br/2(z0) is evenly covered. Let V
be a component of δ−1(Br/2(z0)) in 
M. Since 
M is locally path connected,
V is open. We need to show that δ: V →Br/2(z0) is a homeomorphism.
Choose x ∈V , set z = δ(x), and let σ = (δ|Ux)−1 : Br(z) →Ux.
Now, σ(Br/2(z0)) is a connected subset of δ−1(Br/2(z0)) that contains a
point x in common with V , so it must be contained in V . This implies, for
any z′ ∈Br/2(z0), that δ(σ(z′)) = z′, so δ: V →Br/2(z0) is surjective.
On the other hand, ∂Br(z) is disjoint from Br/2(z0) by the triangle
inequality. Since δ takes ∂Ux to ∂Br(z), it follows that ∂Ux ∩V = ∅. Now,
V ∩Ux is open in 
M and therefore open in V , and V ∩Ux = V ∩U x is
closed in V . Since V is connected, V ∩Ux is all of V , which means that
V ⊂Ux. Thus δ|V is the restriction of a homeomorphism, so it is injective
and open, and therefore δ: V →Br/2(z0) is a homeomorphism.

The Classiﬁcation Theorem
283
Corollary 12.18. Let M be a compact surface. The universal covering
space of M is homeomorphic to
(a) S2 if M ≈S2 or P2;
(b) R2 if M ≈T2 or P2 # P2;
(c) B2 if M is any other surface.
Proof. This was proved for all the orientable surfaces and P2 in this chapter.
If M is a connected sum of n ≥2 projective planes, then by Problem 11-8
M has a two-sheeted covering by the orientable surface N of genus n−1. If

M is the universal covering space of M, then 
M also covers N by Corollary
12.6(a), so M and N have the same universal covering space.
Note that R2 and B2 are homeomorphic, so up to topological equiva-
lence there are only two simply connected 2-manifolds that cover compact
surfaces. It is useful, however, to distinguish the two cases because of the
diﬀerent character of their covering transformations. For example, the cov-
ering transformations for the torus are all translations of the plane that
preserve the Euclidean metric, while for the higher genus orientable sur-
faces they are M¨obius transformations.
The Classiﬁcation Theorem
In this section we assemble the results of this chapter to come up with
a complete classiﬁcation of coverings of a given space. The idea is that
every covering of X is itself covered by the universal covering space, and
intermediate coverings can be built from the universal covering as quotients
by suitable group actions.
Theorem 12.19 (Classiﬁcation of Coverings). Let X be a connected,
locally simply connected, locally compact Hausdorﬀspace (for example, any
connected manifold), and let q ∈X be any base point. There is a one-to-
one correspondence between isomorphism classes of coverings of X and
conjugacy classes of subgroups of π1(X, q). The correspondence associates
each covering p′ : X′ →X with the conjugacy class of its induced subgroup.
Proof. The covering isomorphism theorem shows that there is at most one
isomorphism class of coverings corresponding to any conjugacy class of
subgroups, so all we need to show is that there is at least one. Let H ⊂
π1(X, q) be any subgroup in the given conjugacy class. Let p: 
X →X be
the universal covering of X, and choose a base point q ∈p−1(q). Then the
simply connected case of the covering group structure theorem (Corollary
11.32) shows that π1(X, q) is isomorphic to the covering group Cp( 
X),

284
12. Classiﬁcation of Coverings
under the map α: π1(X, q) →Cp( 
X) that sends [f] to the unique covering
transformation ϕ taking q to q · [f]. Let H = α(H) ⊂Cp( 
X).
Since Cp( 
X) acts freely and properly on 
X, it follows easily that H does
too. So let X′ denote the quotient space 
X/ H and π: 
X →X′ the quotient
map; by Theorem 12.11, π is a normal covering map. Moreover, p: 
X →X
is constant on the ﬁbers of π (since they are contained in the ﬁbers of p),
so p descends to a continuous map p′ : X′ →X such that the following
diagram commutes:
p′


	
X′
π
@@
R

X
X.
?
p
We have to show that p′ is a covering map. Let q1 ∈X be arbitrary,
let U be a neighborhood of q1 that is evenly covered by p, and let U ′ be
any component of p′−1(U). To show that p′ is a covering map, it suﬃces
to show that U ′ is mapped homeomorphically onto U by p′.
Because X′ is locally path connected, U ′ is open and closed in p′−1(U).
Thus π−1(U ′) is open and closed in π−1(p′−1(U)) = p−1(U), which implies
that it is a union of components of p−1(U). If U is any such component,
the following diagram commutes:
p′


	
U ′
π
@@
R
U
U.
?
p
(12.8)
In this diagram, p = p′ ◦π is a homeomorphism, so π is injective on U. If
π(U) ̸= U ′, then
π(π−1(U ′)) =

ϕ∈
H
π(ϕ(U)) = π(U) ̸= U,
which contradicts the fact that π: 
X →X′ is surjective. Thus π: U →U ′
is bijective, and because it is an open map, it is a homeomorphism. Since
p and π are homeomorphisms in (12.8), so is p′.

The Classiﬁcation Theorem
285
ϕ(q)
q
ϕ
f
p′ ◦f
f

X
X
X′
p
π
p′
q
q′
FIGURE 12.13. Proof of the classiﬁcation theorem.
The last step is to show that p′
∗π1(X′, q′) = H for some q′ ∈X′ such
that p′(q′) = q. Let q′ = π(q) and consider the following diagram:
π1(X, q)
Cp( 
X),
-
α
π1(X′, q′)
Cπ( 
X)
-
α′
?
p′
∗
?
ι
where α′ and α represent the isomorphisms given by the covering group
structure theorem, and ι is inclusion.
If this diagram commutes, we are done, because then
p′
∗π1(X′, q′) = α−1 ◦ι ◦α′(π1(X′, q′))
= α−1 ◦ι(Cπ( 
X))
= α−1( H) = H.
To see that it commutes, let [f] ∈π1(X′, q′) be arbitrary, and let ϕ = α′[f],
so ϕ takes q to q·[f] = f(1), where f is the lift of f to a path in 
X starting
at q (Figure 12.13). Then ι ◦α′[f] = ϕ, thought of as an element of Cp( 
X).
On the other hand, α ◦p′
∗[f] = α[p′ ◦f] is the transformation ψ ∈Cp( 
X)
taking q to 
p′ ◦f(1). Now, p ◦f = p′ ◦π ◦f = p′ ◦f, so f is the lift of
p′ ◦f starting at q, which implies that 
p′ ◦f(1) = f(1). Thus ϕ = ψ and
the diagram commutes.

286
12. Classiﬁcation of Coverings
We end with a pair of interesting and representative examples.
Example 12.20 (Coverings of Lens Spaces).
By the preceding the-
orem, the coverings of the lens space L(n, m) are in one-to-one corre-
spondence with subgroups of Z/⟨n⟩. (Since Z/⟨n⟩is abelian, each con-
jugacy class contains precisely one subgroup.) Since every subgroup of a
cyclic group is cyclic (Exercise A.27), the only possibilities for subgroups
G ⊂π1(L(n, m)) are cyclic groups of order p where p is a factor of n. In
each such case, a covering of L(n, m) is obtained by restricting the action
of Z/⟨n⟩on S3 to G, and mapping the resulting quotient space down to
L(n, m) by sending each G-equivalence class to its Z/⟨n⟩-equivalence class.
If n = pq for positive integers p and q, let G ⊂Z/⟨n⟩be the cyclic sub-
group of order p generated by (the coset of) q. It is easy to check from
the deﬁnitions that S3/G = L(p, m), and we obtain a q-sheeted covering
L(p, m) →L(n, m). These are the only coverings of the lens spaces up to
isomorphism.
Our last application will be to classify all the coverings of the torus up
to isomorphism.
Proposition 12.21 (Classiﬁcation of Torus Coverings).
Every cov-
ering of T2 is isomorphic to precisely one of the following:
(a) the universal covering E : R2 →T2;
(b) the coverings p : S1 × R →T2 by p(z, y) = (zaε(y)b, zbε(y)−a), where
(a, b) are integers with a ≥0 and b > 0 if a = 0;
(c) the coverings p : T2 →T2 by p(z, w) = (zawb, wc), where (a, b, c) are
integers with 0 ≤b < a and c > 0.
Proof. Note that all of these maps are coverings: the universal cover by
Example 11.3; the maps in part (b) by Problem 12-7; and those in part (c)
by Example 12.16.
Let us use q = (1, 1) ∈T2 as base point, and represent π1(T2, q) as the
product group ⟨β⟩×⟨γ⟩, where β and γ are the path classes of the standard
generator of π1(S1, 1) in the ﬁrst and second factors, respectively. Then the
map (m, n) 
→βmγn is an isomorphism of Z2 with π1(T2, q).
The classiﬁcation theorem says that isomorphism classes of coverings of
T2 are in one-to-one correspondence with subgroups of π1(T2, q) under the
correspondence that matches a covering p : X →T2 with the subgroup
induced by p. So we begin by showing that each subgroup of Z2 is one and
only one of the following:
(i) the trivial subgroup;
(ii) inﬁnite cyclic subgroups generated by (a, b) satisfying the conditions
of (b) above;

The Classiﬁcation Theorem
287
(iii) subgroups of the form Z⟨(a, 0), (b, c)⟩, where (a, b, c) satisfy the con-
ditions of (c) above.
To prove this, let G be an arbitrary subgroup of Z2. Because Z2 is free
abelian of rank 2, G is free abelian of rank at most 2 by Proposition 9.13.
Thus there are three mutually exclusive cases, in which G has rank 0, 1,
or 2. Clearly, the trivial subgroup has rank 0; we will show that the rank 1
and 2 cases correspond to (ii) and (iii), respectively.
If G has rank 1, it is cyclic. In this case there are two elements (a, b) and
(−a, −b) that generate G, and exactly one of these satisﬁes the conditions
of (b). Thus (i) corresponds to the rank 1 case.
It remains to show that when G has rank 2 there are unique integers
(a, b, c) satisfying the conditions in (c) such that {(a, 0), (b, c)} forms a basis
for G. The subgroup G1 = G ∩(Z × {0}) is not trivial: If {(m, n), (i, j)}
is any basis for G, then j(m, n) −n(i, j) is an element of G in Z × {0},
which is not (0, 0) because of the independence of (m, n) and (i, j). Since
Z × {0} is cyclic, so is G1. Let (a, 0) be a generator of G1; replacing it by
its negative if necessary, we may assume a > 0.
Since G has rank 2, it is not contained in G1. As in the proof of Propo-
sition 9.13, there is a basis for G of the form {(a, 0), (b, c)}, where c is a
generator of the image of G under the projection π2 : Z2 →Z. Replacing
(b, c) by its negative if necessary, we may assume c > 0. Subtracting a
multiple of (a, 0) from (b, c) (which still yields a basis), we may assume
0 ≤b < a. Thus we have found (a, b, c) satisfying the conditions in (c) such
that (a, 0) and (b, c) are a basis for G.
Finally, we need to show that two such triples (a, b, c) and (a′, b′, c′)
that determine the same subgroup are identical. Since each basis can be
expressed in terms the other, there is an integer matrix M such that
a
b
0
c

M =
a′
b′
0
c′

.
Examining the lower left entry in this equation shows that M is also upper
triangular. Since M has an inverse that also has integer entries, its deter-
minant must be ±1; and then the above equation shows that det M = 1
(recall that a, c, a′, and c′ are all positive). Since M is upper triangular, its
determinant is the product of its (integer) diagonal entries, so these must
be both +1 or both −1; and then the fact that a and a′ are both positive
forces both diagonal entries to be 1, so a = a′ and c = c′. The upper right
entry of the matrix equation then becomes ak + b = b′ (where k is the
upper right entry of M). Since both b and b′ satisfy 0 ≤b < a, this forces
k = 0, so M is the identity.
To complete the proof, we need to check that the subgroups of π1(T2, q)
induced by the covering maps (a), (b), (c) are exactly those corresponding
to (i), (ii), (iii), respectively.
Case (a) is obvious, since the fundamental group of R2 is trivial.

288
12. Classiﬁcation of Coverings
For (b), note that the fundamental group of S1 × R is inﬁnite cyclic,
generated by the path class of the loop c(t) = (α(t), 0). The image of
this loop under p is p ◦c(t) = (α(t)a, α(t)b), which represents the element
βaγb ∈π1(T2, q). Under our isomorphism with Z2, this corresponds to (a, b)
and generates the inﬁnite cyclic group described in (ii).
For (c), it is easy to check that p carries the generators β and γ of
π1(T2, q) to βa and βbγc. Under our isomorphism with Z2, the subgroup
generated by these elements is exactly the one described in (iii).

Problems
289
Problems
12-1. Let E be the following subset of R3 × R3:
E = {(x, y) ∈R3 × R3 : x ̸= y}.
Deﬁne an equivalence relation in E by setting (x, y) ∼(y, x) for all
(x, y) ∈E. Compute the fundamental group of E/∼.
12-2. Let M = T2 # T2.
(a) Show that the fundamental group of M has a subgroup of index
2.
(b) Prove that there exists a manifold 
M and a two-sheeted covering
map p: 
M →M.
12-3. Consider the map f : S1 →T2 given by
f(z) = (z2, 1).
For which coverings p: 
X →T2 can f be lifted to 
X?
12-4. Consider the action of Z on Rm ∖{0} deﬁned by n · x = 2nx.
(a) Show that Z acts continuously, freely, and properly.
(b) Show that the orbit space (Rm ∖{0})/Z is homeomorphic to
Sm−1 × S1.
(c) If m ≥3, show that the universal covering space of Sm−1 × S1
is homeomorphic to Rm ∖{0}.
12-5. Identify a group Γ of homeomorphisms of the plane, generated by
translations and reﬂections, such that R2/Γ is homeomorphic to the
Klein bottle.
12-6. Show that any continuous action of a ﬁnite group on a manifold is
proper.
12-7. For any integers a, b, c, d such that ad −bc ̸= 0, show that the map
p : S1 × R →T2 given by p(z, y) = (zaε(y)b, zcε(y)d) is a covering
map. [Hint: Using a commutative diagram similar to (12.2), show
that p is an open map and a continuous homomorphism with discrete
kernel.]
12-8. Prove the triangle inequality for the hyperbolic metric as follows.
Show that it suﬃces to assume that one of the points is the origin,

290
12. Classiﬁcation of Coverings
and use the identity cosh2 x −sinh2 x = 1 to show that sinh d(z, 0) =
2|z|/(1 −|z|2), and therefore by the Euclidean triangle inequality,
cosh d(z1, z2) ≤cosh d(z1, 0) cosh d(z2, 0) + sinh d(z1, 0) sinh d(z2, 0)
= cosh(d(z1, 0) + d(0, z2)).
12-9. Let G be a connected, locally simply connected, locally compact
Hausdorﬀtopological group, and let G be its universal covering space.
Show that G has a unique group structure such that it is a topological
group and such that the covering map p: G →G is a homomorphism
with discrete kernel.

13
Homology
In addition to the fundamental group and the higher homotopy groups,
there are other groups that can be attached to a topological space in a
way that is topologically invariant. To motivate them, let us look again
at the fundamental group. Using the device of circle representatives as
described in Chapter 7, we can think of the fundamental group of a space
X as equivalence classes of maps from the circle into X modulo those that
extend to the disk. Roughly, the idea of homology theory is to divide out
by a somewhat larger equivalence relation, consisting of those maps that
extend to a map into X from any surface whose boundary is the circle.
To see how this can lead to diﬀerent results, let X = T2 # T2 be the
two-holed torus, and consider the loop f in X pictured in Figure 13.1. (It
goes once around the boundary of the disk that is removed to form the
connected sum.) In terms of our standard generators for π1(X), this loop
is path homotopic to either α1β1α−1
1 β−1
1
or β2α2β−1
2 α−1
2 , so it is not null
f
FIGURE 13.1. A loop that extends to a surface map.

292
13. Homology
homotopic, and its circle representative has no extension to a map from the
closed disk into X. However, it is easy to see that the circle representative
does extend to a map from T2 minus a disk into X—for example, the
inclusion map of the left half of X is such an extension.
It turns out that a more satisfactory theory results if instead of con-
sidering loops modulo those that extend to maps from a 2-manifold with
boundary, we consider instead formal sums of maps from a 1-simplex mod-
ulo those that are “boundaries” of sums of maps from a 2-simplex. Getting
the deﬁnitions correct requires some care, and it is easy to lose sight of the
geometric meaning among the technical details, but it will help if you keep
the above example in mind throughout the discussion. The reward is a the-
ory that extends easily to higher dimensions, is computationally tractable,
and will allow us to prove a number of signiﬁcant facts about manifolds
that are much more diﬃcult or even impossible to prove using homotopy
groups alone.
We begin the chapter by deﬁning a sequence of abelian groups attached to
each topological space, called its singular homology groups, which formalize
the intuitive discussion above. It follows immediately from the deﬁnition
that these groups are topological invariants, and with a bit more work we
show they are also homotopy invariants. Next we prove that there is a
simple relationship between the ﬁrst homology group H1(X) and the fun-
damental group, namely that H1(X) is naturally isomorphic to the abelian-
ization of π1(X). Then we introduce one of the main tools for computing
homology groups, the Mayer–Vietoris theorem, which is a homology ana-
logue of the Seifert–Van Kampen theorem. Using these tools, we compute
the homology groups of most of the spaces we have studied so far. We then
describe some applications of homology: to the topological invariance of
the dimension of a manifold, the existence of vector ﬁelds on spheres, and
(using a diﬀerent homology theory called simplicial homology) the topo-
logical invariance of the Euler characteristic of a polyhedron. In the ﬁnal
section we give a brief introduction to cohomology.
Singular Homology Groups
We begin with some deﬁnitions. For any integer p ≥0, let Δp ⊂Rp denote
the Euclidean simplex ⟨e0, e1, . . . , ep⟩, where e0 = 0 and, for 1 ≤i ≤p,
ei = (0, . . . , 1, . . . , 0) is the vector with a 1 in the ith place and zeros
elsewhere. We call Δp the standard p-simplex. If X is a topological space,
a singular p-simplex in X is a continuous map σ: Δp →X. For example,
a singular 0-simplex is just a map from the one-point space Δ0 into X,
which we may identify with a point in X; and a singular 1-simplex is a
map from Δ1 = [0, 1] ⊂R into X, which is just a path in X. (A map is
generally called “singular” if it fails to have some desirable property such

Singular Homology Groups
293
as continuity or diﬀerentiability. In this case, the term singular is meant
to reﬂect the fact that σ need not be an embedding, so its image may not
look at all like a simplex.)
Let Cp(X) denote the free abelian group generated by the set of all
singular p-simplices in X. An element of Cp(X), which can be written as a
formal linear combination of singular simplices with integer coeﬃcients, is
called a singular p-chain in X, and the group Cp(X) is called the singular
chain group in dimension p.
There are some special singular simplices in Euclidean spaces that we
will use frequently. Let K ⊂Rn be a convex subset. For any p + 1 points
v0, . . . , vp ∈K (not necessarily in general position or even distinct), let
α(v0, . . . , vp): Δp →Rn denote the restriction of the unique aﬃne map
that takes ei to vi for i = 0, . . . , p. By convexity, the image lies in K,
so this is a singular p-simplex in K, called an aﬃne singular simplex. A
singular chain in which every singular simplex that appears is aﬃne will
be called an aﬃne chain.
The point of homology theory is to use singular chains to detect “holes.”
The intuition is that any chain that closes up on itself (like a closed path)
but is not equal to the “boundary value” of a chain of one higher dimension
must surround a hole in X. To this end, we deﬁne a homomorphism from
p-chains to (p −1)-chains that precisely captures the notion of boundary
values.
For each i = 0, . . . , p, let Fi,p : Δp−1 →Δp be the aﬃne singular simplex
Fi,p = α(e0, . . . , ei, . . . , ep),
where the hat indicates that ei is to be omitted. More speciﬁcally, Fi,p is
the aﬃne map that sends
e0

→
e0
. . .
. . .
ei−1

→
ei−1
ei

→
ei+1
. . .
. . .
ep−1

→
ep
and therefore maps Δp−1 homeomorphically onto the boundary face of Δp
opposite the vertex ei. We call Fi,p the ith face map in dimension p.
For any singular simplex σ: Δp →X, deﬁne a (p −1)-chain ∂σ called
the boundary of σ by
∂σ =
p

i=0
(−1)iσ ◦Fi,p.
By the characteristic property of free abelian groups, this extends uniquely
to a homomorphism ∂: Cp(X) →Cp−1(X), called the boundary operator.

294
13. Homology
Δ2
X
σ
+
+
−
FIGURE 13.2. The boundary of a singular 2-simplex.
We sometimes indicate which chain group the boundary operator is acting
on by a subscript, as in ∂p : Cp(X) →Cp−1(X). The boundary of any
0-chain is deﬁned to be zero.
A p-chain c is called a cycle if ∂c = 0, and it is called a boundary if
there exists a (p + 1)-chain b such that c = ∂b. The set Zp(X) of p-cycles
is a subgroup of Cp(X), because it is the kernel of the homomorphism ∂p.
Similarly, the set Bp(X) of p-boundaries is also a subgroup (the image of
∂p+1).
It might help clarify what is going on to work out some simple exam-
ples. When thinking about these examples, you should note the similarity
between the formula for ∂σ and the induced orientation on the boundary
faces of a simplex, discussed in Chapter 5.
A singular 1-simplex is just a path σ: I →X, and ∂σ is the formal
diﬀerence σ(1)−σ(0). Therefore, a 1-cycle is a formal sum of paths with the
property that the set of initial points counted with multiplicities is exactly
the same as the set of terminal points with multiplicities. A typical example
is a sum of paths k
i=1 σi such that σi(1) = σi+1(0) and σk(1) = σ1(0).
Apart from notation, this is pretty much the same thing as a product of
paths (in the sense in which we used the term in Chapter 7) such that the
last path ends where the ﬁrst one starts (hence the term “cycle”). The only
real diﬀerence is that chains do not keep track of the order in which the
paths appear.
The boundary of a singular 2-simplex σ: Δ2 →X is a sum of three paths
with signs (Figure 13.2). Think of this as a cycle in X that traverses the
boundary values of σ in the counterclockwise direction. (Intuitively, you
can think of a path with a negative sign as representing the same path
going in the opposite direction; although they are not really the same, we
will see below that they diﬀer by a boundary, so they are equivalent from
the point of view of homology.)
The most important feature of the singular boundary map is that “the
boundary of a boundary is zero,” as the next lemma shows.
Lemma 13.1. For any singular chain c, ∂(∂c) = 0.

Singular Homology Groups
295
Proof. Since each chain group Cp(X) is generated by singular simplices, it
suﬃces to show this in the case in which c = σ is a singular p-simplex.
First we note that the face maps satisfy the commutation relation
Fi,p ◦Fj,p−1 = Fj,p ◦Fi−1,p−1
when i > j,
(13.1)
as can be seen immediately by observing that the vertices of Δp−2 are
mapped according to the following chart:
Fj,p−1
Fi,p
e0

→
e0

→
e0
. . .
. . .
. . .
ej−1

→
ej−1

→
ej−1
ej

→
ej+1

→
ej+1
. . .
. . .
. . .
ei−2

→
ei−1

→
ei−1
ei−1

→
ei

→
ei+1
. . .
. . .
. . .
ep−2

→
ep−1

→
ep.
Fi−1,p−1
Fj,p
e0

→
e0

→
e0
. . .
. . .
. . .
ej−1

→
ej−1

→
ej−1
ej

→
ej

→
ej+1
. . .
. . .
. . .
ei−2

→
ei−2

→
ei−1
ei−1

→
ei

→
ei+1
. . .
. . .
. . .
ep−2

→
ep−1

→
ep.
In other words, both compositions are equal to the aﬃne simplex
α(e0, . . . , ej, . . . , ei, . . . , ep). Using this, we compute
∂(∂σ) =
p−1

j=0
p

i=0
(−1)i+jσ ◦Fi,p ◦Fj,p−1
=

0≤j<i≤p
(−1)i+jσ ◦Fi,p ◦Fj,p−1
+

0≤i≤j≤p−1
(−1)i+jσ ◦Fi,p ◦Fj,p−1.
Making the substitutions i = j′, j = i′ −1 into the second sum and using
(13.1), we see that the sums cancel term by term.
Because of the preceding lemma, the group Bp(X) of p-boundaries is a
subgroup of the group Zp(X) of p-cycles. The pth singular homology group
of X is deﬁned to be the quotient group
Hp(X) = Zp(X)/Bp(X) = Ker ∂p/ Im ∂p+1.
It is zero if and only if every p-cycle is the boundary of some (p + 1)-
chain, which you should interpret intuitively as meaning that there are no
p-dimensional “holes” in X. The equivalence class of a p-cycle c in Hp(X)
is denoted by [c], and is called its homology class. If two p-cycles determine
the same homology class (i.e., if they diﬀer by a boundary), they are said
to be homologous.

296
13. Homology
The signiﬁcance of the homology groups derives from the fact that they
are topological invariants. The proof is a very easy consequence of the
fact that continuous maps induce homology homomorphisms. We begin by
deﬁning homomorphisms on the chain groups.
Given a continuous map f : X →Y , let f# : Cp(X) →Cp(Y ) be the
homomorphism deﬁned by setting f#σ = f ◦σ for each singular p-simplex
σ. The key fact is that f# commutes with the boundary operators:
f#(∂σ) =
p

i=0
(−1)if ◦σ ◦Fi,p = ∂(f#σ).
Because of this, f# maps Zp(X) to Zp(Y ) and Bp(X) to Bp(Y ), and there-
fore passes to the quotient to deﬁne a homomorphism f∗: Hp(X) →Hp(Y ),
called the homomorphism induced by f.
Proposition 13.2 (Functorial Properties of Homology). Let X, Y ,
and Z be topological spaces.
(a) The homomorphism (IdX)∗: Hp(X) →Hp(X) induced by the identity
map of X is the identity of Hp(X).
(b) If f : X →Y and g: Y →Z are continuous maps, then (g ◦f)∗=
g∗◦f∗: Hp(X) →Hp(Z).
Thus the pth singular homology group deﬁnes a covariant functor from the
category of topological spaces to the category of abelian groups.
Proof. It is trivial to check that both properties hold already for f#.
Corollary 13.3 (Topological Invariance of Singular Homology).
If f : X →Y is a homeomorphism, then f∗: Hp(X) →Hp(Y ) is an
isomorphism.
Exact Sequences and Chain Complexes
It is useful to look at the construction we just did in a somewhat more
algebraic way. A sequence of abelian groups and homomorphisms
· · · →Gp+1
αp+1
−−−→Gp
αp
−→Gp−1 →· · ·
is said to be exact if Im αp+1 = Ker αp for all p. For example, a 5-term
exact sequence of the form
0 →A
α
−→B
β−→C →0
is called a short exact sequence. (The maps on the ends are the zero homo-
morphisms.) Because the image of the zero homomorphism is {0}, exactness

Singular Homology Groups
297
at A means that α is injective, and similarly exactness at C means that β
is surjective. Exactness at B means that Ker β = α(A), and the ﬁrst iso-
morphism theorem then tells us that C ∼= B/α(A). A short exact sequence
is thus a graphic summary of the ﬁrst isomorphism theorem.
More generally, a sequence of abelian groups and homomorphisms
· · · →Cp+1
∂p+1
−−−→Cp
∂p
−→Cp−1 →· · ·
is called a chain complex if the composition of any two consecutive ho-
momorphisms is the zero map: ∂p ◦∂p+1 = 0. This is equivalent to the re-
quirement that Im ∂p+1 ⊂Ker ∂p. (The homomorphisms ∂p are often called
“boundary operators” by analogy with the case of singular homology.) We
will denote such a chain complex by C∗, with the boundary maps being
understood from the context. In many applications (such as the singular
chain groups), Cp is deﬁned only for p ≥0, but it is sometimes conve-
nient to extend this to all p by deﬁning Cp to be the trivial group and the
associated homomorphisms to be zero for p < 0.
The pth homology group of the chain complex C∗is
Hp(C∗) = Ker ∂p/ Im ∂p+1.
Clearly, the chain complex is exact if and only if Hp(C∗) = 0 for all p; thus
the homology groups provide a precise quantitative measurement of how
the complex fails to be exact.
Now suppose C∗and D∗are chain complexes. A chain map F : C∗→D∗
is a collection of homomorphisms F : Cp →Dp (we could distinguish them
with subscripts, but there is no need) such that ∂p ◦F = F ◦∂p for all p:
· · ·
-
· · ·
-
Dp
Dp−1
-
∂p
Cp
Cp−1
-
∂p
?
F
?
F
· · · .
-
· · ·
-
For example, the homomorphisms f# : Cp(X) →Cp(Y ) constructed above
from a continuous map f deﬁne a chain map from the singular chain com-
plex of X to that of Y . Any chain map takes Ker ∂to Ker ∂and Im ∂
to Im ∂, and therefore induces a homology homomorphism F∗: Hp(C∗) →
Hp(D∗) for each p.
The study of exact sequences, chain complexes, and homology is part of
the subject known as homological algebra. It began as a branch of topology,
but has acquired a life of its own as a branch of algebra. We will return to
these ideas brieﬂy later in this chapter.

298
13. Homology
Elementary Computations
Although the deﬁnition of the singular homology groups may seem less
intuitive than that of the fundamental group and the higher homotopy
groups, the homology groups oﬀer a number of advantages. For example,
they are all abelian, which circumvents some of the thorny computational
problems that beset the fundamental group. Also, there is no need to choose
a base point, so unlike the homotopy groups, homology groups give us
information about all the path components of a space, as the following
lemma shows.
Lemma 13.4. Let X be a space, let {Xα}α∈A be the set of path compo-
nents of X, and let ια : Xα 	→X be inclusion. Then for each p ≥0 the
maps (ια)∗: Hp(Xα) →Hp(X) induce an isomorphism
#
α∈A
Hp(Xα) →Hp(X).
Proof. Since the image of any singular simplex must lie entirely in one
path component, it is clear that the chain maps (ια)# : Cp(Xα) →Cp(X)
already induce isomorphisms
#
α∈A
Cp(Xα) →Cp(X).
The result for homology follows easily from this.
As in the case of the fundamental group, the deﬁnition of the homology
groups does not give us much insight into how to compute them in general,
because it involves taking quotients of huge groups by huge subgroups.
There are, however, two simple cases that we can compute directly right
now: the zero-dimensional homology groups of all spaces and all the homol-
ogy groups of a one-point space. In the rest of this chapter we will develop
some powerful tools for computing the rest of the homology groups.
Proposition 13.5 (Zero-Dimensional Homology).
For any topolog-
ical space X, H0(X) is a free abelian group with basis consisting of an
arbitrary point in each path component.
Proof. It suﬃces to show that H0(X) is the inﬁnite cyclic group generated
by the class of any point when X is path connected, for then in the general
case Lemma 13.4 guarantees that H0(X) is the direct sum of inﬁnite cyclic
groups, one for each path component.
A singular 0-chain is a formal linear combination of points in X with
integer coeﬃcients: c = m
i=1 nixi. Because the boundary operator is the
zero map in dimension 0, every 0-chain is a cycle.

Singular Homology Groups
299
Assume that X is path connected, and deﬁne a map ε: C0(X) →Z by
ε
 m

i=1
nixi

=
m

i=1
ni.
It is clear that ε is a surjective homomorphism. We will show that
Ker ε = B0(X), from which it follows by the ﬁrst isomorphism theorem
that ε induces an isomorphism H0(X) →Z. Since ε takes any single point
to 1, the result follows.
If σ is a singular 1-simplex, then ∂σ = σ(1)−σ(0), so ε(∂σ) = 1−1 = 0.
Therefore, B0(X) ⊂Ker ε.
To show that Ker ε ⊂B0(X), choose any point x0 ∈X, and for each
x ∈X let α(x) be a path from x0 to x. This is a singular 1-simplex whose
boundary is the 0-chain x −x0. Thus, for an arbitrary 0-chain c = 
i nixi
we compute
∂

i
niα(xi)

=

i
nixi −

i
nix0 = c −ε(c)x0.
In particular, if ε(c) = 0, then c ∈B0(X).
Proposition 13.6 (Homology of a One-Point Space).
Let ∗be a
one-point space. The singular homology groups of ∗are
Hp(∗) ∼=

Z
if p = 0,
0
if p > 0.
(13.2)
Proof. The case p = 0 follows from the preceding proposition, so we con-
centrate on p > 0. There is exactly one singular simplex in each dimension,
namely the constant map σp : Δp →∗, so each chain group Cp(∗) is the
inﬁnite cyclic group generated by σp. For p > 0, the boundary of σp is the
alternating sum
∂σp =
p

i=0
(−1)iσp ◦Fi,p =
p

i=0
(−1)iσp−1 =

0
if p is odd,
σp−1
if p is even.
Thus ∂: Cp(∗) →Cp−1(∗) is an isomorphism when p is even and positive,
and the zero map when p is odd:
· · ·
∼
=
−→C3(∗)
0−→C2(∗)
∼
=
−→C1(∗)
0−→C0(∗) →0.
It follows that for p > 0,
Zp(∗) =

Cp(∗)
if p is odd,
0
if p is even;
Bp(∗) =

Cp(∗)
if p is odd,
0
if p is even.

300
13. Homology
X
X × I
Y
H
ι0
ι1
f0
f1
FIGURE 13.3. The setup for Theorem 13.7.
Taking quotients, we ﬁnd that Hp(∗) = 0.
[[Homotopy]] Invariance
Just like the fundamental group, the singular homology groups are also
homotopy invariant. The proof, as in the case of the fundamental group,
depends on the fact that homotopic maps induce the same homology ho-
momorphism.
Theorem 13.7. If f0, f1 : X →Y are homotopic maps, then for each p ≥
0 the induced homomorphisms (f0)∗, (f1)∗: Hp(X) →Hp(Y ) are equal.
Before proving this theorem, we state its most important corollary.
Corollary 13.8 ([[Homotopy]] Invariance of Singular Homology).
If
f : X →Y is a homotopy equivalence, then for each p ≥0, f∗: Hp(X) →
Hp(Y ) is an isomorphism.
Exercise 13.1.
Prove Corollary 13.8.
Proof of Theorem 13.7. We begin by considering the special case in which
Y = X × I and fi = ιi, where ι0, ι1 : X →X × I are the maps
ι0(x) = (x, 0),
ι1(x) = (x, 1).
(See Figure 13.3.) Clearly, ι0 ≃ι1. We will show below that (ι0)∗= (ι1)∗. As
it turns out, this immediately implies the general case as follows. Suppose
f0, f1 : X →Y are continuous maps and H : X × I →Y is a homotopy
from f0 to f1 (Figure 13.3). Then since H ◦ιi = fi, we have
(f0)∗= (H ◦ι0)∗= H∗◦(ι0)∗= H∗◦(ι1)∗= (H ◦ι1)∗= (f1)∗.

[[Homotopy]] Invariance
301
To prove (ι0)∗= (ι1)∗, it would suﬃce to show that (ι0)#c and (ι1)#c
diﬀer by a boundary for each chain c. In fact, a little experimentation will
probably convince you that this is usually false. But in fact all we need is
that they diﬀer by a boundary when c is a cycle. So we might try to deﬁne
a map h: Zp(X) →Cp+1(X × I) such that
∂h(c) = (ι1)#c −(ι0)#c.
(13.3)
It turns out to be hard to deﬁne such a thing for cycles only. Instead, we
will deﬁne h(c) for all p-chains c, and show that it satisﬁes a formula that
implies (13.3) when c is a cycle.
For each p ≥0, we will deﬁne a homomorphism h: Cp(X) →Cp+1(X×I)
that satisﬁes the following identity:
h ◦∂+ ∂◦h = (ι1)# −(ι0)#.
(13.4)
From (13.4) it follows immediately that (ι1)#c −(ι0)#c = ∂h(c) whenever
∂c = 0, and therefore (ι1)∗[c] = (ι0)∗[c].
The construction of h is basically a “triangulated” version of the obvious
homotopy from ι0 to ι1. Consider the convex set Δp × I ⊂Rp+1 = Rp × R.
Note that Δp × {0} and Δp × {1} are Euclidean p-simplices in Rp+1. Let
us denote the vertices of Δp × {0} by Ei = (ei, 0) and those of Δp × {1} by
E′
i = (ei, 1). For 0 ≤i ≤p, let Gi,p : Δp →Δp × I be the following aﬃne
singular (p + 1)-simplex in Rp+1:
Gi,p = α(E0, . . . , Ei, E′
i, . . . , E′
p).
Then deﬁne h: Cp(X) →Cp+1(X × I) by
h(σ) =
p

i=0
(−1)i(σ × Id) ◦Gi,p.
Note that Gi,p takes its values in Δ × I and σ × Id is a map from Δ × I to
X × I, so this does indeed deﬁne a (p + 1)-chain in X × I.
To get an idea of what this means geometrically, consider the case p = 2.
The three simplices ⟨E0, E′
0, E′
1, E′
2⟩, ⟨E0, E1, E′
1, E′
2⟩, and ⟨E0, E1, E2, E′
2⟩
give a triangulation of Δ2 × I (see Figure 13.4). In the special case in
which σ is the identity map of Δ2, h(σ) is a sum of aﬃne singular simplices
mapping Δ3 homeomorphically onto each one of these 3-simplices, with
signs chosen to correspond to the natural orientation on each simplex. In
the general case, h(σ) is this singular chain followed by the map σ × Id,
and thus is a chain in X × I whose image is the product set σ(Δ2) × I.
Now we need to prove that h satisﬁes (13.4). For this purpose, we will
need some relations between the aﬃne simplices Gi,p and the face maps
Fj,p. First, if 1 ≤j ≤p, note that Gj,p and Gj−1,p agree on all the vertices

302
13. Homology
E0
E1
E2
E′
1
E′
2
E′
0
Δ3
Gi,2
X × I
σ × Id
Δ2 × I
FIGURE 13.4. The operator h in dimension 2.
of Δp except ej. Because Fj,p+1 skips ej, the compositions Gj,p ◦Fj,p+1
and Gj−1,p ◦Fj,p+1 are equal. In fact, it is straightforward to check that
Gj,p ◦Fj,p+1 = Gj−1,p ◦Fj,p+1 = α(E0, . . . , Ej−1, E′
j, . . . , E′
p).
(13.5)
Similarly, by following what each map does to basis elements as we did in
the proof of Lemma 13.1, one can compute that
(Fj,p × Id) ◦Gi,p−1 =

Gi+1,p ◦Fj,p+1
if i ≥j,
Gi,p ◦Fj+1,p+1
if i < j.
(13.6)
Let σ be an arbitrary singular p-simplex in X. Using (13.6), we compute
h(∂σ) = h
p

j=0
(−1)jσ ◦Fj,p
=
p−1

i=0
p

j=0
(−1)i+j
(σ ◦Fj,p) × Id

◦Gi,p−1
=
p−1

i=0
p

j=0
(−1)i+j(σ × Id) ◦(Fj,p × Id) ◦Gi,p−1
=

0≤j≤i≤p−1
(−1)i+j(σ × Id) ◦Gi+1,p ◦Fj,p+1
+

0≤i<j≤p
(−1)i+j(σ × Id) ◦Gi,p ◦Fj+1,p+1.
(13.7)

[[Homotopy]] Invariance
303
On the other hand,
∂h(σ) = ∂
p

i=0
(−1)i(σ × Id) ◦Gi,p
=
p+1

j=0
p

i=0
(−1)i+j(σ × Id) ◦Gi,p ◦Fj,p+1.
Separating the terms where i < j −1, i = j −1, i = j, and i > j, this
becomes
∂h(σ) =

0≤i<j−1<j≤p+1
(−1)i+j(σ × Id) ◦Gi,p ◦Fj,p+1
−

1≤j≤p+1
(σ × Id) ◦Gj−1,p ◦Fj,p+1
+

0≤j≤p
(σ × Id) ◦Gj,p ◦Fj,p+1
+

0≤j<i≤p
(−1)i+j(σ × Id) ◦Gi,p ◦Fj,p+1.
Making the index substitutions j = j′ + 1 in the ﬁrst sum and i = i′ + 1
in the last, we see that these two sums exactly cancel those in (13.7). By
virtue of (13.5), all the terms in the middle two sums cancel except those
where j = 0 and j = p + 1. These two terms yield
h(∂σ) + ∂h(σ) = −(σ × Id) ◦α(E0, . . . , Ep) + (σ × Id) ◦α(E′
0, . . . , E′
p)
= −(ι0)#σ + (ι1)#σ.
This completes the proof.
As an immediate application, we can conclude that contractible spaces
have trivial homology in all dimensions greater than zero. (It is inﬁnite
cyclic in dimension zero by Proposition 13.5.)
Corollary 13.9. Suppose X is a contractible space. Then Hp(X) = 0 for
all p > 0.
There is an abstract algebraic version of what we just did. Suppose
F, G: C∗→D∗are chain maps. A collection of homomorphisms h: Cp →
Dp+1 is called a chain homotopy from F to G if the following identity is
satisﬁed on each group Cp:
h ◦∂+ ∂◦h = G −F.
If there exists such a map, F and G are said to be chain homotopic.
Exercise 13.2.
If F, G: C∗→D∗are chain homotopic chain maps, show
that F∗= G∗: Hp(C∗) →Hp(D∗) for all p.

304
13. Homology
f0
f0
f0
f1
f1
f1
p
p
p
q
q
q
b
H
σ
X
FIGURE 13.5. Path homotopic paths diﬀer by a boundary.
Homology and the Fundamental Group
In this section we show that there is a simple relationship between the
ﬁrst homology group of a path connected space and its fundamental group:
The former is just the abelianization of the latter. This will enable us to
compute the ﬁrst homology groups of all the spaces whose fundamental
groups we know.
We begin by deﬁning a map from the fundamental group to the ﬁrst
homology group. Let X be a space and q any point in X. A loop f based at q
is also a singular 1-simplex. In fact, it is a cycle, since ∂f = f(1)−f(0) = 0.
Therefore, any loop determines a 1-homology class. The following lemma
shows that the resulting class depends only on the path homotopy class of
f.
Lemma 13.10. Suppose f0 and f1 are paths in X, and f0 ∼f1. Then,
considered as a singular chain, f0 −f1 is a boundary.
Proof. We must show there is a singular 2-chain whose boundary is the
1-chain f0 −f1. Let H : f0 ∼f1, and let b: I × I →Δ2 be the map
b(x, y) = (x −xy, xy),
(13.8)
which maps the square onto the triangle by sending each horizontal line
segment linearly to a radial line segment (Figure 13.5). Then b is a quotient
map by the closed map lemma, and identiﬁes the left-hand edge of the
square to the origin. Since H respects the identiﬁcations made by b, it
passes to the quotient to yield a continuous map σ: Δ2 →X, i.e., a singular
2-simplex. From the deﬁnition of the boundary operator, ∂σ = cq −f1 +f0,

Homology and the Fundamental Group
305
f
f
f
q
q
p
p
σ
FIGURE 13.6. Proof that [f −1]H = −[f]H.
where q = f0(1). Since cq is the boundary of the constant 2-simplex that
maps Δ2 to q, it follows that f0 −f1 is a boundary.
In this section, because we will be dealing with various equivalence re-
lations on paths, we adopt the following notation. For any path in X (not
necessarily a loop), we let [f]π denote its equivalence class modulo path
homotopy. In particular, if f is a loop based at q, then [f]π is its path class
in π1(X, q). Similarly, if c is any 1-chain we let [c]H denote its equivalence
class modulo B1(X), so if c is a cycle (a loop for example), then [c]H is an
element of H1(X). Deﬁne a map γ : π1(X, q) →H1(X), which we will call
the Poincar´e homomorphism, by
γ([f]π) = [f]H.
By Lemma 13.10, γ is well-deﬁned.
Theorem 13.11. Let X be a path connected space and q ∈X. Then
γ : π1(X, q) →H1(X) is a surjective homomorphism whose kernel is the
commutator subgroup of π1(X, q). Consequently, H1(X) is isomorphic to
the abelianization of π1(X, q).
Proof. We begin by showing that [f −1]H = −[f]H for any path f in X. To
see this, deﬁne a singular 2-simplex σ: Δ2 →X by σ(x, y) = f(x) (Figure
13.6). Then ∂σ = f −1 −cq + f, where q = f(0). Since cq is a boundary, it
follows that the 1-chains f −1 and −f diﬀer by a boundary.
Next we show that γ is a homomorphism. Somewhat more generally, we
will show that [f · g]H = [f]H + [g]H for any two paths f, g such that
f(1) = g(0). When applied to loops f and g based at q, this implies that γ
is a homomorphism.
Given such paths f and g, deﬁne a singular 2-simplex σ: Δ2 →X by
σ(x, y) =

f(y −x + 1)
if y ≤x,
g(y −x)
if y ≥x.

306
13. Homology
f
f
g
g
σ
f · g
FIGURE 13.7. Proof that γ is a homomorphism.
(See Figure 13.7.) This is constant on each line segment y −x = constant,
and is continuous by the gluing lemma. It is easy to check that its boundary
is the 1-chain (f · g) −g + f −1, from which it follows that
[f · g]H = [g]H −[f −1]H = [g]H + [f]H.
Thus γ is a homomorphism.
Next we need to show that γ is surjective. For each point x ∈X, let α(x)
be a speciﬁc path from q to x, with α(q) chosen to be the constant path cq.
Since each path α(x) is in particular a 1-chain, the map x 
→α(x) extends
uniquely to a group homomorphism α: C0(X) →C1(X). For any path σ
in X, deﬁne a loop σ based at q by
σ = α(σ(0)) · σ · α(σ(1))−1.
Observe that
γ([σ]π) = [α(σ(0)) · σ · α(σ(1))−1]H
= [α(σ(0))]H + [σ]H −[α(σ(1))]H
= [σ]H −[α(∂σ)]H.
(13.9)
Now suppose c = m
i=1 niσi is an arbitrary 1-chain. Let f be the loop
f = (σ1)n1 · · · · · (σm)nm.
From (13.9) and the fact that γ is a homomorphism it follows that
γ([f]π) =
m

i=1
ni

[σi]H −[α(∂σi)]H

= [c]H −[α(∂c)]H.

Homology and the Fundamental Group
307
e0
e1
e2
α(v0)
α(v1)
α(v2)
q
v0
v1
v2
σ(0)
σ(1)
σ(2)
X
σ
FIGURE 13.8. Proof that Ker γ is the commutator subgroup.
In particular, if c is a cycle, then γ([f]π) = [c]H, which shows that γ is
surjective.
Because H1(X) is an abelian group, Ker γ clearly contains the commu-
tator subgroup [π1(X, q), π1(X, q)]. All that remains is to show that the
commutator subgroup is the entire kernel.
Let Π denote the abelianized fundamental group of X, and for any loop
f based at q let [f]Π denote the equivalence class of [f]π in Π. Because
the product in Π is induced by path multiplication, we will indicate it
with a dot and write it multiplicatively even though Π is abelian. For any
singular 1-simplex σ, let β(σ) = [σ]Π ∈Π. Because Π is abelian, this
extends uniquely to a homomorphism β : C1(X) →Π. We will show that
β takes all 1-boundaries to the identity element of Π.
Let σ be an arbitrary singular 2-simplex. Write vi = σ(ei) and σ(i) =
σ◦Fi,2, so that ∂σ = σ(0) −σ(1) +σ(2) (see Figure 13.8). Note that the loop
σ(0) · (σ(1))−1 · σ(2) is path homotopic to the constant loop cv1. (This can
be seen either by identifying Δ2 with the closed disk via a homeomorphism
and noting that σ provides an extension of the circle representative of σ(0)·
(σ(1))−1 · σ(2) to the disk; or by applying Lemma 7.12 to the composition
σ ◦b, where b: I × I →Δ2 is given by (13.8).) We compute
β(∂σ) = [σ(0)]Π ·

[σ(1)]Π

−1 · [σ(2)]Π
= [σ(0) · (σ(1))−1 · σ(2)]Π
= [α(v1) · σ(0) · α(v2)−1 · α(v2) · (σ(1))−1 · α(v0)−1
· α(v0) · σ(2) · α(v1)−1]Π
= [α(v1) · σ(0) · (σ(1))−1 · σ(2) · α(v1)−1]Π
= [α(v1) · cv1 · α(v1)−1]Π
= [cq]Π,

308
13. Homology
which proves that B1(X) ⊂Ker β.
Now suppose f is a loop such that [f]π ∈Ker γ. This means that [f]H =
0, or equivalently that the singular 1-chain f is a boundary. On the one
hand, because f is a loop based at q, β(f) = [ f]Π = [f]Π. On the other
hand, since β takes boundaries to the identity element of Π, it follows that
[f]Π = 1, or equivalently that [f]π is in the commutator subgroup.
Corollary 13.12. The following spaces have the indicated ﬁrst homology
groups.
H1(S1) ∼= Z;
H1(Sn) = 0
if n ≥2;
H1(T2 # · · · # T2

 !
"
n
) ∼= Z2n;
H1(P2 # · · · # P2

 !
"
n
) ∼= Zn−1 × Z/⟨2⟩.
The Poincar´e homomorphism γ : π1(X, q) →H1(X) can be generalized
easily to a homomorphism from πk(X, q) to Hk(X) for any k, called the
Hurewicz homomorphism. The relationship between the higher homotopy
and homology groups is not so simple however, except in one important
special case: The Hurewicz theorem, proved by Witold Hurewicz in 1934,
says that if X is path connected and πj(X, q) is trivial for 1 ≤j < k, then
Hj(X) is trivial for the same values of j and the Hurewicz homomorphism
is an isomorphism between πk(X, q) and Hk(X). For a proof, see [Spa89]
or [Whi78].
The Mayer–Vietoris Theorem
Our main tool for computing higher-dimensional homology groups will be
a result analogous to the Seifert–Van Kampen theorem, in that it gives a
recipe for computing the homology groups of a space that is the union of
two open sets in terms of the homology of the two open sets and that of
their intersection.
Statement of the Theorem
The setup for the theorem is similar to that of the Seifert–Van Kampen
theorem: We are given a space X and two open subsets U, V ⊂X whose
union is X. (In this case, there is no requirement that any of the spaces be

The Mayer–Vietoris Theorem
309
path connected.) There are four inclusion maps
j@
@@
R
U
U ∩V
i



V
l



X,
k
@
@@
R
all of which induce homology homomorphisms.
Theorem 13.13 (Mayer–Vietoris).
Let X be a topological space, and
let U, V be open subsets of X whose union is X. Then for each p there
is a homomorphism ∂∗: Hp(X) →Hp−1(U ∩V ) such that the following
sequence is exact:
· · ·
∂∗
−→Hp(U ∩V )
i∗⊕j∗
−−−→Hp(U) ⊕Hp(V )
k∗−l∗
−−−−→Hp(X)
∂∗
−→Hp−1(U ∩V )
i∗⊕j∗
−−−→· · · .
(13.10)
The sequence (13.10) is called the Mayer–Vietoris sequence of the triple
(X, U, V ), and ∂∗is called the connecting homomorphism. The other maps
are the obvious ones: (i∗⊕j∗)[c] = (i∗[c], j∗[c]) and (k∗−l∗)([c], [c′]) =
k∗[c] −l∗[c′].
Before proving the theorem, let us apply it to an example to show how
it can be used to compute homology groups.
Proposition 13.14 (Homology Groups of Spheres).
For n ≥1, Sn
has the following singular homology groups:
Hp(Sn) ∼=
⎧
⎪
⎪
⎪
⎨
⎪
⎪
⎪
⎩
Z
if p = 0,
0
if 0 < p < n,
Z
if p = n,
0
if p > n.
Proof. We use the Mayer–Vietoris sequence as follows. Let N and S denote
the north and south poles, and let U = Sn ∖{N}, V = Sn ∖{S} as in
the proof that Sn is simply connected (Theorem 8.7). Part of the Mayer–
Vietoris sequence reads
Hp(U) ⊕Hp(V ) →Hp(Sn)
∂∗
−→Hp−1(U ∩V ) →Hp−1(U) ⊕Hp−1(V ).
Because U and V are contractible, when p > 1 this sequence reduces to
0 →Hp(Sn)
∂∗
−→Hp−1(U ∩V ) →0,

310
13. Homology
from which it follows that ∂∗is an isomorphism. Thus, since U ∩V is
homotopy equivalent to Sn−1,
Hp(Sn) ∼= Hp−1(U ∩V ) ∼= Hp−1(Sn−1)
for p > 1, n ≥1.
(13.11)
We will prove the proposition by induction on n. In the case n = 1,
H0(S1) ∼= H1(S1) ∼= Z by Proposition 13.5 and Corollary 13.12. For p > 1,
(13.11) shows that Hp(S1) ∼= Hp−1(S0). Since each component of S0 is
a one-point space, Hp−1(S0) is the trivial group by Proposition 13.6 and
Lemma 13.4.
Now let n > 1, and suppose the result is true for Sn−1. The cases p = 0
and p = 1 are again taken care of by Proposition 13.5 and Corollary 13.12.
For p > 1, (13.11) and the inductive hypothesis give
Hp(Sn) ∼= Hp−1(Sn−1) ∼=
⎧
⎪
⎨
⎪
⎩
0
if p < n,
Z
if p = n,
0
if p > n.
Proof of the Theorem
To prove the Mayer–Vietoris theorem, we need to introduce a few more
basic concepts from homological algebra.
Suppose C∗, D∗, and E∗are chain complexes. A sequence of chain maps
· · · →C∗
F
−→D∗
G
−→E∗→· · ·
is said to be exact if each of the sequences
· · · →Cp
F
−→Dp
G
−→Ep →· · ·
is exact.
The following lemma is a standard result in homological algebra. The
proof, which is easier to do than it is to read, uses a technique commonly
called “diagram chasing.” The best way to understand it is probably to
read the ﬁrst paragraph or two to get an idea of how the arguments go,
and then sit down with pencil and paper and carry out the rest yourself.
Lemma 13.15 (The Zigzag Lemma).
Let
0 →C∗
F
−→D∗
G
−→E∗→0
be a short exact sequence of chain maps. Then for each p there is a con-
necting homomorphism ∂∗: Hp(E∗) →Hp−1(C∗) such that the following
sequence is exact:
· · ·
∂∗
−→Hp(C∗)
F∗
−→Hp(D∗)
G∗
−−→Hp(E∗)
∂∗
−→Hp−1(C∗)
F∗
−→· · · . (13.12)

The Mayer–Vietoris Theorem
311
The sequence (13.12) is called the long exact homology sequence associ-
ated with the given short exact sequence of chain maps.
Proof. Consider the diagram
0
- Cp+1
-
F
Dp+1
Ep+1
-
G
0
-
?
∂
?
∂
?
∂
0
- Cp
-
F
Dp
Ep
-
G
0
-
?
∂
?
∂
?
∂
0
- Cp−1
-
F
Dp−1
Ep−1
-
G
0
-
?
∂
?
∂
?
∂
0
- Cp−2
-
F
Dp−2
Ep−2
-
G
0.
-
The hypothesis is that this diagram commutes and the horizontal rows are
exact.
We will use brackets to denote the homology class of a cycle in any of
these groups, so for example if dp ∈Dp satisﬁes ∂dp = 0, then [dp] ∈
Hp(D∗). To deﬁne the connecting homomorphism ∂∗, let [ep] ∈Hp(E∗) be
arbitrary. This means that ep ∈Ep and ∂ep = 0. Surjectivity of G: Dp →
Ep means that there is an element dp ∈Dp such that Gdp = ep, and
then commutativity of the diagram means that G∂dp = ∂Gdp = ∂ep = 0,
so ∂dp ∈Ker G. By exactness at Dp−1 there is an element cp−1 ∈Cp−1
such that Fcp−1 = ∂dp. Now, F∂cp−1 = ∂Fcp−1 = ∂∂dp = 0, and since
F is injective, ∂cp−1 = 0. Therefore, cp−1 represents a homology class in
Hp−1(C∗).
We wish to set ∂∗[ep] = [cp−1]. To do so, we have to make sure the
homology class of cp−1 does not depend on any of the choices we made
along the way. Another set of choices will be of the form e′
p ∈Ep such
that ep −e′
p = ∂ep+1, d′
p ∈Dp such that Gd′
p = e′
p, and c′
p−1 ∈Cp−1
such that Fc′
p−1 = ∂d′
p. Because G is surjective, there exists dp+1 ∈Dp+1
such that Gdp+1 = ep+1. Then G∂dp+1 = ∂Gdp+1 = ∂ep+1 = ep −e′
p, so
G(dp −d′
p) = ep −e′
p = G∂dp+1. Since dp −d′
p −∂dp+1 ∈Ker G, there
exists cp ∈Cp such that Fcp = dp −d′
p −∂dp+1. Now F∂cp = ∂Fcp =
∂(dp −d′
p −∂dp+1) = ∂dp −∂d′
p = Fcp−1 −Fc′
p−1. Since F is injective,
this implies ∂cp = cp−1 −c′
p−1, or [cp−1] = [c′
p−1]. To summarize, we have
deﬁned ∂∗[ep] = [cp−1], provided that there exists dp ∈Dp such that
Gdp = ep;
Fcp−1 = ∂dp.
To prove that ∂∗is a homomorphism, just note that if ∂∗[ep] = [cp−1]
and ∂∗[e′
p] = [c′
p−1], there exist dp, d′
p ∈Dp such that Gdp = ep, Gd′
p = e′
p,
Fcp−1 = ∂dp, Fc′
p−1 = ∂d′
p. It follows immediately that G(dp+d′
p) = ep+e′
p

312
13. Homology
and F(cp−1 + c′
p−1) = ∂(dp + d′
p), and so ∂∗[ep + e′
p] = [cp−1 + c′
p−1] =
∂∗[ep] + ∂∗[e′
p].
Now we have to prove exactness of (13.12). Let us start at Hp(C∗).
Suppose [cp] = ∂∗[ep+1]. Then looking back at the deﬁnition of ∂∗, there
is some dp+1 such that Fcp = ∂dp+1, so F∗[cp] = [Fcp] = [∂dp+1] = 0;
thus Im ∂∗⊂Ker F∗. Conversely, if F∗[cp] = [Fcp] = 0, there is some
dp+1 ∈Dp+1 such that Fcp = ∂dp+1, and then ∂Gdp+1 = G∂dp+1 =
GFcp = 0. In particular, this means ep+1 = Gdp+1 represents a homology
class in Hp+1(E∗), and threading through the deﬁnition of ∂∗we ﬁnd that
∂∗[ep+1] = [cp]. Thus Ker F∗⊂Im ∂∗.
Next we prove exactness at Hp(D∗). From GF = 0 it follows immediately
that G∗F∗= 0, so Im F∗⊂Ker G∗. If G∗[dp] = [Gdp] = 0, there exists
ep+1 ∈Ep+1 such that ∂ep+1 = Gdp. By surjectivity of G, there is some
dp+1 ∈Dp+1 such that Gdp+1 = ep+1, and then G∂dp+1 = ∂Gdp+1 =
∂ep+1 = Gdp. Thus dp −∂dp+1 ∈Ker G = Im F, so there is cp ∈Cp with
Fcp = dp −∂dp+1. Moreover, F∂cp = ∂Fcp = ∂(dp −∂dp+1) = ∂dp = 0, so
∂cp = 0 by injectivity of F. Thus cp represents a homology class in Hp(C∗),
and F∗[cp] = [Fcp] = [dp −∂dp+1] = [dp]. This proves that Ker G∗⊂Im F∗.
Finally, we prove exactness at Hp(E∗). Suppose [ep] ∈Im G∗. This means
that [ep] = G∗[dp] for some dp ∈Dp with ∂dp = 0, so ep = Gdp + ∂ep+1.
Replacing ep with ep−∂ep+1, we may assume Gdp = ep. Then by deﬁnition
∂∗[ep] = [cp−1], where cp−1 ∈Cp−1 is chosen so that Fcp−1 = ∂dp. But
in this case ∂dp = 0, so we may take cp−1 = 0 and therefore ∂∗[ep] = 0.
Conversely, suppose ∂∗[ep] = 0. This means that there exists dp ∈Dp such
that Gdp = ep and cp−1 ∈Cp−1 such that Fcp−1 = ∂dp, and cp−1 is a
boundary. Writing cp−1 = ∂cp, we ﬁnd that ∂Fcp = F∂cp = Fcp−1 = ∂dp.
Thus dp −Fcp represents a homology class, and G∗[dp −Fcp] = [Gdp −
GFcp] = [ep −0] = [ep]. Therefore, Ker ∂∗⊂Im G∗, and the proof is
complete.
The connecting homomorphism in the long exact homology sequence
satisﬁes an important naturality property, which we will use later in this
chapter.
Proposition 13.16 (Naturality of Connecting Homomorphisms).
Suppose
0
- C∗
-
F
D∗
E∗
-
G
0
-
?
κ
?
δ
?
ε
0
- C′
∗
-
F ′
D′
∗
E′
∗
-
G′
0
-
(13.13)

The Mayer–Vietoris Theorem
313
is a commutative diagram of chain maps in which the horizontal rows are
exact. Then the following diagram commutes for each p:
Hp(E′
∗)
Hp−1(C′
∗).
-
∂∗
Hp(E∗)
Hp−1(C∗)
-
∂∗
?
ε∗
?
κ∗
Proof. Let [ep] ∈Hp(E∗) be arbitrary. Then ∂∗[ep] = [cp−1], where
Fcp−1 = ∂dp for some dp such that Gdp = ep. Then by commutativity
of (13.13),
F ′(κcp−1) = δFcp−1 = δ∂dp = ∂(δdp);
G′(δdp) = εGdp = εep.
By deﬁnition, this means that
∂∗ε∗[ep] = ∂∗[εep] = [κcp−1] = κ∗[cp−1] = κ∗∂∗[ep],
which was to be proved.
While we are on the subject, here is another algebraic result whose proof
is a routine diagram chase.
Lemma 13.17 (The Five Lemma).
Suppose the horizontal rows are
exact in the following commutative diagram of abelian groups and homo-
morphisms:
A1
-
α1
A2
-
α2
A3
A4
-
α3
A5
-
α4
?
f1
?
f2
?
f3
?
f4
?
f5
B1
-
β1
B2
-
β2
B3
B4
-
β3
B5.
-
β4
If f1, f2, f4, and f5 are isomorphisms, then f3 is also.
Proof. We will prove that f3 is surjective, and leave the proof of injectivity
to you. Suppose b3 ∈B3 is arbitrary. By surjectivity of f4, there exists
a4 ∈A4 such that f4a4 = β3b3. By commutativity and exactness, f5α4a4 =
β4f4a4 = β4β3b3 = 0. Since f5 is injective, this means that α4a4 = 0, and by
exactness again there exists a3 ∈A3 such that a4 = α3a3. Substituting, we
obtain β3b3 = f4a4 = f4α3a3 = β3f3a3, which implies b3 −f3a3 ∈Ker β3 =
Im β2. Thus there exists b2 ∈B2 such that β2b2 = b3 −f3a3, and by
surjectivity of f2 there exists a2 ∈A2 such that b2 = f2a2. Summarizing, we
have b3−f3a3 = β2b2 = β2f2a2 = f3α2a2, which shows that b3 ∈Im f3.
Exercise 13.3.
Finish the proof of the ﬁve lemma by showing that f3 is
injective.

314
13. Homology
Proof of the Mayer–Vietoris theorem. Let X, U, and V be as in the state-
ment of the theorem. Consider the three chain complexes C∗(U ∩V ),
C∗(U)⊕C∗(V ), and C∗(X). (The boundary operator in the second complex
is ∂(c, c′) = (∂c, ∂c′).) We are interested in the following sequence of maps:
0 →Cp(U ∩V )
i#⊕j#
−−−−→Cp(U) ⊕Cp(V )
k#−l#
−−−−→Cp(X).
Because the chain maps i#, j#, k#, l# are all induced by inclusion, their
action is simply to consider a chain in one space as a chain in a bigger
space. It is easy to check that i# ⊕j# and k# −l# are chain maps and that
this sequence is exact, as far as it goes. For example, if c and c′ are chains
in U and V , respectively, such that k#c −l#c′ = 0, this means that they
are equal when thought of as chains in X. For this to be the case, the two
chains must be identical, and the image of each singular simplex in each
chain must actually lie in U ∩V . Thus c is actually a chain in U ∩V , and
(c, c′) = (i# ⊕j#)(c). The rest of the conditions for exactness are similar.
Unfortunately, however, k# −l# is not surjective. It is not hard to see
why: The image of this map is the set of all p-chains in X that can be
written as a sum of a chain in U plus a chain in V . Any singular p-simplex
whose image is not contained in either U or V therefore deﬁnes a chain
that is not in the image. Thus we cannot apply the zigzag lemma directly
to this sequence.
Instead, we use the following subterfuge: Let U denote the open cover
of X consisting of the sets U and V , and for each p let CU
p (X) denote the
subgroup of Cp(X) generated by singular simplices whose images lie either
entirely in U or entirely in V . The boundary operator carries CU
p (X) into
CU
p−1(X), so we get a new chain complex CU
∗(X). Clearly, the following
sequence is exact:
0 →C∗(U ∩V )
i#⊕j#
−−−−→C∗(U) ⊕C∗(V )
k#−l#
−−−−→CU
∗(X) →0.
The zigzag lemma then yields the following long exact homology sequence:
· · ·
∂∗
−→Hp(U ∩V )
i∗⊕j∗
−−−→Hp(U) ⊕Hp(V )
k∗−l∗
−−−−→HU
p (X)
∂∗
−→Hp−1(U ∩V )
i∗⊕j∗
−−−→· · · ,
(13.14)
where HU
p (X) is the pth homology group of the complex CU
∗(X). This is
almost what we are looking for. The ﬁnal step is to invoke Proposition 13.18
below, which shows that inclusion CU
∗(X) 	→C∗(X) induces a homology
isomorphism HU
p (X) ∼= Hp(X). Making this substitution into (13.14), we
obtain the Mayer–Vietoris sequence.
The missing step in the above proof is the fact that the singular homology
of X can be detected by looking only at singular simplices that lie either
in U or in V . More generally, suppose U is any open cover of X. A singular

The Mayer–Vietoris Theorem
315
chain c is said to be U-small if every singular simplex that appears in c has
image lying entirely in one of the open sets of U. Let CU
p (X) denote the
subgroup of Cp(X) consisting of U-small chains, and let HU
p (X) denote the
homology of the complex CU
∗(X).
Proposition 13.18. If U is any open cover of X, the inclusion map
CU
∗(X) →C∗(X) induces a homology isomorphism HU
p (X) ∼= Hp(X) for
all p.
The idea of the proof is simple, although the technical details are some-
what involved. If σ: Δp →X is any singular p-simplex, the plan is to
show that there is a homologous p-chain obtained by subdividing Δp and
restricting σ to each of the p-simplices of the subdivision. If we subdivide
suﬃciently ﬁnely, we can ensure that each of the resulting simplices will be
U-small. The tricky part is to do this in a systematic way that allows us to
keep track of the boundary operators. Before the formal proof, let us lay
some groundwork.
Recall the barycentric subdivision of a Euclidean simplicial complex in-
troduced in Chapter 5. It is obtained by replacing each simplex with its
barycenter together with cones on appropriate lower-dimensional simplices
from the barycenter. To deﬁne a subdivision operator in singular homology,
we begin by extending the cone construction to aﬃne singular simplices.
If σ = α(v0, . . . , vp) is an aﬃne singular p-simplex in some convex set
K ⊂Rm and v is any point in K, we deﬁne an aﬃne singular (p+1)-simplex
v ∗σ called the cone on σ from v by
v ∗σ = v ∗α(v0, . . . , vp) = α(v, v0, . . . , vp).
In other words, v ∗σ: Δp+1 →K is the unique aﬃne simplex that sends
e0 to v and whose 0th face map is equal to σ. We extend this operator to
aﬃne chains by linearity: v ∗(
i niσi) = 
i ni(v ∗σi). (It is not deﬁned
for arbitrary singular chains.)
Lemma 13.19. If c is an aﬃne chain, then
∂(v ∗c) = c −v ∗∂c.
(13.15)
Proof. For an aﬃne simplex σ = α(v0, . . . , vp), this is just a computation:
∂(v ∗σ) = ∂α(v, v0, . . . , vp)
=
p+1

i=0
(−1)iα(v, v0, . . . , vp) ◦Fi,p
= α(v0, . . . , vp) +
p

i=0
(−1)i+1α(v, v0, . . . , vi, . . . , vp)
= σ −v ∗∂σ.
The general case follows by linearity.

316
13. Homology
e0
b1
e1
b2
si1
si2
σ
σ
FIGURE 13.9. Singular subdivisions in dimensions 1 and 2.
Now we deﬁne an operator s taking p-chains to p-chains, called the sin-
gular subdivision operator. We deﬁne it ﬁrst for aﬃne chains in Rn, by
induction on p. For p = 0, simply set s = Id. For p > 0, set
sc = bp ∗s∂c,
where bp is the barycenter of Δp. For example, if ip : Δp →Δp is the
identity map, thought of as an aﬃne singular p-simplex in Δp, sip is a
sum of aﬃne simplices mapping homeomorphically onto the simplices of
the barycentric subdivision of Δp.
For a singular p-simplex σ in any space X, note that σ = σ#ip, where
σ# : Cp(Δp) →Cp(X) is the chain map obtained from the continuous map
σ: Δp →X. We deﬁne sσ = σ#(sip), and extend by linearity to all of
Cp(X). Low-dimensional examples are pictured in Figure 13.9. We can
iterate s to obtain operators s2 = s ◦s and more generally sk = s ◦sk−1.
Lemma 13.20. The singular subdivision operator has the following prop-
erties.
(a) s ◦f# = f# ◦s for any continuous map f.
(b) ∂◦s = s ◦∂.
(c) Given an open cover U of X and any c ∈Cp(X), there exists m such
that smc ∈CU
p (X).
Proof. The ﬁrst identity follows immediately from the deﬁnition of s:
s(f#σ) = s(f ◦σ) = (f ◦σ)#(sip) = f#σ#(sip) = f#(sσ).

The Mayer–Vietoris Theorem
317
The second is proved by induction on p. For p = 0 it is trivial, and for
p > 0 we use part (a), (13.15), and the inductive hypothesis to compute
∂sσ = ∂σ#(bp ∗s∂ip)
= σ#∂(bp ∗s∂ip)
= σ#(s∂ip −bp ∗∂s∂ip)
= sσ#∂ip −σ#bp ∗(s∂∂ip)
= s∂σ#ip −0
= s∂σ.
To prove (c), deﬁne the mesh of an aﬃne chain c in Rn to be the maximum
of the diameters of the images of the aﬃne simplices that appear in c. By
Lemma 5.18, by choosing m large enough, we can make the mesh of smip
arbitrarily small.
If σ is any singular simplex in X, by the Lebesgue number lemma there
exists δ > 0 such that σ maps any subset of Δp of diameter less than δ
into one of the sets of U. In particular, if c is an aﬃne chain in Δp whose
mesh is less than δ, then σ#c ∈CU
p (X). Choose δ to be the minimum of the
Lebesgue numbers for all the singular simplices appearing in c, and choose
m large enough that smip has mesh less than δ. Then smσ = σ#(smip) ∈
CU
p (X) as desired.
With the machinery we have set up, it is now an easy matter to prove
Proposition 13.18.
Proof of Proposition 13.18.
The crux of the proof is the construction of a
chain homotopy between s and the identity map of Cp(X). Recall that this
is a homomorphism h: Cp(X) →Cp+1(X) satisfying
∂◦h + h ◦∂= Id −s.
(13.16)
We deﬁne h by induction on p. For p = 0, h is the zero homomorphism.
For p > 0, if σ is a singular p-simplex in any space, deﬁne
hσ = σ#bp ∗(ip −sip −h∂ip).
As with s, it is a trivial consequence of the deﬁnition that h ◦f# = f# ◦h
for any continuous map f. Observe also that if σ is a U-small simplex, then
hσ is a U-small chain, so h also maps CU
p (X) to CU
p+1(X).
The chain homotopy identity (13.16) is proved by induction on p. For
p = 0 it is immediate because h = ∂= 0 and s = Id. Suppose it holds for
(p −1)-chains in all spaces. If σ is a singular p-simplex, then
∂hσ = ∂σ#bp ∗(ip −sip −h∂ip)
= σ#∂bp ∗(ip −sip −h∂ip)
= σ#(ip −sip −h∂ip) −σ#bp ∗(∂ip −∂sip −∂h∂ip).

318
13. Homology
The expression inside the second set of parentheses is equal to ∂ip −s∂ip −
∂h∂ip −h∂∂ip, which is zero by the inductive hypothesis because ∂ip is a
(p −1)-chain. Therefore,
∂hσ = σ#ip −sσ#ip −h∂σ#ip = σ −sσ −h∂σ,
which was to be proved.
Now if c is any singular cycle in X, (13.16) shows that
c −sc = ∂hc + h∂c = ∂hc,
so sc diﬀers from c by a boundary. If c ∈CU
p (X), the diﬀerence is the
boundary of a chain in CU
p+1(X). By induction the same is true for smc for
any positive integer m. Moreover, smc is a cycle because s commutes with
∂.
The inclusion map ι: CU
p (X) 	→Cp(X) is clearly a chain map, and so
induces a homology homomorphism ι∗: HU
p (X) →Hp(X). It is surjective
because for any [c] ∈Hp(X) we can choose m large enough that smc ∈
CU
p (X), and the argument above shows that c is homologous to smc. To
prove injectivity, suppose [c] ∈HU
p (X) satisﬁes ι∗[c] = 0. This means that
there is a (p + 1)-chain b ∈Cp+1(X) such that c = ∂b. Choose m large
enough that smb ∈CU
p+1(X). Then ∂smb = sm∂b = smc, which diﬀers
from c by the boundary of a chain in CU
p+1(X). Thus c represents the zero
element of HU
p (X).
Applications
In this section we give a sampling of the numerous signiﬁcant applications
of homology theory to the study of manifolds. These applications are based
on the fact that the homology groups give us a simple way to distinguish
topologically between spheres of diﬀerent dimensions and between homo-
topy classes of maps of spheres, something that the fundamental group
could not do. Several more such applications are outlined in the problems.
Invariance of Dimension
The dimension of a manifold is part of its deﬁnition: An n-dimensional
manifold is one that admits local homeomorphisms to open subsets of Rn.
It seems intuitively obvious that dimension ought to be a topological in-
variant: A manifold of dimension n ought not to be homeomorphic to one
of some other dimension. This is true, but the proof is decidedly nontrivial.
A proof for n = 1 was outlined in Problem 4-1 using the fact that Rn ∖{0}
is connected when n > 1. Similarly, Problem 8-5 suggested a proof for
n = 2 using the fact that Rn ∖{0} is simply connected when n > 2. But

Applications
319
x
U
Sε(x)
FIGURE 13.10. Proof of Lemma 13.21.
neither connectedness nor simple connectedness can distinguish Rn ∖{0}
from Rm ∖{0} when both m and n are larger than 2. Homology can.
Lemma 13.21. Let U be an open subset of Rn, n ≥2. If x is any point
in U, then Hn−1(U ∖{x}) ̸= 0.
Proof. Choose ε > 0 small enough that the sphere Sε(x) of radius ε about
x is contained in U (Figure 13.10). Consider the following commutative
diagram of inclusion maps:
Sε(x)
?
i
k
QQQQ
s
U ∖{x}
Rn ∖{x}.
-
j
These induce homology homomorphisms
Hn−1(Sε(x))
?
i∗
k∗
QQQQQQQ
s
Hn−1(U ∖{x})
Hn−1(Rn ∖{x}).
-
j∗
Because k is a homotopy equivalence, k∗is an isomorphism. This implies
that i∗is injective (and j∗is surjective). Since Hn−1(Sε(x)) is not trivial,
neither is Hn−1(U ∖{x}).
Theorem 13.22 (Invariance of Dimension).
If m ̸= n, a topological
space cannot be both an n-manifold and an m-manifold.
Proof. The zero-dimensional case is easy to dispose of, because a 0-manifold
is a discrete space, and points in a positive-dimensional manifold are not

320
13. Homology
open sets. Suppose M is both an m-manifold and an n-manifold, and as-
sume that n > m ≥1. Any x ∈M has a neighborhood U ⊂M that
is homeomorphic to Rn. Because an open subset of a manifold is again a
manifold, U is also an m-manifold, so x has a neighborhood V ⊂U that
is homeomorphic to Rm. On the one hand, because V is homeomorphic to
an open subset in Rn, Lemma 13.21 implies Hn−1(V ∖{x}) ̸= 0. On the
other hand, V ∖{x} ≈Rm ∖{0} ≃Sm−1, so Hn−1(V ∖{x}) = 0.
Degree Theory for Spheres
In Problem 8-7, we deﬁned the degree of a continuous map f : S1 →S1.
Homology theory allows us to extend this deﬁnition to higher-dimensional
spheres. Suppose n ≥1. Because Hn(Sn) is inﬁnite cyclic, if f : Sn →Sn is
any continuous map, f∗: Hn(Sn) →Hn(Sn) is multiplication by a unique
integer (Exercise A.28), called the degree of f and denoted by deg f.
Proposition 13.23. Suppose n ≥1 and f, g: Sn →Sn are continuous
maps.
(a) If f ≃g, then deg f = deg g.
(b) deg(g ◦f) = (deg g)(deg f).
(c) The identity map has degree 1.
Proof. Part (a) follows from the fact that homotopic maps induce the same
homology homomorphism; part (b) from the fact that (g ◦f)∗= g∗◦
f∗; and part (c) from the fact that the identity map induces the identity
homomorphism on homology.
For a map f : S1 →S1 the deﬁnition of deg f given in Problem 8-7 was
the unique integer k such that the homomorphism (ρ ◦f)∗: π1(S1, 1) →
π1(S1, 1) is given by γ 
→γk, where ρ is the rotation taking f(1) to 1. For
the moment, let us call that deﬁnition the homotopic degree of f, and the
degree we have deﬁned in this chapter its homological degree.
Lemma 13.24. The homological degree and the homotopic degree of a con-
tinuous map f : S1 →S1 are equal.
Proof. By examining the deﬁnition of the Poincar´e homomorphism γ, it is
easy to see that the following diagram commutes:
H1(S1)
H1(S1).
-
(ρ ◦f)∗
π1(S1, 1)
π1(S1, 1)
-
(ρ ◦f)∗
?
γ
?
γ

Applications
321
It follows that the homotopic degree of f is equal to the homological degree
of ρ ◦f. Since the rotation ρ is homotopic to the identity map, it has
homological degree 1, so the homological degree of ρ ◦f is equal to that of
f.
Some of the most important applications of degree theory come from
considering the antipodal map A: Sn →Sn given by A(x) = −x.
Lemma 13.25. For each n ≥1, the antipodal map A: Sn →Sn has degree
(−1)n+1.
Proof. Consider the reﬂection maps Ri : Sn →Sn given by
Ri(x1, . . . , xi, . . . , xn+1) = (x1, . . . , −xi, . . . , xn+1).
We will prove by induction on n that Ri has degree −1; because the an-
tipodal map is equal to the (n + 1)-fold composition R1 ◦· · · ◦Rn+1, it
follows that A has degree (−1)n+1.
Note that if deg Ri = −1 for one value of i the same is true for all of
them, because Ri can be obtained from Rj by conjugating with the linear
transformation that interchanges xi and xj.
For n = 1, R2(z) = z in complex notation, which has degree −1 by
Problem 8-7. So suppose n > 1, and assume that the claim is true for
reﬂections in dimension n −1.
Recall that in the course of proving Proposition 13.14 we showed that
Hn(Sn) ∼= Hn−1(Sn−1). In fact, we will reﬁne that argument to show that
there is an isomorphism between these groups such that the following dia-
gram commutes:
Hn(Sn)
Hn−1(Sn−1).
-
Hn(Sn)
Hn−1(Sn−1)
-
?
R1∗
?
R1∗
(13.17)
From this it follows immediately by induction that R1 has degree −1 on
Sn.
To prove (13.17), let U = {U, V } be the covering of Sn by contractible
open sets used in the proof of Proposition 13.14 (the complements of the
north and south poles). Note that R1 preserves the sets U and V , and
therefore induces chain maps that make the following diagram commute:
0- C∗(U ∩V )
- C∗(U) ⊕C∗(V )
CU
∗(Sn)
-
0
-
?
R1#
?
R1# ⊕R1#
?
R1#
0- C∗(U ∩V )
- C∗(U) ⊕C∗(V )
CU
∗(Sn)
-
0.
-

322
13. Homology
Therefore, by the naturality property of ∂∗, the following diagram also
commutes:
Hn(Sn)
-
∂∗
Hn−1(U ∩V )
Hn−1(Sn−1)
ι∗
?
R1∗
?
R1∗
?
R1∗
Hn(Sn)
-
∂∗
Hn−1(U ∩V )
Hn−1(Sn−1),
ι∗
where Sn−1 = Sn ∩{x : xn+1 = 0} is the equatorial (n −1)-sphere and
ι: Sn−1 →U ∩V is inclusion. The horizontal maps are isomorphisms: ι∗
because ι is a homotopy equivalence, and ∂∗by the argument in the proof of
Proposition 13.14. Composing the horizontal isomorphisms and eliminating
the middle column, we obtain (13.17).
Proposition 13.26. The antipodal map A: Sn →Sn is homotopic to the
identity map if and only if n is odd.
Proof. If n = 2k −1 is odd, an explicit homotopy H : Id ≃A is given by
H(x, t) = ((cos πt)x1 + (sin πt)x2, (cos πt)x2 −(sin πt)x1,
. . . , (cos πt)x2k−1 + (sin πt)x2k, (cos πt)x2k −(sin πt)x2k−1).
If n = 0, A interchanges the two points of S0, and so is clearly not homotopic
to the identity. When n is even and positive, A has degree −1, while the
identity map has degree 1, so they are not homotopic.
A vector ﬁeld on Sn is a continuous map V : Sn →Rn+1 such that for
each x ∈Sn, V (x) is tangent to Sn at x, or in other words the Euclidean
dot product V (x)·x = 0. The following theorem is popularly known as the
“hairy ball theorem” because in the two-dimensional case it implies that
you cannot comb the hair on a hairy billiard ball without introducing a
discontinuity somewhere.
Theorem 13.27 (The Hairy Ball Theorem).
There exists a nowhere
vanishing vector ﬁeld on Sn if and only if n is odd.
Proof. Suppose there exists such a vector ﬁeld V . By replacing V with
V/|V |, we can assume |V (x)| = 1 everywhere. We use V to construct a
homotopy between the identity map and the antipodal map as follows:
H(x, t) = (cos πt)x + (sin πt)V (x).
Direct computation, using the facts that |x|2 = |V (x)|2 = 1 and x·V (x) =
0, shows that H takes its values in Sn. Since H(x, 0) = x and H(x, 1) = −x,
H is the desired homotopy. By Proposition 13.26, n must be odd.

The Homology of a Simplicial Complex
323
Conversely, when n = 2k −1 is odd, the following explicit vector ﬁeld is
easily checked to be tangent to the sphere and nowhere vanishing:
V (x1, . . . , x2k) = (x2, −x1, x4, −x3, . . . , x2k, −x2k−1).
The Homology of a Simplicial Complex
Because both simplicial complexes and singular homology are built out of
simplices, it is reasonable to expect that the homology of a simplicial com-
plex should be computable from the combinatorial structure of the complex.
In this section we deﬁne another kind of homology group associated with
a simplicial complex, called simplicial homology groups, and prove that
they are isomorphic to the singular homology groups. As an application,
we prove the topological invariance of the Euler characteristic.
Let K be a ﬁnite simplicial complex. We deﬁne the pth simplicial chain
group of K, denoted by CΔ
p (K), to be the free abelian group on the set of
p-simplices in K.
To deﬁne the boundary operator, we choose a total ordering of the ver-
tices (v1, . . . , vN), and for a p-simplex ⟨vk0, . . . , vkp⟩we set
∂⟨vk0, . . . , vkp⟩=
p

i=0
(−1)i⟨vk0, . . . , vki, . . . , vkp⟩
if k0 < · · · < kp.
This extends uniquely to a homomorphism ∂: CΔ
p (K) →CΔ
p−1(K).
Lemma 13.28. For any simplicial p-chain c, ∂(∂c) = 0.
Proof. It suﬃces to show this when c is a p-simplex σ = ⟨vk0, . . . , vkp⟩, in
which case (assuming that the vertices appear in increasing order),
∂(∂σ) = ∂
p

i=0
(−1)i⟨vk0, . . . , vki, . . . , vkp⟩
=

0≤j<i≤p
(−1)i+j⟨vk0, . . . , vkj, . . . , vki, . . . , vkp⟩
+

0≤i≤j≤p−1
(−1)i+j⟨vk0, . . . , vki, . . . , vkj+1, . . . , vkp⟩.
After j = i′ −1 and i = j′ are substituted in the second sum, these two
sums cancel each other term by term.

324
13. Homology
We deﬁne
ZΔ
p (K) = Ker ∂: CΔ
p (K) →CΔ
p−1(K),
BΔ
p (K) = Im ∂: CΔ
p+1(K) →CΔ
p (K),
the groups of simplicial cycles and simplicial boundaries, respectively. The
preceding lemma shows that BΔ
p (K) is a subgroup of ZΔ
p (K), so we may
deﬁne the pth simplicial homology group of K to be the quotient
HΔ
p (K) = ZΔ
p (K)/BΔ
p (K).
Because the simplicial chain groups of a ﬁnite complex are all ﬁnitely
generated, simplicial homology can in principle be computed directly from
the combinatorial structure of a complex. In practice this is not usually
eﬃcient, at least without a computer, because triangulations of even very
simple spaces typically have a large number of simplices. We will see below
that the simplicial homology groups are isomorphic to the singular ones.
However, there is one case in which simplicial homology is not hard to
compute directly.
Lemma 13.29. Let K be a complex consisting of a single n-simplex and its
faces. Then HΔ
0 (K) is the inﬁnite cyclic group generated by the homology
class of any vertex, and HΔ
p (K) is trivial for p > 0.
Proof. We assume that an ordering (v0, . . . , vp) has been chosen for the
vertices of K. Deﬁne a homomorphism h: CΔ
p (K) →CΔ
p+1(K) by setting,
for any p-simplex τ = ⟨vk0, . . . , vkp⟩∈K,
hτ =

⟨v0, vk0, . . . , vkp⟩
if k0 ̸= 0,
0
if k0 = 0,
and extending h to a homomorphism.
When p > 0, a straightforward computation shows that ∂◦h+h◦∂= Id.
Thus if c is any p-cycle, c = ∂hc, which shows that HΔ
p (K) = 0.
For p = 0, deﬁne a homomorphism ε: CΔ
0 (K) →Z by ε(
i ni⟨vi⟩) =

i ni as in the proof of Proposition 13.5. Because ε⟨v0⟩= 1, ε is surjective.
Another computation shows that ∂hc = c −ε(c)⟨v0⟩for any 0-chain c, so
any chain in Ker ε is a boundary. Conversely, any boundary is in Ker ε
because ε∂⟨vi, vj⟩= ε(⟨vj⟩−⟨vi⟩) = 0 (assuming i < j). This shows that
ε descends to an isomorphism from HΔ
0 (K) to Z, so HΔ
0 (K) is the inﬁnite
cyclic group generated by the class of ⟨v0⟩.
It should be noted that there are several alternative ways of deﬁning
simplicial homology groups. The one most commonly used is to deﬁne the
simplicial chain group as the free abelian group on the set of oriented sim-
plices, with the convention that σ′ = −σ if σ′ is the same simplex as

The Homology of a Simplicial Complex
325
σ with the opposite orientation. Another possible chain group is the free
abelian group on all ordered simplices, considering diﬀerent vertex order-
ings of the same simplex as distinct generators. Both of these deﬁnitions
have the advantage that, unlike our deﬁnition, they do not depend on a
choice of ordering of the vertices; this is important if one wishes to deﬁne
homomorphisms induced by simplicial maps (which may not preserve the
vertex ordering) and prove functorial properties such as topological and
homotopy invariance. If our goal were to develop an entire theory of sim-
plicial homology groups, we would have to use one of these deﬁnitions. But
our aim is more modest: We wish only to show that simplicial homology
gives an alternative way of computing the singular homology groups, so
we use a deﬁnition that is technically somewhat simpler, and conﬁne our
attention to the properties needed for this purpose.
The main result we need is an analogue of the Mayer–Vietoris theorem
for simplicial homology. Fortunately, its proof is much easier than in the
singular case.
The setup for this theorem is slightly diﬀerent from that of its singular
cousin. In this case, instead of considering open subsets, we suppose K′
and K′′ are subcomplexes of K, and let L = K′ ∩K′′ (which is also a
subcomplex). As in the singular case, we have inclusion maps
j@
@@
R
K′
L
i



K′′
l



K.
k
@
@@
R
Each of these induces an inclusion map on simplicial chains, which is a
chain map, provided that we choose the vertex orderings in K′, K′′, and
L to be the restrictions of the ordering we chose for K. Therefore, all four
maps induce homology homomorphisms as well.
Theorem 13.30 (Simplicial Mayer–Vietoris Theorem).
Let K be a
ﬁnite simplicial complex, with subcomplexes K′, K′′ whose union is K,
and let L = K′ ∩K′′. For each p there is a connecting homomorphism
∂∗: HΔ
p (K) →HΔ
p−1(L) such that the following sequence is exact:
· · ·
∂∗
−→HΔ
p (L)
i∗⊕j∗
−−−→HΔ
p (K′) ⊕Hp(K′′)
k∗−l∗
−−−−→HΔ
p (K)
∂∗
−→HΔ
p−1(L)
i∗⊕j∗
−−−→· · · .
Proof. The sequence of chain maps
0 →CΔ
p (L)
i#⊕j#
−−−−→CΔ
p (K′) ⊕CΔ
p (K′′)
k#−l#
−−−−→CΔ
p (K) →0

326
13. Homology
is easily seen to be exact in this case. The existence of the connecting
homomorphism and the exactness of the Mayer–Vietoris sequence then
follow immediately from the zigzag lemma.
To analyze the relationship between simplicial and singular homology,
we deﬁne a map from the simplicial chain complex of K to the singular
chain complex of its geometric realization as follows. For any p-simplex
σ = ⟨vk0, . . . , vkp⟩∈K, let α(σ) denote the aﬃne singular p-simplex
α(vk0, . . . , vkp) in |K| (with the vertices in increasing order). This extends
uniquely to a homomorphism α: CΔ
p (K) →Cp(|K|). To see that it is a
chain map, just compute
∂α(vk0, . . . , vkp) =
p

i=0
(−1)iα(vk0, . . . , vkp) ◦Fi,p
=
p

i=0
(−1)iα(vk0, . . . , vki, . . . , vkp)
= α(∂⟨vk0, . . . , vkp⟩).
Therefore, α induces a homology homomorphism α∗: HΔ
p (K) →Hp(|K|).
Theorem 13.31. For any ﬁnite complex K, the map α∗: HΔ
p (K) →
Hp(|K|) is an isomorphism for all p.
Proof. We prove the theorem by induction on the dimension of K. If
dim K = 0, then K is just a ﬁnite set of vertices. In this case, CΔ
0 (K)
is the free abelian group on the set of vertices, and all the other simplicial
chain groups are trivial. Therefore, all the boundary operators are zero,
and HΔ
p (K) ∼= CΔ
p (K), which is isomorphic to the corresponding singular
group. The map α∗: HΔ
0 (K) →H0(|K|) takes each generator [⟨v⟩] to a
generator [α(v)], so the theorem is proved in this case.
Now suppose the theorem is true for complexes of dimension n −1, and
let K have dimension n. We proceed by induction on the number of n-
simplices in K. When there are no n-simplices, K is (n −1)-dimensional,
so the theorem is true in that case.
Suppose K′ is the subcomplex of K obtained by deleting a single n-
simplex σ. (It is a subcomplex because K has no simplices of dimension
greater than n.) Let K′′ denote the subcomplex consisting of σ and all its
faces, and L = K′ ∩K′′. We will prove the inductive step by comparing the
Mayer–Vietoris sequence of K (in simplicial homology) with that of |K| (in
singular homology).
To set up the sequence in singular homology, let V be a neighborhood
of |σ| that admits a strong deformation retraction onto |σ| (such a neigh-
borhood exists by Problem 7-6), and let U = |K| ∖{x} for some point
x ∈Int |σ|. Clearly, |K′| ⊂U, |K′′| ⊂V , and |L| ⊂U ∩V . All of these
inclusions are homotopy equivalences: Our choice of V guarantees that it

The Homology of a Simplicial Complex
327
admits a strong deformation retraction onto |K′′|, and it is easy to con-
struct a strong deformation of U onto |K′| that deforms σ ∖{x} onto its
boundary while leaving |K′| ﬁxed. Gluing these maps together, we obtain
a strong deformation retraction of U ∩V onto L.
Restricting α: CΔ
p (K) →Cp(|K|) to the chain groups of the various sub-
complexes yields the following diagram of chain maps, which is obviously
commutative:
0
- CΔ
∗(L)
-
i# ⊕j# CΔ
∗(K′) ⊕CΔ
∗(K′′)
CΔ
∗(K)
-
k# −l#
0
-
?
α
?
α ⊕α
?
α
0- C∗(U ∩V )
-
i# ⊕j# C∗(U) ⊕C∗(V )
CU
∗(|K|)
-
k# −l#
0.
-
Therefore, using Proposition 13.16 we see that the following diagram com-
mutes and has exact rows:
HΔ
p (L)
- HΔ
p (K′) ⊕HΔ
p (K′′)
HΔ
p (K)
-
-
?
?
?
Hp(U ∩V )
- Hp(U) ⊕Hp(V )
HU
p (|K|)
-
-
HΔ
p−1(L)
HΔ
p−1(K′) ⊕HΔ
p−1(K′′)
-
?
?
Hp−1(U ∩V )
Hp−1(U) ⊕Hp−1(V ).
-
With U ∩V , U, and V in these groups replaced by their homotopy equiv-
alent spaces |L|, |K′|, and |K′′|, the diagram still commutes because the
homotopy equivalences are all inclusion maps. Thus we ﬁnally arrive at a
diagram in which all the vertical homomorphisms except the center one are
isomorphisms. (For K′ and L this follows from the inductive hypothesis,
and for K′′ it follows from Lemma 13.29.) Therefore, by the ﬁve lemma,
the middle arrow is also an isomorphism. Finally, replacing HU
p by Hp, we
obtain the result.
Topological Invariance of the Euler Characteristic
Our most signiﬁcant application of simplicial homology is the following
theorem, which generalizes Corollary 10.15 and Problem 10-9.
Theorem 13.32. The Euler characteristic of a ﬁnite simplicial complex
K is given by the formula
χ(K) =

p
(−1)p rank Hp(|K|).
Therefore, the Euler characteristic is a topological invariant of |K|.

328
13. Homology
Proof. Let n = dim K. Recall from Chapter 5 that the Euler characteristic
of K is deﬁned as
χ(K) =
n

p=0
(−1)pcp,
where cp is the number of p-simplices in K. Note that cp is also the rank
of the simplicial chain group CΔ
p (K).
Consider the following short exact sequences:
0 →BΔ
p (K) 	→ZΔ
p (K) →HΔ
p (K) →0,
0 →ZΔ
p (K) 	→CΔ
p (K)
∂→BΔ
p−1(K) →0.
Let us write
bp = rank BΔ
p (K),
zp = rank ZΔ
p (K),
hp = rank HΔ
p (K).
By Proposition 9.16, we have the following equalities:
zp = hp + bp,
cp = zp + bp−1.
Therefore,
χ(K) =
n

p=0
(−1)pcp
=
n

p=0
(−1)p(zp + bp−1)
=
n

p=0
(−1)p(hp + bp + bp−1).
Because b−1 = bn = 0, the bp and bp−1 terms above form a telescoping
sum adding to zero. Because hp = rank Hp(|K|) by Theorem 13.31, this
completes the proof.
For any topological space X, the integer βp(X) = rank Hp(X) (if it is ﬁ-
nite) is called the pth Betti number of X. We deﬁne the Euler characteristic
of X by
χ(X) =

p
(−1)pβp(X)
provided that each βp(X) is ﬁnite and βp(X) = 0 for p suﬃciently large.
The preceding theorem then says that χ(K) = χ(|K|) for a ﬁnite simplicial
complex K.

Cohomology
329
Cohomology
As Proposition 13.2 shows, the singular homology groups are covariant
functors from the category of topological spaces to the category of abelian
groups. For many applications, it turns out to be much more useful to have
contravariant functors. We will not pursue any of these applications here,
but content ourselves to note that one of the most important, the de Rham
theory of diﬀerential forms, plays a central role in diﬀerential geometry.
To give you a view of what is to come, in this ﬁnal section we introduce
singular cohomology, which is essentially a contravariant version of singular
homology. It does not give us any new information about topological spaces,
but the information is organized in a diﬀerent way, which is much more
appropriate for some applications.
In Example 7.32 we observed that for any ﬁxed abelian group G, there
is a contravariant functor from the category of abelian groups to itself
that sends each group X to the group Hom(X, G) of homomorphisms into
G, and each homomorphism f : X →Y to the induced homomorphism
f ∗: Hom(Y, G) →Hom(X, G) given by f ∗(ϕ) = ϕ ◦f. We apply this to
the singular chain groups as follows. Given a topological space X and an
abelian group G, for any integer p ≥0 let Cp(X; G) denote the group
Hom(Cp(X), G). Elements of Cp(X; G) are called p-dimensional singular
cochains with coeﬃcients in G (p-cochains for short).
The boundary operator ∂: Cp+1(X) →Cp(X) induces a homomorphism
δ: Cp(X; G) →Cp+1(X; G), called the coboundary operator, characterized
by
(δϕ)(c) = ϕ(∂c).
It is immediate that δ ◦δ = 0, so we have a chain complex
· · · →Cp−1(X; G)
δ−→Cp(X; G)
δ−→Cp+1(X; G) →· · · .
(Actually, when the arrows go in the direction of increasing indices as in
this case, it is customary to call it a cochain complex.) A p-cochain ϕ is
called a cocycle if δϕ = 0, and a coboundary if there exists ψ ∈Cp−1(X; G)
such that δψ = ϕ. The subgroups of Cp(X; G) consisting of cocycles and
coboundaries are denoted by Zp(X; G) and Bp(X; G), respectively.
We deﬁne the pth singular cohomology group of X with coeﬃcients in G
to be the quotient
Hp(X; G) = Zp(X; G)/Bp(X; G).
If f : X →Y is a continuous map, we obtain a map f # : Cp(Y ; G) →
Cp(X; G) (note the reversal of direction) by
(f #ϕ)(c) = ϕ(f#c).

330
13. Homology
This map commutes with the coboundary operators because
(f #δϕ)(c) = δϕ(f#c) = ϕ(∂f#c) = ϕ(f#∂c) = (f #ϕ)(∂c) = (δf #ϕ)(c).
(A map that commutes with δ is called, predictably enough, a cochain map.)
Therefore, f # induces a cohomology homomorphism f ∗: Hp(Y ; G) →
Hp(X; G) by f ∗[ϕ] = [f #ϕ].
Proposition 13.33. The induced cohomology homomorphism satisﬁes the
following properties.
(a) If f : X →Y and g: Y →Z are continuous, then (g ◦f)∗= f ∗◦g∗.
(b) The homomorphism induced by the identity map is the identity.
Therefore, the assignment X 
→Hp(X; G), f 
→f ∗deﬁnes a contravariant
functor from the category of topological spaces to the category of abelian
groups.
Corollary 13.34 (Topological Invariance of Cohomology).
If
f : X →Y is a homeomorphism, then for any abelian group G and any
integer p ≥0, f ∗: Hp(Y ; G) →Hp(X; G) is an isomorphism.
Exercise 13.4.
Prove Proposition 13.33 and Corollary 13.34.
In a very speciﬁc sense, the singular cohomology groups express the same
information as the homology groups, but in rearranged form. The precise
statement is given by the universal coeﬃcient theorem, which gives an exact
sequence from which the cohomology groups with any coeﬃcients can be
computed from the singular homology groups. The statement and proof
can be found in [Mun75] or [Spa89]. We will not go into the general case
here, but we can easily handle one special case.
Let F be a ﬁeld of characteristic zero, which just means that F is torsion
free as an abelian group under addition. (In most applications F will be
R, C, or Q.) We can form the cohomology groups Hp(X; F) as usual, just
by regarding F as an abelian group; but in this case they have a bit more
structure. The basic algebraic facts are expressed in the following lemma.
Lemma 13.35. Let F be a ﬁeld of characteristic zero.
(a) For any abelian group G, the set Hom(G, F) of group homomorphisms
from G to F is a vector space over F with scalar multiplication deﬁned
pointwise: (aϕ)(g) = a(ϕ(g)) for a ∈F.
(b) If f : G1 →G2 is a group homomorphism, then the induced homo-
morphism f ∗: Hom(G2, F) →Hom(G1, F) is a linear transformation
of vector spaces.

Cohomology
331
(c) If G is ﬁnitely generated, the dimension of Hom(G, F) is equal to the
rank of G.
Proof. The proofs of (a) and (b) are straightforward (and hold for any
ﬁeld, not just one of characteristic zero), and are left as an exercise. For
(c), we proceed as follows. First suppose G is free abelian of rank n, and
let g1, . . . , gn be a basis for G (as an abelian group). For each i, deﬁne a
homomorphism ϕi : G →F by setting
ϕi(gj) =

1
if i = j,
0
if i ̸= j.
If 
i aiϕi is the zero homomorphism for some scalars ai ∈F, applying this
homomorphism to gj shows that aj = 0, so the ϕi’s are linearly indepen-
dent. On the other hand, it is easy to see that an arbitrary ϕ ∈Hom(G, F)
can be written ϕ = 
i aiϕi with ai = ϕ(gi); thus the ϕi’s are a basis for
Hom(G, F), proving the result in this case.
In the general case, let Gtor ⊂G be the torsion subgroup of G.
The surjective homomorphism π: G →G/Gtor induces a homomorphism
π∗: Hom(G/Gtor, F) →Hom(G, F). It follows easily from the surjectivity
of π that π∗is injective. On the other hand, let ϕ ∈Hom(G, F) be ar-
bitrary. If g ∈G satisﬁes kg = 0, then ϕ(g) = ϕ(kg)/k = 0, so Gtor ⊂
Ker ϕ and ϕ descends to a homomorphism ϕ ∈Hom(G/Gtor, F). Clearly,
π∗ϕ = ϕ, so π∗is an isomorphism. Because G/Gtor is free abelian, we have
dim Hom(G, F) = dim Hom(G/Gtor, F) = rank(G/Gtor) = rank G.
Exercise 13.5.
Prove parts (a) and (b) of Lemma 13.35.
Applying this to Cp(X; F) = Hom(Cp(X), F), we see that the cochain
groups are F-vector spaces and the coboundary operators are linear maps.
It follows that Zp(X; F) and Bp(X; F) are vector spaces as is the quo-
tient Hp(X; F) = Zp(X; F)/Bp(X; F). Moreover, for any continuous map
f : X →Y , the induced cohomology map f ∗: Hp(Y ; F) →Hp(X; F) is also
a linear map.
The special feature of ﬁeld coeﬃcients that makes the cohomology groups
easier to calculate is expressed in the following lemma.
Lemma 13.36 (Extension Lemma).
Let F be a ﬁeld of characteristic
zero. If G is an abelian group, any group homomorphism from a subgroup
of G to F admits an extension to all of G.
Proof. Suppose H ⊂G is a subgroup and f : H →F is a homomorphism.
Consider the set F of all pairs (H′, f ′), where H′ is a subgroup of G con-
taining H and f ′ : H′ →F is an extension of f. Deﬁne a partial ordering
on F by declaring (H′, f ′) ≤(H′′, f ′′) if H′ ⊂H′′ and f ′′|H′ = f ′. Given
any totally ordered subset T ⊂F, deﬁne H to be the union of all the

332
13. Homology
spaces H′ such that (H′, f ′) ∈T. There is a uniquely deﬁned homomor-
phism f : H →F, deﬁned by setting f(h) = f ′(h) for any pair (H′, f ′) ∈T
such that h ∈H′. The pair ( H, f) is easily seen to be an upper bound for
T. Thus by Zorn’s lemma (Lemma A.3 in the Appendix), there exists a
maximal element in F; call it (H0, f0).
If H0 = G, we are done. If not, we will show that f0 can be extended to
a larger subgroup containing H0, which contradicts the maximality of H0.
Suppose there is some element g ∈G ∖H0. Let Hg denote the subgroup
Hg = {h + mg : h ∈H0, m ∈Z}.
The quotient group Hg/H0 is cyclic and generated by the coset of g. There
are two cases.
If Hg/H0 is inﬁnite, then no multiple of g is in H0, so every element
of Hg can be written uniquely in the form h + mg and we can deﬁne an
extension f ′
0 of f0 just by setting f ′
0(h+mg) = f0(h). On the other hand, if
Hg/H0 is ﬁnite, let n be the order of this group. This means that mg ∈H0
if and only if m is a multiple of n. Let k = f0(ng)/n ∈F, and deﬁne an
extension f ′
0 of f0 by letting
f ′
0(h + mg) = f0(h) + mk.
To show that this is well-deﬁned, suppose h+mg = h′ +m′g for h, h′ ∈H0
and m, m′ ∈Z. Then (m−m′)g = h′ −h ∈H0, which implies m−m′ = jn
for some integer j. We compute
(f0(h) + mk) −(f0(h′) + m′k) = f0(h −h′) + (m −m′)k
= f0(−jng) + jnk = 0.
Therefore, f ′
0 is an extension of f0, which completes the proof.
Now we come to the main result of this section, which gives explicit
formulas for singular cohomology with coeﬃcients in F.
Theorem 13.37. Let F be a ﬁeld of characteristic zero. For any topological
space X, the vector spaces Hp(X; F) and Hom(Hp(X), F) are isomorphic;
hence if Hp(X) is ﬁnitely generated, then the dimension of Hp(X; F) is
equal to the rank of Hp(X).
Proof. An arbitrary cocycle ϕ ∈Zp(X; F) deﬁnes a homomorphism
ϕ: Hp(X) →F by
ϕ[c] = ϕ(c).
Since ϕ(∂b) = δϕ(b) = 0, this is well-deﬁned independently of the choice
of representative c in its homology class. If ϕ = δη is a coboundary, then
ϕ[c] = ϕ(c) = δη(c) = η(∂c) = 0, so the homomorphism ϕ 
→ϕ contains

Cohomology
333
the coboundary group Bp(X; F) in its kernel. It therefore descends to a
homomorphism β : Hp(X; F) →Hom(Hp(X), F), given by β[ϕ] = ϕ. We
will show that β is an isomorphism.
Let f ∈Hom(Hp(X), F) be arbitrary. Letting π: Zp(X) →Hp(X)
denote the projection deﬁning Hp(X), we obtain a homomorphism f ◦
π: Zp(X) →F. By the extension lemma, this extends to a homomorphism
ϕ: Cp(X) →F, i.e., a p-cochain. In fact, ϕ is a coboundary, because
(δϕ)c = ϕ(∂c) = f ◦π(∂c) = f[∂c] = 0.
Unwinding the deﬁnitions, we see that f = β[ϕ], so β is surjective.
To show that it is injective, suppose β[ϕ] = 0. This means that ϕ ∈
Cp(X; F) satisﬁes ϕ(c) = 0 for all cycles c, so Zp(X) ⊂Ker ϕ. Therefore,
ϕ descends to a homomorphism ϕ: Cp(X)/Zp(X) →F.
On the other hand, the surjective homomorphism ∂: Cp(X) →Bp−1(X)
has kernel equal to Zp(X), and therefore induces an isomorphism
∂: Cp(X)/Zp(X) →Bp−1(X). Composition gives a homomorphism ϕ ◦
∂−1 : Bp−1(X) →F:
Bp−1(X)
∂−1
−−→Cp(X)/Zp(X)
ϕ
−→F.
By the extension lemma, this extends to a homomorphism η: Cp−1(X) →
F. If c ∈Cp(X) is arbitrary,
η(∂c) = (ϕ ◦∂−1)(∂c) = ϕ(c),
which shows that ϕ = δη, and so [ϕ] = 0. Thus β is injective, completing
the proof.
As a consequence of this theorem, the Euler characteristic of a space
can also be computed in terms of its cohomology. The following corollary
follows immediately from the theorem.
Corollary 13.38. If X is a topological space such that Hp(X) is ﬁnitely
generated for all p and zero for p suﬃciently large, then for any ﬁeld F of
characteristic zero,
χ(X) =

p
(−1)p dim Hp(X; F).

334
13. Homology
Problems
13-1. Let Pn be the real projective space of dimension n.
(a) Show that Pn is homeomorphic to the quotient of Bn by the
relation that identiﬁes antipodal points on the boundary sphere.
(b) Use (a) and the results of this chapter to compute the singular
homology groups of P2 and P3.
13-2. Let n ≥1. If f : Sn →Sn is a continuous map that has a continuous
extension to a map F : Bn+1 →Sn, show that f has degree zero.
13-3. Show that Sn is not a retract of Bn+1 for any n.
13-4. Prove the Brouwer ﬁxed point theorem: Any continuous map f : Bn →
Bn has a ﬁxed point. [See Problem 8-9.]
13-5. Show that the dimension of a ﬁnite-dimensional simplicial complex
K is a topological invariant of |K|, and that any triangulation of an
n-manifold has dimension n. [Be careful: We are not assuming that
the complexes are ﬁnite.]
13-6. Prove that the singular homology groups of any compact polyhedron
are ﬁnitely generated.
13-7. If M is a triangulable compact manifold, show that Hp(M) = 0 if
p > dim M.
13-8. An n-dimensional pseudomanifold is an n-dimensional simplicial com-
plex in which every simplex is a face of some n-simplex, every
(n −1)-simplex is a face of exactly two n-simplices, and for every
pair of n-simplices σ, σ′ there exists a ﬁnite sequence of n-simplices
σ = σ1, . . . , σk = σ′ such that σi and σi+1 have an (n−1)-dimensional
face in common. Show that the nth (singular or simplicial) homology
group of an n-dimensional pseudomanifold is inﬁnite cyclic if it is ori-
entable and trivial if not. [It can be shown (see, e.g., [Mun75]) that
every triangulated, connected, compact manifold is a pseudomanifold,
and then this result characterizes the nth homology of triangulable
compact n-manifolds. But this requires more machinery than we have
developed.]
13-9. Suppose M is an n-manifold with boundary. Show that the set of
boundary points and the set of interior points of M are disjoint.
13-10. Let X1 and X2 be spaces with nondegenerate base points q1 and q2.
Show that Hp(X1 ∨X2) ∼= Hp(X1) ⊕Hp(X2) for all p > 0. [Hint: For
p = 1, use Problem 10-15.]

Problems
335
13-11. A (covariant or contravariant) functor from the category of abelian
groups to itself is said to be exact if it takes exact sequences to exact
sequences. If F is a ﬁeld of characteristic zero, show that the functor
G 
→Hom(G, F), f 
→f ∗is exact.
13-12. If U and V are open subsets of the topological space X, prove that
there is an exact Mayer–Vietoris sequence for cohomology with coef-
ﬁcients in a ﬁeld F of characteristic zero:
· · · →Hp−1(U ∩V ; F) →Hp(X; F) →Hp(U; F) ⊕Hp(V ; F) →
Hp(U ∩V ; F) →· · · .
[Hint: Use Problem 13-11.]
13-13. An abelian group K is said to be divisible if for any k ∈K and nonzero
n ∈Z, there exists k′ ∈K such that nk′ = k. It is said to be injective
if for every group G, any homomorphism from a subgroup of G into
K extends to all of G. Show that an abelian group K is injective if
and only if it is divisible if and only if the functor G 
→Hom(G, K)
is exact.

Appendix
Review of Prerequisites
The most important prerequisite for studying this book is a thorough
grounding in advanced calculus. Since there are hundreds of books that
treat this subject well, we will simply assume familiarity with it, and re-
mind the reader of important facts when necessary. We also assume that
the reader is familiar with the terminology and rules of ordinary logic.
The other prerequisites are a solid understanding of the basic properties
of sets, metric spaces, and groups, at the level that you would ﬁnd in most
undergraduate courses in real analysis and abstract algebra.
In this appendix we brieﬂy review some fundamental aspects of these
three subjects. If you have not studied this material before, you cannot hope
to learn it from scratch here. But this appendix can serve as a reminder of
important concepts that you may have forgotten, as a way to standardize
our notation and terminology, and as a source of references to books where
you can look up more of the details to refresh your memory. You can use
the exercises to test your knowledge, or to brush up on any aspects of the
subject on which you feel your knowledge is shaky.
Set Theory
In this book, as in most modern mathematics, mathematical statements
are couched in the language of set theory. We give here a brief descriptive
summary of the parts of set theory that we will use, in the form that is
commonly called “naive set theory.” The word naive should be understood

338
Appendix: Review of Prerequisites
in the same sense in which it is used by Paul Halmos in his classic text
Naive Set Theory [Hal74]: The axioms of set theory are to be viewed much
as Euclid viewed his geometric axioms, as intuitively clear statements of
fact from which reliable conclusions can be drawn.
One must be a bit careful with the axioms, to be sure, because it is
possible to get into trouble by trying to construct sets too freely, as is
illustrated by the famous [[Paradox|paradox]] of Bertrand Russell described below. It
is primarily for this reason that we take the trouble to enumerate the axioms
at all. For more detail on the subject, in the same spirit as the treatment
here, consult [Hal74] or [Dev93]. We leave it to the set theorists to explore
the deep consequences of the axioms and the relationships among diﬀerent
axiom systems.
Basic Concepts
The word set is, mathematically, an undeﬁned term. A set should be
thought of as an assemblage of “mathematical objects,” whatever they
may be—things such as numbers, ordered pairs, functions, or other sets.
The properties of sets, and the rules for manipulating them, are expressed
in the axioms we list below. We sometimes use the words collection and
family as synonyms for set.
The fundamental relationship involving sets, which we also leave math-
ematically undeﬁned, is that of membership. Intuitively, if x is one of the
objects in the set S, then we say that x is a member or an element of S,
or x belongs to S, written x ∈S. The essential characteristic of sets is that
they are determined by their members. Formally, we deﬁne S = T to mean
x ∈S ⇐⇒x ∈T.
The set containing no elements is called the empty set and denoted by
∅. It is unique, because any two sets with no elements are equal by our
deﬁnition of set equality, so we are justiﬁed in calling it “the” empty set.
(We could postulate its existence as a separate axiom, but its existence will
follow from our other axioms, as you will see below.) If S and T are sets
such that every element of S is also an element of T, then S is a subset of
T, written S ⊂T. It is a proper subset if S ⊂T but S ̸= T. The notation
T ⊃S means S ⊂T. Clearly, S = T if and only if S ⊂T and T ⊂S.
The axioms for sets describe precisely what sets can be asserted to exist,
and what properties they have. Here is the ﬁrst one.
• Specification axiom: Given a set S and a sentence P(x) that is
either true or false whenever x is any particular element of S, there
is a set consisting of all those x ∈S for which P(x) is true, denoted
by {x ∈S : P(x)}.
Note that one must start with a speciﬁc set before the speciﬁcation
axiom can be used. This requirement rules out forming sets out of self-
contradictory speciﬁcations such as the one discovered by Bertrand Russell

Set Theory
339
and now known as “Russell’s paradox”: The sentence C = {X : X ̸∈X}
looks as if it might deﬁne a set, but it does not, because each statement
C ∈C and C ̸∈C implies its own negation. Similarly, the speciﬁcation axiom
implies that there does not exist a “set of all sets,” for if there were such a
set S, we could use the speciﬁcation axiom to deﬁne C = {S ∈S : S ̸∈S}
and reach the same contradiction.
Still, there are times when we will need to speak of “all sets” or other
similar aggregations, primarily in the context of category theory (see Chap-
ter 7). For this purpose, we reserve the word class to refer to an aggregate
of mathematical objects that may or may not constitute a set.
• Power set axiom: Given any set S, there is a set P(S), called the
power set of S, whose elements are exactly the subsets of S.
• Union axiom: Given any collection C of sets, there is a set called
their union and denoted by  C, with the property that x ∈ C if
and only if x ∈S for some S ∈C.
Given any nonempty collection C of sets, their intersection, denoted by
	 C, is deﬁned as the set

C = {x ∈ C : x ∈S for every S ∈C}.
Other notations for unions and intersections are

S∈C
S;
S1 ∪S2 ∪· · · ;

S∈C
S;
S1 ∩S2 ∩· · · .
Given any collection C of sets, if A∩B = ∅whenever A, B ∈C and A ̸= B,
the sets in C are said to be disjoint.
If A and B are any sets, their set diﬀerence is deﬁned to be the set
A ∖B = {x ∈A : x ̸∈B},
which exists by the speciﬁcation axiom. If B ⊂A, the set diﬀerence A ∖B
is also called the complement of B in A.
When sets are deﬁned by speciﬁcation, it is common to abbreviate the
notation in certain circumstances if it can be done unambiguously. For ex-
ample, if the elements of a set can be named explicitly, the set is commonly
speciﬁed simply by listing its elements, as in {a1, a2, . . . , ak}. As long as
each of the elements ai is an element of some other set Si, this is a legit-
imate use of our axioms and can be interpreted as {x ∈S1 ∪· · · ∪Sk :
x = a1 or x = a2 or . . . or x = ak}. Since the resulting set is the same
regardless of what sets Si the ai’s originally came from, there is no need to
include them in the notation. A set {a} with a unique element a is called
a singleton.

340
Appendix: Review of Prerequisites
Cartesian Products, Relations, and Functions
Another primitive concept that we will use without a formal deﬁnition is
that of an ordered pair. Think of it as a pair of objects in a speciﬁc order,
indicated by writing them in parentheses and separated by a comma, as in
(a, b). The objects a and b are called the components of the ordered pair.
The deﬁning characteristic is that two ordered pairs are equal if and only
if their ﬁrst components are equal and their second components are equal:
(a, b) = (a′, b′) ⇐⇒a = a′ and b = b′.
• Cartesian product axiom: Given sets A and B, there exists a set
A × B, called their Cartesian product, whose members are precisely
the ordered pairs (a, b) for every a ∈A and b ∈B.
With these axioms we can deﬁne the most important constructions in
mathematics: relations and functions. A relation between sets X and Y is
a subset of X × Y . If r is a relation, it is often convenient to use some
notation such as x r⃝y to mean (x, y) ∈r. For example, both “equals” and
“less than” are relations in R × R.
An important special case arises when we consider relations between a
set S and itself, which we usually call a relation “on S.” Let ∼denote such
a relation. It is said to be reﬂexive if x ∼x for all x ∈S, symmetric if
x ∼y implies y ∼x, and transitive if x ∼y and y ∼z imply x ∼z. A
relation that is reﬂexive, symmetric, and transitive is called an equivalence
relation. Given an equivalence relation ∼, for each x ∈S the equivalence
class of x is deﬁned to be the set
[x] = {y ∈S : y ∼x}.
The set of equivalence classes is denoted by S/∼.
Closely related to equivalence relations is the following notion: A parti-
tion of a set S is a collection C of disjoint nonempty subsets of S whose
union is S. In this situation one also says that S is the disjoint union of
the sets in C.
Exercise A.1.
Given an equivalence relation ∼on a set S, show that
the set S/∼of equivalence classes is a partition of S. Conversely, given a
partition of S, show that there is a unique equivalence relation whose set of
equivalence classes is exactly the original partition.
If r is any relation on a set S, the next exercise shows that there is a
“smallest” equivalence relation ∼such that x r⃝y =⇒x ∼y. It is called
the equivalence relation generated by r.
Exercise A.2.
Let r ⊂X × X be any relation, and deﬁne ∼to be the
intersection of all equivalence relations in X × X that contain r.
(a) Show that ∼is an equivalence relation.

Set Theory
341
(b) Show that x ∼y if and only if one of the following is true: x = y,
x r⃝′ y, or there is a ﬁnite sequence of elements z1, . . . , zn ∈X such
that x r⃝′ z1 r⃝′ · · · r⃝′ zn r⃝′ y, where x r⃝′ y means “x r⃝y or y r⃝x.”
(See below for the formal deﬁnition of a ﬁnite sequence.)
Another particularly important type of relation is a partial ordering: This
is a relation ≤on a set X that is reﬂexive, transitive, and antisymmetric,
which means that x ≤y and y ≤x together imply x = y. If in addition
every pair x, y ∈X satisfy either x ≤y or y ≤x, it is called a total ordering
(or sometimes a linear or simple ordering). The notation x < y is deﬁned to
mean x ≤y and x ̸= y, and the notations x > y and x ≥y have the obvious
meanings. If X is a set endowed with an ordering, one often says that X
is a (totally or partially) ordered set, with the ordering being understood
from the context.
The most common examples of totally ordered sets are number systems
such as the real numbers or the integers (which we will introduce formally
below). An important example of a partially ordered set is the set P(S) of
subsets of a given set S, with the partial order relation deﬁned by inclusion:
X ≤Y if and only if X ⊂Y . It is easy to see that any subset of a partially
ordered set is itself partially ordered with (the restriction of) the same
order relation, and if the original ordering is total, then the subset is also
totally ordered.
If X is a partially ordered set and S ⊂X is any subset, an element
x ∈X is said to be an upper bound for S if x ≥s for every s ∈S. If
S has an upper bound, it is said to be bounded above. The terms lower
bound and bounded below are deﬁned similarly. An element s ∈S is said
to be maximal if there is no s′ ∈S such that s′ > s, and it is the largest
element of S if s′ ≤s for every s′ ∈S. Minimal and smallest elements are
deﬁned similarly. Clearly, the largest element of S, if it exists, is unique
and maximal. If S is totally ordered, a maximal element is automatically
largest; but in a partially ordered set this may not be the case, because
there may be elements that are neither larger nor smaller than s. A totally
ordered set X is said to be well-ordered if every nonempty subset S ⊂X has
a smallest element. For example, the set of natural numbers is well-ordered,
but the integers and the real numbers are not.
A function from X to Y is a relation f ⊂X × Y with the property
that for every x ∈X there is a unique y ∈Y such that (x, y) ∈f. This
unique element of Y is denoted by f(x). The sets X and Y are called the
domain and range of f, respectively. The words map and mapping are used
synonymously for function.
The notation f : X →Y means “f is a function from X to Y ” (or,
depending on how it is used in a sentence, “f, a function from X to Y ,”
or “f, from X to Y ”). The equation y = f(x) is also sometimes written
f : x 
→y or, if the name of the function is not important, x 
→y. Note
that the type of arrow (
→) used to denote the action of a function on an

342
Appendix: Review of Prerequisites
element of its domain is diﬀerent from the arrow (→) used between the
domain and range.
Given two functions f : X →Y and g: Y →Z, their composition is the
function g ◦f : X →Z deﬁned by (g ◦f)(x) = g(f(x)).
For every set X, there exists a natural function IdX : X →X called
the identity map of X, deﬁned by f(x) = x for all x ∈X. If S ⊂X is a
subset, there is a function ιS : S →X called the inclusion map of S, given
by ιS(x) = x for x ∈S. We sometimes use the notation ιS : S 	→X to
emphasize the fact that it is an inclusion map. If f : X →Y and S is a
subset of X, there is a function f|S : S →Y called the restriction of f to S,
obtained by applying f only to elements of S. In terms of ordered pairs, f|S
is just the subset of S × Y consisting of ordered pairs (x, y) ∈f such that
x ∈S. It is immediate that f|S = f ◦ιS, and ιS is just the restriction of
IdX to S. If g: S →Y is a map and f : X →Y is a map whose restriction
to S is equal to g, we say that f is an extension of g.
Let f : X →Y be a function. If S ⊂X, the image of S under f is the
set
f(S) = {y ∈Y : y = f(x) for some x ∈S}.
The set f(X) ⊂Y , the image of the entire domain X, is just called the
image of f. (Warning: In analysis it is common to use the word “range” to
denote what we call the image of a function, and the word “codomain” to
denote what we call its range.) If B is a subset of Y , the inverse image of
B, denoted by f −1(B), is the set
f −1(B) = {x ∈X : f(x) ∈B}.
If B = {b} is a singleton, it is common to use the notation f −1(b) in place
of the more accurate but more cumbersome f −1({b}).
Exercise A.3.
Let f : X →Y be a map.
(a) If A ⊂B ⊂Y , then f −1(A) ⊂f −1(B).
(b) If B ⊂Y , then f −1(Y ∖B) = X ∖f −1(B).
(c) Give a counterexample to show that it is not generally true that f(X ∖
A) = Y ∖f(A) whenever A ⊂X.
The function f is said to be injective or one-to-one if f(x) = f(y) implies
x = y. It is said to be surjective or to map X onto Y if f(X) = Y , or in
other words if every y ∈Y is equal to f(x) for some x ∈X. A function
that is both injective and surjective is said to be bijective or a one-to-
one correspondence. A bijective map from a set X to itself is also called a
permutation of X.
Given f : X →Y , if there exists a map g: Y →X such that f ◦g = IdY
and g ◦f = IdX, then g is said to be an inverse for f. Since inverses are

Set Theory
343
unique (see the next exercise), the inverse map is denoted unambiguously
by f −1 when it exists. More generally, if g satisﬁes only g ◦f = IdX, it is
called a left inverse for f, and if f ◦g = IdY , g is a right inverse for f.
Lemma A.1. If f : X →Y is a function and X ̸= ∅, then f has a left
inverse if and only if it is injective, and a right inverse if and only if it is
surjective.
Proof. Suppose g is a left inverse for f. If f(x) = f(x′), applying g to both
sides implies x = x′, so f is injective. Similarly, if g is a right inverse and
y ∈Y is arbitrary, then f(g(y)) = y, so f is surjective.
Now suppose f is injective. Choose any x0 ∈X, and deﬁne g: Y →X
by g(y) = x if y ∈f(X) and y = f(x), and g(y) = x0 if y ̸∈f(X). It
is immediate that g ◦f = IdX. The proof that surjectivity implies the
existence of a right inverse requires the axiom of choice, so we postpone it
until the end of the section (Exercise A.8).
Exercise A.4.
Let f be a function.
(a) Show that f has an inverse if and only if it is bijective.
(b) If f has an inverse, show that it is unique.
Number Systems and Cardinality
So far, all the set-theoretic axioms we have introduced describe ways of
obtaining new sets from already existing ones. Before the theory will have
much content, we need to know that some sets exist. We take the set of real
numbers as our starting point. The properties that characterize it are that
it is an ordered ﬁeld (a ﬁeld in the algebraic sense, endowed with a total
ordering in which y < z =⇒x + y < x + z and x > 0, y > 0 =⇒xy > 0)
that is complete (every nonempty subset with an upper bound has a least
upper bound).
• Existence axiom: There exists a complete ordered ﬁeld R, called
the real numbers.
Because this axiom guarantees the existence of at least one set, we now
can assert the existence of the empty set, since {x ∈R : x ̸= x} = ∅.
Exercise A.5.
Show that the real numbers are unique, in the sense that
any complete ordered ﬁeld admits an order-preserving isomorphism with R.
Let S ⊂R be a nonempty subset with an upper bound. The least upper
bound of S is also called the supremum of S, and is denoted by sup S.
Similarly, any nonempty set T with a lower bound has a greatest lower
bound, also called its inﬁmum and denoted by inf T.
We will work extensively with the usual subsets of R:

344
Appendix: Review of Prerequisites
• The set of natural numbers N (the positive counting numbers), deﬁned
as the smallest subset of R containing 1 and containing n+1 whenever
it contains n.
• The set of integers Z = {n ∈R : n = 0 or n ∈N or −n ∈N}.
• The set of rational numbers Q = {x ∈R : x = p/q for some p, q ∈Z}.
We consider the set C of complex numbers to be simply R × R, in which
the real numbers are identiﬁed with the subset R×{0} ⊂C and i stands for
the imaginary unit (0, 1). Multiplication and addition of complex numbers
are deﬁned by the usual rules with i2 = −1; thus x+iy is another notation
for (x, y).
For any pair of integers m ≤n, the notation {m, . . . , n} means {k ∈
Z : m ≤k ≤n}. For subsets of the real numbers, we use the following
notation:
[a, b] = {x ∈R : a ≤x ≤b},
(a, b) = {x ∈R : a < x < b},
[a, b) = {x ∈R : a ≤x < b},
(a, b] = {x ∈R : a < x ≤b}.
We also allow a or b or both to be replaced by either of the symbols ∞or
−∞in any of the above deﬁnitions in which it makes sense, with the obvious
meanings. A nonempty subset J ⊂R is called an interval if whenever
a, b ∈J, every c such that a < c < b is also in J.
Exercise A.6.
Show that an interval must be one of the nine types of sets
[a, b], (a, b), [a, b), (a, b], (−∞, b], (−∞, b), [a, ∞), (a, ∞), or (−∞, ∞).
The natural numbers play a special role in set theory, as a yardstick for
measuring sizes of sets. Two sets are said to have the same cardinality if
there exists a one-to-one correspondence between them. A set is ﬁnite if
it is empty or has the same cardinality as {1, . . . , n} for some n ∈N (in
which case it is said to have cardinality n), and otherwise it is inﬁnite. A
set is countably inﬁnite if it has the same cardinality as N, countable if it is
either ﬁnite or countably inﬁnite, and uncountable otherwise. The sets N,
Z, and Q are countable, but R and C are not.
Exercise A.7.
(a) Prove that the union of a countable collection of countable sets is
countable.
(b) Prove that any subset of a countable set is countable.

Set Theory
345
Indexed Collections
Using what we have introduced so far, it is easy to extend the notion of
ordered pair. Given a natural number n and a set S, an ordered n-tuple
of elements of S is a function x: {1, . . . , n} →S. It is customary to write
xi instead of x(i) for the value of x at i, and the whole n-tuple can be
written (x1, . . . , xn) or {xi : i = 1, . . . , n} or {xi}n
i=1. Similarly, a sequence
of elements of S is a function x: N →S, written {x1, x2, . . . } or {xi : i ∈N}
or {xi}∞
i=1. An ordered n-tuple is sometimes called a ﬁnite sequence.
A subsequence of a sequence {xi}i∈N in a set S is a sequence of the
form {xf(j)}j∈N, where f : N →N is a function that is strictly increasing,
meaning that i < j implies f(i) < f(j). We usually write ij for f(j).
We sometimes need to deal with collections of objects that are indexed,
not by the natural numbers or subsets of them, but by arbitrary sets,
potentially even uncountable ones. An indexed collection of elements of S
is just a function from a set A (called the index set) to S, and in this context
is denoted by {xα : α ∈A} or {xα}α∈A. Occasionally, when the index set
is understood or is irrelevant, we will omit it from the notation and simply
write {xα}. If {Xα}α∈A is an indexed collection of sets, 
α∈A Xα is just
another notation for the union of the (unindexed) collection {X ∈S : X =
Xα for some α ∈A}, where S is the range of the indexing function. If the
index set is ﬁnite, the union is usually written as X1 ∪· · · ∪Xn. A similar
remark applies to the intersection 	
α∈A Xα or X1 ∩· · · ∩Xn.
Earlier we mentioned that given a set S and a partition of it, S is said
to be the disjoint union of the sets in the partition. It sometimes happens
that we are given a collection of sets, which may or may not be disjoint, but
which we want to consider as disjoint subsets of a larger set. For example,
we might want to form a set consisting of “ﬁve copies of R,” in which
we consider the diﬀerent copies to be disjoint from each other. We can
accomplish this by the following trick. Suppose {Xα}α∈A is an indexed
collection of nonempty sets. If we imagine “tagging” each element of Xα
with its index α, we can make the sets Xα and Xβ disjoint when α ̸= β,
even if they were not disjoint to begin with. Formally, an element x with
a tag α is just an ordered pair (x, α). Thus we deﬁne the disjoint union of
the indexed collection, denoted by 
α∈A Xα, to be the set

α∈A
Xα = {(x, α) : α ∈A and x ∈Xα}.
If the index set is ﬁnite, the disjoint union is usually written as X1⨿· · ·⨿Xn.
For each set Xα, there is a natural injective map ια : Xα →
α∈A Xα,
given by ια(x) = (x, α). The images of these maps are disjoint from each
other, so we can identify each set Xα with its image under ια. In practice,
we think of each Xα as a subset of the disjoint union and think of the
injection ια as an inclusion map. With this convention, this usage of the
term disjoint union is consistent with our previous one.

346
Appendix: Review of Prerequisites
The deﬁnition of Cartesian product now extends easily from two sets
to arbitrarily many. If (X1, . . . , Xn) is an ordered n-tuple of sets, their
Cartesian product X1 × · · · × Xn is just the set of all ordered n-tuples
(x1, . . . , xn) such that xi ∈Xi for i = 1, . . . , n. (To be sure we are strictly
following the axioms, we should note that this is a subset of the set of all
functions from {1, . . . , n} to X1 ∪· · · ∪Xn, which in turn is a subset of the
power set of {1, . . . , n} × (X1 ∪· · · ∪Xn).) If X1 = · · · = Xn = X, the
n-fold Cartesian product X × · · · × X is often written simply as Xn.
A Cartesian product comes equipped with projection maps πi : X1 ×
· · · × Xn →Xi, deﬁned by πi(x1, . . . , xn) = xi. It is easy to see that each
of these maps is surjective. If f : S →X1 × · · · × Xn is any function into a
Cartesian product, the composite functions fi = πi ◦f : S →Xi are called
its component functions. Any such function f is completely determined by
its component functions, by the formula
f(y) = (f1(y), . . . , fn(y)).
More generally, the Cartesian product of an arbitrary indexed collection
{Xα}α∈A of sets is deﬁned to be the set of all functions x: A →
α∈A Xα
such that xα ∈Xα for each α. It is denoted by 
α∈A Xα. Just as in the case
of ﬁnite products, any Cartesian product comes equipped with projection
maps πβ : 
α∈A Xα →Xβ, deﬁned by πβ(x) = xβ.
Our last set-theoretic axiom asserts that it is possible to choose an ele-
ment from each set in an arbitrary indexed collection.
• Axiom of choice: Given any nonempty indexed collection {Xα}α∈A
of nonempty sets, there exists a function c: A →
α∈A Xα, called a
choice function, such that c(α) ∈Xα for each α.
In other words, the Cartesian product of any nonempty indexed collection
of nonempty sets is nonempty.
Here are two immediate applications of the axiom of choice.
Exercise A.8.
Complete the proof of Lemma A.1 by showing that f is
surjective if and only if it has a right inverse.
Exercise A.9.
If there exists a surjective map from a countable set onto
S, prove that S is countable.
The axiom of choice has a number of interesting equivalent reformula-
tions; the relationships among them make fascinating reading, for example
in [Hal74]. The only other formulations we will make use of are the follow-
ing two (the well-ordering theorem in Problem 4-6, and Zorn’s lemma in
the proof of Lemma 13.36).
Theorem A.2 (The Well-Ordering Theorem).
Every
set
can
be
given a total ordering that is well-ordered.

Metric Spaces
347
Theorem A.3 (Zorn’s Lemma).
Let X be a partially ordered set in
which every totally ordered subset has an upper bound. Then X has a max-
imal element.
For proofs, see [Hal74] or [Dev93].
Metric Spaces
Metric spaces play an indispensable role in real analysis, and their proper-
ties provide the underlying motivation for most of the basic deﬁnitions in
topology. In this section we summarize the important properties of metric
spaces with which you should be familiar. For a thorough treatment of the
subject, see any good undergraduate real analysis text such as [Rud76].
Euclidean Spaces
Most of topology, in particular manifold theory, is modeled on the behavior
of Euclidean spaces and their subsets, so we begin with a quick review of
their properties.
The Cartesian product Rn = R × · · · × R of n copies of the real line is
known as n-dimensional Euclidean space. It is the set of ordered n-tuples
of real numbers. A point in Rn is denoted by (x1, . . . , xn) or simply x.
The numbers xi are called its components or coordinates. Zero-dimensional
Euclidean space R0 is, by convention, the singleton {0}.
We will use without further comment the fact that Rn is an n-dimensional
vector space with the usual operations of scalar multiplication and vector
addition. The geometric properties of Rn are derived from the Euclidean
dot product x · y = x1y1 + · · · + xnyn. In particular, the norm or length of
a vector x ∈Rn is given by
|x| = (x · x)1/2 =

(x1)2 + · · · + (xn)2
1/2 .
The angle between two nonzero vectors x, y is deﬁned to be cos−1(x ·
y)/(|x| |y|). Given two points x, y ∈Rn, the line segment between them
is the set {tx + (1 −t)y : 0 ≤t ≤1}.
Continuity and convergence in Euclidean spaces are deﬁned in the usual
ways. A map f : U →V between subsets of Euclidean spaces is continuous
if for any x ∈U and any ε > 0 there exists δ > 0 such that |x −y| < δ
implies |f(x) −f(y)| < ε. A sequence {xi} of points in Rn converges to
x ∈Rn if for any ε > 0 there exists N such that i ≥N implies |xi −x| < ε.
Metrics, Convergence, and Continuity
Metric spaces are generalizations of Euclidean spaces, in which none of the
vector space properties are present and only the distance function remains.

348
Appendix: Review of Prerequisites
If M is any set, a metric on M is a function d: M × M →R, also called a
distance function, satisfying the following three properties:
(i) Symmetry: For all x, y ∈M, d(x, y) = d(y, x).
(ii) Positivity: For all x, y ∈M, d(x, y) ≥0, and d(x, y) = 0 if and only
if x = y.
(iii) Triangle inequality: For all x, y, z ∈M, d(x, z) ≤d(x, y)+d(y, z).
The pair (M, d) is called a metric space. (Actually, unless it is important to
specify which metric is being considered, we often just say “M is a metric
space,” with the metric being understood from the context.)
Example A.4.
(a) If M is any subset of Rn, the function d(x, y) = |x −y| is a metric
on M (Exercise A.10), called the Euclidean metric. Whenever we
consider a subset of Rn as a metric space, unless we specify otherwise
it will always be with the Euclidean metric.
(b) Similarly, if M is any metric space and X is a subset of M, then X
inherits a metric simply by restricting the distance function of M to
points in X.
(c) If X is any set, deﬁne a metric on X by setting d(x, y) = 1 unless
x = y, in which case d(x, y) = 0. This is called the discrete metric on
X.
Exercise A.10.
Prove that d(x, y) = |x −y| is a metric on any subset of
Rn.
Here are some of the standard deﬁnitions used in metric space theory.
Let M be a metric space.
• For any x ∈M and r > 0, the (open) ball of radius r around x is the
set
Br(x) = {y ∈M : d(y, x) < r},
and the closed ball of radius r around x is
Br(x) = {y ∈M : d(y, x) ≤r}.
• Given a subset A ⊂M, a point x ∈M is said to be a limit point (or
accumulation point or cluster point) of A if every open ball around x
contains a point of A other than x.
• A set A ⊂M is said to be open if it contains an open ball around
each of its points.

Metric Spaces
349
• A set A ⊂M is said to be closed if it contains all its limit points.
• The diameter of a set A ⊂M is sup{d(x, y) : x, y ∈A} (which may
be inﬁnite).
• A set A ⊂M is said to be bounded if it has ﬁnite diameter.
Exercise A.11.
Let M be a metric space.
(a) Show that A ⊂M is open if and only if M ∖A is closed.
(b) Show that an open ball in M is an open set, and a closed ball in M is
a closed set.
(c) Show that the union of an arbitrary collection of open sets is open,
and the intersection of ﬁnitely many open sets is open.
(d) Show that the intersection of an arbitrary collection of closed sets is
closed, and the union of ﬁnitely many closed sets is closed.
(e) Show that a subset of M is bounded if and only if it is contained in an
open ball if and only if it is contained in a closed ball.
Exercise A.12.
In each part below, a subset S of a metric space M is
given. In each case, decide whether S is open, closed, both, or neither.
(a) M = R, and S = [0, 1).
(b) M = R, and S = N.
(c) M = Z, and S = N.
(d) M = R2, and S is the set of points with rational coordinates.
(e) M = R2, and S is the unit disk {(x, y) ∈R2 : x2 + y2 < 1}.
(f) M = R3, and S is the unit disk {(x, y, z) ∈R3 : z = 0 and x2+y2 < 1}.
(g) M = {(x, y) ∈R2 : x > 0 and y > 0}, and S = {(x, y) ∈M : x2 +y2 ≤
1}.
The deﬁnition of continuity in the context of metric spaces is a straight-
forward generalization of the Euclidean deﬁnition. If (M1, d1) and (M2, d2)
are metric spaces, a map f : M1 →M2 is said to be continuous if for ev-
ery x ∈M1 and every ε > 0, there exists δ > 0 such that d1(x, y) < δ
implies d2(f(x), f(y)) < ε. Similarly, if {xi} is a sequence of points in a
metric space (M, d), it is said to converge to x ∈M, written xi →x or
limi→∞xi = x, if for any ε > 0 there exists N such that i ≥N implies
d(xi, x) < ε.
Exercise A.13.
If M and N are metric spaces and f : M →N is a map,
show that f is continuous if and only if it takes convergent sequences to
convergent sequences, i.e., if and only if xi →y in M implies f(xi) →f(y)
in N.

350
Appendix: Review of Prerequisites
Exercise A.14.
Show that a subset A of a metric space M is closed if and
only if, whenever {xi} is a sequence of points in A that converges in M, the
limit lies in A.
A sequence {xi} in a metric space is said to be Cauchy if for every ε > 0,
there exists N such that i, j ≥N implies d(xi, xj) < ε. Every convergent
sequence is Cauchy (Exercise A.15), but the converse is not true in general.
A metric space in which every Cauchy sequence converges is said to be
complete.
Exercise A.15.
Prove that every convergent sequence in a metric space
is Cauchy.
The following criterion for continuity is frequently useful (and in fact,
as is explained in Chapter 2, is the main motivation for the deﬁnition of a
topological space).
Lemma A.5 (Open Set Criterion for Continuity).
A
map
f : M1 →M2 between metric spaces is continuous if and only if the
inverse image of every open set is open: Whenever U is an open subset of
M2, f −1(U) is open in M1.
Exercise A.16.
Prove Lemma A.5
Compactness
Let M be a metric space and K a subset of M. An open cover of K is
a collection {Uα}α∈A of open subsets of M whose union contains K. A
subcover is a subcollection that is still an open cover of K. A subset of M
is said to be compact if every open cover has a ﬁnite subcover.
Two properties of compact sets—closedness and boundedness—follow
immediately from the deﬁnition.
Proposition A.6. Any compact subset of a metric space is closed and
bounded.
Proof. Let K ⊂M be compact, and let x be any point in K. The collection
of open balls {Br(x) : r > 0} is an open cover of K, which therefore must
have a ﬁnite subcover. Letting R be the radius of the largest of these ﬁnitely
many balls, it follows that K ⊂BR(x), which means that it is bounded.
To show that K is closed, we will show that its complement is open. Let q
be any point of M ∖K. For each p ∈K, let δ(p) = d(p, q)/2; then the balls
Bδ(p)(q) and Bδ(p)(p) are disjoint by the triangle inequality. The collection
{Bδ(p)(p) : p ∈K} is an open cover of K, and therefore has a ﬁnite sub-
cover, say {Bδ(p1)(p1), . . . , Bδ(pk)(pk)}. Now let r = min{δ(p1), . . . , δ(pk)}.
Since Br(q) is disjoint from each of the balls Bδ(pi)(pi) and these balls
cover K, it is disjoint from K. In other words, there is a ball around each
q ∈M ∖K contained in M ∖K, so M ∖K is open and thus K is closed.

Metric Spaces
351
In Rn, the converse of this proposition is true. Before proving this result
(the Heine–Borel theorem below), we need a preliminary lemma.
For any point x ∈Rn and any r > 0, the closed cube of side r around x
is the set
Cr(x) = {y ∈Rn : |xi −yi| ≤r/2, i = 1, . . . , n}.
It is easy to check that the diameter of Cr(x) is r√n.
Lemma A.7. Suppose {Ci}∞
i=1 is a sequence of closed cubes in Rn that
are nested, in the sense that C1 ⊃C2 ⊃· · · . Then 	
k Ck is not empty.
Proof. First consider the case n = 1, in which case the cubes are just
closed intervals. Writing the intervals as Ck = [ak, bk], the fact that they
are nested means that a1 ≤a2 ≤· · · ≤ak < bk ≤bk−1 ≤· · · ≤b2 ≤b1.
Let a = sup{ak} and b = inf{bk}. Then clearly, ak ≤a ≤b ≤bk for each
k, so the interval [a, b] (or the point a if a = b) is contained in 	
k Ck.
For general n, just apply the preceding argument to each coordinate.
Theorem A.8 (The Heine–Borel Theorem).
Every
closed
and
bounded subset of Rn is compact.
Proof. We begin by showing that any closed cube in Rn is compact. Let
C be a closed cube of side r, and let U be an open cover of C. Suppose
U has no ﬁnite subcover. Subdividing each of the sides of C in half yields
a decomposition of C into 2n closed cubes of side r/2 whose union is C.
If each of these 2n cubes were covered by ﬁnitely many sets of U, then
putting together these 2n ﬁnite collections of open sets would give a ﬁnite
subcover of C; thus at least one of them must not be covered by any ﬁnite
subcollection of sets from U. Call this smaller cube C1. If we subdivide C1
in the same way, one of the 2n cubes in this subdivision must not admit a
ﬁnite subcover by the same reasoning. Continuing by induction, we obtain
a nested sequence of cubes C = C0 ⊃C1 ⊃· · · with the property that no
Ck is covered by any ﬁnite collection of sets from U. Each cube Ck has side
length r/2k.
By Lemma A.7, there is a point x ∈	
k Ck. Because U is a cover of C, x
must be in one of the sets of U, say x ∈U0. Because U0 is open, there is a
ball Bε(x) ⊂U0. Because Ck has diameter r√n/2k and x ∈Ck, as soon as
k is suﬃciently large Ck ⊂Bε(x) ⊂U0, which contradicts the fact that Ck
cannot be covered by ﬁnitely many sets of U. This proves that any cube is
compact.
Now suppose K ⊂Rn is any closed and bounded subset. Because it is
bounded, it is contained in some cube Cr(0). If U is an open cover of K,
the collection U∪{Rn∖K} is an open cover of Cr(0). (Here we use the fact
that K is closed.) Finitely many of these sets, say {U1, . . . , Um, Rn ∖K},
cover Cr(0), and then it is clear that {U1, . . . , Um} cover K.

352
Appendix: Review of Prerequisites
The Heine–Borel theorem is not true if Rn is replaced by a general metric
space, as the following exercise shows.
Exercise A.17.
(a) In Z with the discrete metric, show that any inﬁnite subset is closed
and bounded, but not compact.
(b) Similarly, in the metric space (0, ∞), show that the set (0, 1
2] is closed
and bounded, but the open cover of it by intervals of the form (1/n, 1)
for n ∈N has no ﬁnite subcover.
Most of the applications of compactness depend on the following theo-
rem.
Theorem A.9. If M and N are metric spaces, f : M →N is continuous,
and K ⊂M is compact, then f(K) is compact.
Exercise A.18.
Prove Theorem A.9.
For example, the following theorem is of fundamental importance in real
analysis.
Theorem A.10 (Euclidean Extreme Value Theorem).
Any contin-
uous real-valued function on a closed and bounded subset of Rn attains its
maximum and minimum values.
Proof. Let f : K →R be such a function. Since K is closed and bounded, it
is compact by the Heine–Borel theorem. By the preceding theorem, f(K) is
compact and therefore closed and bounded in R. In particular, it contains
its supremum and inﬁmum.
Group Theory
We will assume only basic group theory such as one is likely to encounter in
most undergraduate algebra courses. You can ﬁnd much more detail about
all of this material in, for example, [Hun90] or [Her75].
Basic Deﬁnitions
A group is a set G together with a map G × G →G, usually called multi-
plication and written (g, h) 
→gh, satisfying
(i) Associativity: For all g, h, k ∈G, (gh)k = g(hk).
(ii) Existence of identity: There is an element 1 ∈G such that 1g =
g1 = g for all g ∈G.

Group Theory
353
(iii) Existence of inverses: For each g ∈G, there is an element h ∈G
such that gh = hg = 1.
The order of a group G is its cardinality as a set. The trivial group is the
unique group of order 1; it is the group consisting of the identity alone. One
checks easily that the inverse of any element is unique (so the usual notation
g−1 for inverses makes sense), and that (gh)−1 = h−1g−1. Similarly, the
identity is unique.
A group G is said to be abelian if gh = hg for all g, h ∈G. The group
operation in an abelian group is frequently written additively, (g, h) 
→
g + h, in which case the identity element is denoted by 0 and the inverse
of g is denoted by −g.
A subset of G that is itself a group with the same multiplication is called
a subgroup of G. Clearly, a subset is a subgroup if and only if it is closed
under multiplication and contains the inverse of each of its elements.
If S is any set, the set of permutations of S is a group under composition,
called the permutation group of S. In particular, if S is a ﬁnite set, any
permutation of S can be factored as a product of transpositions, which
are permutations that interchange two elements and leave all others ﬁxed.
The factorization into transpositions is not uniquely determined, but the
parity (evenness or oddness) of the number of transpositions is the same
for every such factorization. A permutation is called even or odd depending
on whether it decomposes into an even or odd number of transpositions.
Exercise A.19.
Let Sn denote the group of permutations of the set
{1, . . . , n}, called the symmetric group on n elements.
(a) Show that the map sgn: Sn →{±1} given by
sgn(s) =

+1
if s is even,
−1
if s is odd
is a surjective homomorphism. (Here we consider {±1} as a group
under multiplication.)
(b) Show that every element of Sn can be written as a product of trans-
positions of the following type:
sk(k) = k + 1;
sk(k + 1) = k;
sk(i) = i
if i ̸= k or k + 1.
If G1, . . . , Gn are groups, their direct product is the set G1 × · · · × Gn
with the group structure deﬁned by the multiplication law
(g1, . . . , gn)(g′
1, . . . , g′
n) = (g1g′
1, . . . , gng′
n)
and with identity element (1, . . . , 1). More generally, the direct product of
an arbitrary indexed collection of groups {Gα}α∈A is the Cartesian product
set 
α∈A Gα with multiplication deﬁned componentwise: (gg′)α = gαg′
α.

354
Appendix: Review of Prerequisites
A map f : G →H between groups is called a homomorphism if it pre-
serves multiplication: f(gh) = f(g)f(h). The image of f is f(G) ⊂H, often
written Im f, and its kernel is the set f −1(1), denoted by Ker f. A bijective
homomorphism is called an isomorphism. An isomorphism from G to itself
is called an automorphism.
Exercise A.20.
Let f : G →H be a homomorphism.
• Show that f is injective if and only if Ker f = {1}.
• If f is bijective, show that f −1 is also a homomorphism.
• Show that the image and the kernel of f are subgroups.
• If K ⊂G is a subgroup, show that f(K) is a subgroup of H.
An element g ∈G deﬁnes a map Cg : G →G by Cg(h) = ghg−1. This
map, called conjugation by g, is easily seen to be an automorphism of G,
so the image under Cg of any subgroup H ⊂G (written symbolically as
gHg−1) is another subgroup of G. Two subgroups H, H′ are conjugate if
H′ = gHg−1 for some g ∈G.
Exercise A.21.
Show that conjugacy is an equivalence relation on the set
of all subgroups of G.
The set of subgroups conjugate to a given subgroup H ⊂G is called the
conjugacy class of H.
Cosets and Quotient Groups
Given a subgroup H ⊂G and an element g ∈G, the left coset of H
determined by g is the set
gH = {gh : h ∈H}.
The right coset Hg is deﬁned similarly. Deﬁne a relation called congruence
modulo H by declaring that g ≡g′ (mod H) if and only if g−1g′ ∈H.
Exercise A.22.
Show that congruence modulo H is an equivalence rela-
tion on G, and its equivalence classes are precisely the left cosets of H.
The set of left cosets of H in G is denoted by G/H. (This is just the
partition of G deﬁned by congruence modulo H.) The cardinality of G/H
is called the index of H in G.
A subgroup K ⊂G is said to be normal if it is invariant under all
conjugations, that is if gKg−1 = K for all g ∈G. Clearly, every subgroup
of an abelian group is normal.
Exercise A.23.
Show that a subgroup K ⊂G is normal if and only if
gK = Kg for every g ∈G, so that every left coset of K is also a right coset.

Group Theory
355
Exercise A.24.
Show that the kernel of any homomorphism is a normal
subgroup.
Normal subgroups give rise to one of the most important constructions
in group theory. Given a normal subgroup K ⊂G, deﬁne a multiplication
operator on the set G/K of left cosets by
(gK)(g′K) = (gg′)K.
Lemma A.11. This multiplication is well-deﬁned on cosets and turns
G/K into a group.
Proof. First we need to show that the product does not depend on the
representatives chosen for the cosets: If gK = g′K and hK = h′K, then
(gh)K = (g′h′)K. From Exercise A.22, the fact that g and g′ determine the
same coset means that g−1g′ ∈K, which is the same as saying g′ = gk for
some k ∈K. Similarly, h′ = hk′ for k′ ∈K. Because K is normal, h−1kh is
an element of K. Writing this element as k′′, we have kh = hk′′. It follows
that
g′h′ = gkhk′ = ghk′′k′,
which shows that g′h′ and gh determine the same coset.
Now we just note that the group properties are satisﬁed: Associativity
of the multiplication in G/K follows from that of G; the element 1K = K
of G/K acts as an identity; and g−1K is the inverse of gK.
When K is a normal subgroup of G, the group G/K is called the quotient
group of G by K. The natural projection map π: G →G/K that sends each
element to its coset is a surjective homomorphism whose kernel is K.
The following lemma tells how to deﬁne homomorphisms from a quotient
group.
Lemma A.12. Let K ⊂G be a normal subgroup. Given a homomor-
phism f : G →H such that K ⊂Ker f, there is a unique homomorphism
f : G/K →H such that the following diagram commutes:
G
H
-
f
G/K.
?
π
f



(A.1)
(A diagram such as (A.1) is said to commute, or to be commutative, if
the maps between two spaces obtained by following arrows around either
side of the diagram are equal. So in this case commutativity means that
f ◦π = f.)

356
Appendix: Review of Prerequisites
Proof. Since π(g) = gK, if such a map exists, it has to be given by the
formula f(gK) = f(g); this proves uniqueness. To prove existence, we just
deﬁne f by this formula, so it obviously makes the diagram commute. It is
well-deﬁned, because if g ≡g′ (mod K), then g′ = gk for some k ∈K, and
therefore f(g′) = f(gk) = f(g)f(k) = f(g). It is clear from the deﬁnition
of multiplication in G/K that it is a homomorphism.
In the situation of the preceding lemma, we say that the homomorphism
f passes to the quotient or descends to the quotient.
The most important fact about quotient groups is the following result,
which says in essence that the projection onto a quotient group is the model
for all surjective homomorphisms.
Theorem A.13 (First [[Isomorphism]] Theorem).
Let G, H be groups,
and let f : G →H be a surjective homomorphism. Then K = Ker f is a
normal subgroup of G, and f induces an isomorphism f : G/K →H by
f(gK) = f(g).
Proof. From the preceding lemma, f(gK) = f(g) deﬁnes a homomorphism
f : G/K →H. Because f is surjective, f is surjective: For any h ∈H there
is an element g ∈G with f(g) = h, and then f(gK) = h. To show that f
is injective, suppose 1 = f(gK) = f(g). This means that g ∈Ker f = K,
so gK = K is the identity element of G/K.
Exercise A.25.
Suppose f : G →H is a surjective homomorphism, and
K ⊂G is a normal subgroup. Show that f(K) is normal in H.
Cyclic Groups
Let G be a group and g ∈G. The set ⟨g⟩= {gn : n ∈Z} is obviously
a subgroup of G, called the cyclic subgroup generated by g. The group G
is said to be cyclic if G = ⟨g⟩for some element g ∈G. In this case, the
element g is called a generator of G.
Example A.14 (Cyclic Groups).
(a) The group Z of integers (under addition) is an inﬁnite cyclic group
generated by 1.
(b) For any n ∈Z, the cyclic subgroup ⟨n⟩is normal because Z is abelian.
The quotient group Z/⟨n⟩is called the group of integers modulo n.
It is easily seen to be a cyclic group of order n, with the coset of 1 as
a generator.
Exercise A.26.
Show that any inﬁnite cyclic group is isomorphic to Z
and any ﬁnite cyclic group is isomorphic to Z/⟨n⟩, where n is the order of
the group.

Group Theory
357
Exercise A.27.
Show that every subgroup of a cyclic group is cyclic.
Exercise A.28.
If G is a cyclic group and f : G →G is any homomor-
phism, show there is an integer n such that f(γ) = γn for all γ ∈G. If G is
inﬁnite, show that n is uniquely determined by f.

References
[Dev93]
Keith Devlin. The Joy of Sets: Fundamentals of Contemporary
Set Theory. Springer-Verlag, New York, second edition, 1993.
[DH07]
Max Dehn and Poul Heegaard. Analysis situs. Enzyklop¨adie der
Math. Wiss., III.1.1:153–220, 1907.
[Die89]
Jean Dieudonn´e. A History of Algebraic and Diﬀerential Topol-
ogy 1900–1960. Birkh¨auser Boston, Cambridge, 1989.
[Fre82]
Michael Hartley Freedman.
The topology of four-dimensional
manifolds. J. Diﬀerential Geom., 17:357–453, 1982.
[Hal74]
Paul R. Halmos. Naive Set Theory. Springer-Verlag, New York,
1974.
[Her75]
Israel N. Herstein. Topics in Algebra. Wiley, New York, second
edition, 1975.
[Hun90]
Thomas W. Hungerford.
Abstract Algebra: An Introduction.
Saunders College Publishing, Philadelphia, 1990.
[Lee97]
John M. Lee. Riemannian Manifolds: An Introduction to Cur-
vature. Springer-Verlag, New York, 1997.
[LMM94] Silvio Levy, Delle Maxwell, and Tamara Munzer. Outside in.
The Geometry Center (video), 1994.

360
References
[Mas89]
William S. Massey.
Algebraic Topology: An Introduction.
Springer-Verlag, New York, 1989.
[Max77]
Nelson Max. Turning a sphere inside out. International Film
Bureau (video), 1977.
[Moi77]
Edwin E. Moise. Geometric Topology in Dimensions 2 and 3.
Springer-Verlag, New York, 1977.
[Mun75]
James R. Munkres. Topology: A First Course. Prentice–Hall,
Englewood Cliﬀs, New Jersey, 1975.
[Mun84]
James R. Munkres. Elements of Algebraic Topology. Addison–
Wesley, Reading, Massachusetts, 1984.
[Rad25]
Tibor Rad´o. ¨Uber den Begriﬀder Riemannschen Fl¨ache. Acta
Litt. Sci. Szeged., 2:101–121, 1925.
[Ran96]
A. A. Ranicki.
On the Hauptvermutung.
In A. A. Ranicki,
editor, The Hauptvermutung Book, volume 1 of K-Monographs in
Mathematics, pages 3–31. Kluwer Acad. Publ., Dordrecht, 1996.
[Rud76]
Walter Rudin. Principles of Mathematical Analysis. McGraw-
Hill, New York, third edition, 1976.
[Sco83]
Peter Scott. The geometries of 3-manifolds. Bull. London Math.
Soc., 15:401–487, 1983.
[SFL98]
John M. Sullivan, George Francis, and Stuart Levy. The opti-
verse. National Center for Supercomputing Applications (video),
1998.
[Sie92]
Allan J. Sieradski. An Introduction to Topology and [[Homotopy]].
PWS-Kent, Boston, 1992.
[Sma58]
Stephen Smale. A classiﬁcation of immersions of the two-sphere.
Trans. Amer. Math. Soc., 90:281–290, 1958.
[Sma61]
Stephen Smale. Generalized Poincar´e conjecture in dimensions
greater than 4. Ann. Math., 74:391–406, 1961.
[Spa89]
Edwin H. Spanier.
Algebraic Topology.
Springer-Verlag, New
York, 1989.
[Sti82]
John Stillwell. The word problem and the isomorphism problem
for groups. Bull. Amer. Math. Soc. (N.S.), 6:33–56, 1982.
[Sti93]
John Stillwell.
Classical Topology and Combinatorial Group
Theory. Springer-Verlag, New York, second edition, 1993.

References
361
[Thu97]
William P. Thurston. Three-dimensional geometry and topology,
volume 1. Princeton University Press, Princeton, 1997.
[Whi78]
George
W.
Whitehead.
Elements
of
[[Homotopy]]
Theory.
Springer-Verlag, New York, 1978.

Index
AB (category of abelian groups),
171
abelian
group, 203, 353
free, 204
groups, category of, 171
Lie group, 11
abelianization, 227
characteristic property, 227
functor, 231
of fundamental groups of
surfaces, 228
uniqueness, 231
absolute value, 20
abstract simplex, 96
abstract simplicial complex, 96
accumulation point, 26, 348
action
continuous, 60
free, 60
left, 59, 266
of a group, 59, 266
quotient by, 61
of fundamental group on
ﬁber, 245
proper, 266
right, 59
transitive, 60
aﬃne
chain, 293
hyperplane, 92
map, 92
singular simplex, 293
subspace, 92
algebra, fundamental theorem
of, 191
algebraic geometry, 11
algebraic topology, 6
algebraic variety, 12
algebraically closed, 11
algorithm, reduction, 196
ambient Euclidean space, 17
analysis situs, 4
angle, 7, 347
function, for a path in S1,
179, 182
angle-sum theorem, 7
antipodal map, 248, 321
degree of, 321
homotopic to identity, 322

Index
363
antisymmetric relation, 341
area, 7
associative, 352
associativity of path class
product, 153
automorphism group of covering,
248
automorphism of covering, 248
automorphism of group, 354
axiom
Cartesian product, 340
existence, 343
of choice, 346
power set, 339
speciﬁcation, 338
union, 339
axioms for set theory, 338–347
Bn (unit ball in Rn), 22
Baire category theorem, 85
ball
closed, 348
is a closed set, 349
is a manifold with
boundary, 62
Euclidean, 31
regular, 83
open, 348
is an open set, 349
unit, in Rn, 22
barycenter, 110
barycentric subdivision, 110, 315
base of covering, 234
base point, 151
change of, 154
nondegenerate, 212
based at a point, 151
basis
and continuity, 29
countable, 32
criterion, 27
for a topology, 29
for discrete topology, 29
for Euclidean topology, 29
for free abelian group, 204
for metric topology, 29
for product topology, 48, 50
for subspace topology, 42
for trivial topology, 29
in a set, 27
neighborhood, 32
countable, 32
of Euclidean balls, 38
standard, for Zn, 204
topology generated by, 27
belongs to a set, 338
Betti number, 328
big crunch, 14
bijective, 342
body, rigid, 13
bound
lower, 341
upper, 341
boundary, 25, 26
face, 93
manifold with, 34
of a boundary, 294
simplicial, 323
of a manifold with
boundary, 34, 38
of a simplex, 93
of a singular simplex, 293
operator, 297
simplicial, 323
singular, 293
simplicial, 324
singular, 294
topological, 35
bounded
above, 341
below, 341
not a topological property,
22
set, 349
bouquet of circles, 55
branch, 9
Brouwer ﬁxed point theorem,
192, 334
C (set of complex numbers), 344

364
Index
CPn (complex projective space),
62
Calabi–Yau manifold, 15
cardinality, 344
of ﬁbers of covering, 236,
247
Cartesian coordinates, 3
Cartesian product, 340, 346
axiom, 340
ﬁnite, 346
inﬁnite, 346
category, 170
ﬁrst, 86
homotopy, 173
of abelian groups, 171
of commutative rings, 171
of complex vector spaces,
171
of groups, 171
of real vector spaces, 171
of rings, 171
of sets, 171
of simplicial complexes, 171
of topological spaces, 171
pointed homotopy, 173
second, 86
theorem, Baire, 85
Cauchy sequence, 350
vs. convergent sequence, 350
center of a group, 208
center of gravity, 110
chain
aﬃne, 293
complex, 297
homology groups of, 297
group
simplicial, 323
singular, 293
homotopic, 303
homotopy, 303, 317
map, 297
simplicial, 323
singular, 293
change of base point, 154
characteristic property
abelianization, 227
disjoint union topology, 62
free abelian group, 204
free group, 200
free product, 198
product topology, 49
quotient topology, 56
subspace topology, 41
characteristic zero, 330
characterization of quotient
maps, 57
chart, 31
coordinate, 31
on a manifold with
boundary, 34
choice function, 346
choice, axiom of, 346
circle, 2, 45
as coset space of R, 61
fundamental group, 180
generating, 45
homotopy lifting property,
181
path lifting property, 181
representative, 157
unique lifting property, 181
unit, 45
class, 339
equivalence, 340
classical mechanics, 12
classiﬁcation
of 1-manifolds, 118
of 2-manifolds, 6, 137, 229
of 3-manifolds, 7
of n-manifolds, 7
of coverings, 283
of manifolds, 6
of surface presentations, 137
of surfaces, 6, 137, 229
of torus coverings, 286
closed
ball, 348
is a closed set, 349
is a manifold with
boundary, 62

Index
365
cube, 351
map, 27
lemma, 79
product of, 62
vs. homeomorphism, 27
set, 24, 26
and continuity, 25
and limit points, 26
in a compact space, 74
in a discrete space, 25
in a metric space, 349
in a subspace, 41
intersection, in a metric
space, 349
intersection, in a
topological space, 24
union, in a metric space,
349
union, in a topological
space, 24
closure, 25, 26
and sequences, 38
normal, 201
cluster point, 26, 348
coboundary, 329
operator, 329
cochain
complex, 329
map, 330
singular, 329
cocycle, 329
codomain, 342
coﬀee cup, 5
coherent topology, 99
of ﬁnite union, 114
cohomology
functor, 330
Mayer–Vietoris sequence,
335
singular, 329
topological invariance, 330
with ﬁeld coeﬃcients, 331,
332
collection, 338
combinatorial
equivalence, 112
group theory, 203
invariant, 113, 142
Euler characteristic, 113,
142
orientability, 115
commutative diagram, 355
commutative rings, category of,
171
commutator subgroup, 227
compact
implies closed and bounded,
350
limit point, 76
locally, 81
relatively, 82
sequentially, 77
set
continuous image, 73, 352
in a Hausdorﬀspace, 74
in a metric space, 350
topological space, 73
product of, 74
quotient of, 74
vs. limit point compact, 77,
78
vs. sequentially compact, 78
compactiﬁcation, one-point, 89
complement, 339
complementary edge pair, 139
complete
metric space, 350
ordered ﬁeld, 343
complex
analysis, 8
analytic, 8
chain, 297
general linear group, 10
manifold, 33
numbers, 344
projective space, 12, 62
simplicial
abstract, 96
category of, 171
Euclidean, 93

366
Index
special linear group, 11
vector spaces, category of,
171
component, 70, 347
functions, 346
is closed, 71
of ordered pair, 340
path, 72
composition, 342
continuity of, 20, 21
in a category, 170
of quotient maps, 53
cone, 110
on an aﬃne simplex, 315
conformal, 273
congruence modulo a subgroup,
354
conjugacy class, 354
conjugacy theorem, 243
conjugate subgroups, 354
conjugation, 354
connected
edge path, 101
interval, 68
locally, 72
locally path, 72
product space, 67
quotient space, 67
simply, 156
space, 65
subset, 66
of R, 68
sum, 126
covering of, 253
is a manifold, 126
polygonal presentation,
136
with sphere, 129
connecting homomorphism, 309,
310
naturality, 312
connectivity relation, 70
path, 71
consistent orientations, 107
consolidating, 134
constant loop, 151
constant map, continuity of, 21
continuity
and closed sets, 25
and convergent sequences,
38, 349
at a point, 21
between Euclidean spaces,
347
between metric spaces, 349
between topological spaces,
20
in terms of basis, 29
local criterion, 21
of composition, 20, 21
of constant map, 21
of identity map, 21
of restriction, 21
open set criterion, 350
continuous, see continuity
continuous deformation, 4
continuous group action, 60
continuous image
of compact set, 73
of connected set, 67
continuous map induced by a
simplicial map, 99
contractible space, 161
is simply connected, 162
singular homology of, 303
contravariant functor, 172
convergent sequence
in a metric space, 349
in a topological space, 20
in Euclidean space, 347
is Cauchy, 350
vs. continuity, 38, 349
convex, 69
hull, 92
set, 176
homeomorphic to ball, 80
simply connected, 156
coordinate, 347
coordinate chart, 31
corners, 23

Index
367
correspondence, one-to-one, 342
coset
left, 354
multiplication of, 355
right, 354
space, 61
countable
basis, 32
dense subset, 38
of Rn, 27
ﬁrst, 32
neighborhood basis, 32
second, 32
set, 344
subcover, 32
subset, 344
union, 344
countably inﬁnite, 344
counterclockwise, 107
covariant functor, 172
cover, 32
open, 32, 73
in a metric space, 350
of a subset, 73
covering
cardinality of ﬁbers, 236,
247
classiﬁcation, 283
group, 248
structure theorem, 250
transitivity, 249
homomorphism, 258
criterion, 260
is a covering map, 258
isomorphism, 258
isomorphism theorem, 260
map, 234
classiﬁcation, 283
is a local
homeomorphism, 235
is a quotient map, 235
is open, 235
product of, 253
of connected sum, 253
of Klein bottle, 253
of lens space, 286
of manifold, 253
of projective space, 235, 253
of torus, 270, 286
space, 234
universal, 261
transformation, 248
uniqueness, 260
universal, 261
crease, 5
CRING (category of commutative
rings), 171
crunch, big, 14
cube, 4
closed, 351
nested, 351
open, 29
cubical surface, 23
cup, coﬀee, 5
curvature, 7
curve, 2, 117
classiﬁcation, 118
plane, 2
space, 2
space-ﬁlling, 188
cusp, 11
cutting, 134
cycle
in a graph, 163
simplicial, 324
singular, 294
cyclic group, 356
homomorphism, 357
inﬁnite, 200
cyclic subgroup, 356, 357
cylinder, 3
mapping, 167
∂, see boundary
deck transformation, 248
deformation, 148
continuous, 4
retract, 161
strong, 161
retraction, 161

368
Index
and homotopy
equivalence, 166
strong, 161
degree of a map, 191, 320
homological, 320
homotopic, 320
degrees of freedom, 2
Dehn, Max, 137, 203
dense, 26
nowhere, 85
descending to the quotient, 56,
57
homomorphism, 356
diagonal, 62
diagram, commutative, 355
diameter, 76, 349
diﬀerence of sets, 339
dimension, 1
of a Euclidean simplicial
complex, 94
of a manifold, 33
of a simplex, 92
of a simplicial complex, 334
of an abstract simplex, 96
of an abstract simplicial
complex, 96
of an aﬃne subspace, 92
direct product, 353
direct sum, 177
disconnected, 65
discontinuous, properly, 268
discrete
group, 58
metric, 348
space, 19
closed sets, 25
subgroup, 270
topology, 19
disjoint sets, 339
disjoint union, 340, 345
topology, 37, 177
characteristic property, 62
disk
Euclidean, 31
hyperbolic, 271
distance function, 348
divisible group, 335
domain, 341
dot product, 347
doughnut surface, 3, 5, 45
homeomorphic to torus, 51,
80
dual
map, 173
space, 173
dynamical system, 13
ε (exponential quotient map),
61, 179, 235
edge
of a presentation, 131
of a simplex, 93
pairing transformation, 274
path, 101
connected, 101
periodic, 119
reduced, 101
point, 124
Einstein, Albert, 14
ﬁeld equations, 14
general relativity, 14
element of a set, 338
elementary particle, 14
elementary reduction, 195
elementary subdivision, 112
elementary transformation, 133
ellipsoid, 3
embedding, 40
empty set, 338
existence, 343
empty word, 194
equilibrium point, 14
equivalence
class, 52, 340
combinatorial, 112
homotopy, 161
is an equivalence relation,
161
of words, 195
relation, 52, 340

Index
369
generated by a relation,
340
topological, 4, 22
Euclidean
ball, 31
regular, 83
disk, 31
dot product, 347
geometry, 7
locally, 4, 30
metric, 348
neighborhood, 30
polyhedron, 94
simplex, 96
simplicial complex, 93
space, 2, 347
ambient, 17
is second countable, 33
zero-dimensional, 31, 347
topology, 19
triangle, 7
Euler characteristic, 113, 142,
328
and cohomology, 333
combinatorial invariance,
113, 142
of a graph, 230
of a topological space, 328
of compact surfaces, 143,
229
topological invariance, 229,
327
Euler’s formula, 112
even map, 253
even permutation, 353
evenly covered, 184, 234
exact functor, 335
exact homology sequence, 311
exact sequence, 296
long, 311
of chain complexes, 310
short, 296
existence
axiom, 343
of real numbers, 343
exponential
function, 20
quotient map, 61, 179, 235
Ext, see exterior
extension lemma, 331
extension of a map, 342
exterior, 25, 26
extreme value theorem, 73, 76,
352
face
boundary, 93
map, 293
of a presentation, 131
of a simplex, 93
of an abstract simplex, 96
point, 124
proper, 93
family, 338
fan transformation, 125
ﬁber, 53
action on, by fundamental
group, 245
ﬁeld, 330
characteristic zero, 330
ordered, 343
ﬁeld equations, Einstein, 14
ﬁgure eight space, 55, 160
ﬁnite
graph, 101
locally, 96
sequence, 345
set, 344
simplicial complex, 96
ﬁnitely presented, 202
ﬁrst category, 86
ﬁrst countable, 32
locally Euclidean spaces, 38
metric spaces, 38
ﬁrst isomorphism theorem, 356
ﬁve lemma, 313
ﬁxed point theorem, Brouwer,
192
folding, 134
forgetful functor, 172

370
Index
formal linear combination, 97
free
abelian group, 204
characteristic property,
204
uniqueness, 208
abelian subgroup, 205
group, 200
characteristic property,
200
uniqueness, 201
group action, 60
product, 195
characteristic property,
198
uniqueness, 199
vector space, 97
Freedman, Michael, 7
freedom, degrees of, 2
full subcategory, 171
function, 341
multiple-valued, 8
functor
cohomology, 330
contravariant, 172
covariant, 172
exact, 335
forgetful, 172
fundamental group, 172
homology, 296
fundamental group, 6, 152
action on ﬁber, 245
and homology, 305
and surface presentation,
217
change of base point, 154
functor, 172
homotopy invariance, 161
is a group, 154
of a graph, 215
of a manifold is countable,
189
of a polyhedron, 230
of a product, 189
of a surface, 220
abelianized, 228
of a topological group, 191
of a wedge of spaces, 213
of spheres, 188, 217
of the circle, 180
of the projective plane, 247
of the torus, 189
topological invariance, 159
fundamental theorem of algebra,
191
Gauss–Bonnet theorem, 8
general linear group, 10, 59, 60
complex, 10
general position, 92
general relativity, 14
generating circle, 45
generator
of a cyclic group, 356
of a group, 199
of a presentation, 201
genus, 144
geodesic
hyperbolic, 271
polygon, 273
regular, 274
geometric realization, 97, 99
functor, 172
of a polygonal presentation,
131
geometrization conjecture, 7
geometry
algebraic, 11
Euclidean, 7
plane, 7
Riemannian, 8
solid, 7
GL(n, R) (general linear group),
10, 59, 60
gluing lemma, 46
counterexample, 62
graph, 100
ﬁnite, 101
fundamental group, 215

Index
371
of a continuous function, 2,
43
is a manifold, 44
of a relation, 8
simple, 101
gravitation, 14
gravity, center of, 110
greatest lower bound, 343
GROUP (category of groups),
171
group, 352
abelian, 11, 203
action, 59, 266
continuous, 60
free, 60
proper, 266
quotient by, 61
transitive, 60
as a category, 173
automorphism, of covering,
248
complex general linear, 10
complex special linear, 11
covering, 248
direct product, 353
discrete, 58
divisible, 335
free, 200
free abelian, 204
fundamental, 6, 152
general linear, 10, 59, 60
homotopy, 169–170
injective, 335
Lie, 10
orthogonal, 11, 59, 60
permutation, 353
presentation, 201, 202
special linear, 11
special orthogonal, 11
special unitary, 11
symmetric, 353
theory, combinatorial, 203
topological, 58
quotient, 63
unitary, 11
groups, category of, 171
Hn (upper half space), 34
hairy ball theorem, 322
half space, upper, 34
ham sandwich theorem, 254
handedness, 106
handle, 9, 129
Hauptvermutung, 112
Hausdorﬀ
if diagonal is closed, 62
product space, 50
space, 31
subspace, 42
Heegaard, Poul, 137
Heine–Borel theorem, 351
hole, 5, 6, 147
holomorphic, 8
HomC(X, Y ) (set of morphisms),
170
Hom(X, Y ) (set of group
homomorphisms), 173,
329
homeomorphic, 4, 22
is an equivalence relation,
22
homeomorphism, 4, 22
local, 24
openness, 24
vs. closed map, 27
vs. open map, 27
homogeneity of norm, 89
homogeneous
space, 63
spacetime, 14
homological algebra, 297
homological degree, 320
homologous, 295
homology
and the fundamental group,
305
class, 295
functor, 296
groups
of a chain complex, 297

372
Index
simplicial, 324
singular, 295
homomorphism
induced by a chain map,
297
induced by a continuous
map, 296
homotopy invariance, 300
of a compact polyhedron,
334
of a contractible space, 303
of a disconnected space, 298
of a one-point space, 299
of a pseudomanifold, 334
of a simplex, 324
of a triangulable manifold,
334
of a wedge, 334
of spheres, 309
sequence, long exact, 311
simplicial, 324
vs. singular, 326
singular, 295
vs. simplicial, 326
topological invariance, 296
zero-dimensional, 298
homomorphism
covering, 258
is a covering map, 258
criterion, covering, 260
from a quotient group, 355
fundamental group, induced
by a continuous map,
159
homology
induced by a chain map,
297
induced by a continuous
map, 296
of cyclic group, 357
of group, 354
of topological groups, 270
homotopic, 148
degree, 320
maps and fundamental
group homomorphisms,
164
maps and homology
homomorphisms, 300
path, 151
relative to a subspace, 151
homotopy
category, 173
category, pointed, 173
chain, 303, 317
equivalence, 161
and deformation
retraction, 166
is an equivalence relation,
161
equivalent, 161
groups, 169–170
invariance
of path product, 152
of singular homology, 300
of the fundamental group,
161
is an equivalence relation,
148
lifting property, 238
of the circle, 181
of maps, 148
path, 151
and composition, 158
is an equivalence relation,
151
preserved by composition,
149
relative, 151
straight-line, 150
theory, 170
type, 161
hull, convex, 92
Hurewicz
homomorphism, 308
theorem, 308
Hurewicz, Witold, 308
hyperbolic
disk, 271

Index
373
geodesic, 271
metric, 271
triangle inequality, 289
neighborhood, regular, 278
hyperplane, aﬃne, 92
i (imaginary unit), 344
I (unit interval), 54
ιS (inclusion map), 342
	
α Xα (intersection), 345
ideal point, 12
identiﬁcation space, 52
identity
in a category, 171
in a group, 352
uniqueness, 353
map, 342
continuity, 21
path class, 153
Im f (image of f), 354
image
inverse, 342
is a subgroup, 354
of a function, 342
of a homomorphism, 354
of a normal subgroup, 356
set, 342
imaginary unit, 344
inclusion map, 342
continuity, 41
increasing function, 345
independent, linearly, 204
index
of a subgroup, 354
of a vector ﬁeld, 192
index set, 345
indexed collection, 345
intersection, 345
union, 345
induced
homomorphism of
fundamental groups,
159
by homotopic maps, 164
homomorphism, in
homology, 296, 297
morphism, 172
orientation, 107
subgroup, 239
inﬁmum, 343
inﬁnite
cyclic group, 200, 356
dimensional simplicial
complex, 96
product, 49
set, 344
initial point of a path, 150
initial vertex, 131
injection
in a category, 175
into direct sum, 177
into disjoint union, 345
into free group, 200
into free product, 197
injective, 342
group, 335
injectivity theorem, 239
inside out sphere, 5
Int, see interior
integers, 344
modulo n, 356
interior, 25, 26
of a manifold with
boundary, 34, 38
of a simplex, 93
intermediate value theorem, 65,
68
intersection
of an indexed collection, 345
of closed sets
in a metric space, 349
in a topological space, 24
of open sets
in a metric space, 349
in a topological space, 18
of sets, 339
intertwined edge pairs, 140
interval, 344
is connected, 68

374
Index
unit, 54
invariance of dimension, 318, 319
invariant
combinatorial, 113, 142
topological, 6
inverse
image, 342
in a group, 352
uniqueness, 353
left, 343
map, 342
of a path class, 153
right, 343, 346
isolated singular point, 192
isometry, 8
isomorphic coverings, 258
isomorphism
in a category, 171
of coverings, 258
of groups, 354
problem, 203
simplicial, 96
theorem, covering, 260
theorem, ﬁrst, 356
isotropic spacetime, 14
k-skeleton, see skeleton
Ker, see kernel
kernel, 354
is a subgroup, 354
is normal, 355
Klein bottle, 126
covering, 253
presentation, 133
largest element, 341
latitude, 3
laws of motion, Newton’s, 12
least upper bound, 343
Lebesgue number, 76
lemma, 76
left
action, 59
coset, 354
coset space, 61
inverse, 343
translation, 59, 63
length, 7, 347
lens space, 269
coverings of, 286
Lie group, 10
abelian, 11
lift, 179, 180, 237
lifting criterion, 240
lifting problem, 239
lifting property
homotopy, 238
of the circle, 181
path, 238
of the circle, 181
unique, 237
of the circle, 181
limit of a sequence
in a discrete space, 20
in a Hausdorﬀspace, 32
in a metric space, 349
in a topological space, 20
in a trivial space, 20
limit point, 26, 348
and closed sets, 26
compact, 76
vs. compact, 77, 78
vs. sequentially compact,
77, 78
line
long, 88
real, 2
segment, 347
with two origins, 62
linear combination, 204
formal, 97
linear ordering, 341
linear transformation, 20
linearly independent, 204
local criterion for continuity, 21
local ﬁniteness, see locally ﬁnite
local homeomorphism, 24
openness, 24
local section, 184, 236
of a covering map, 236

Index
375
locally
compact, 81
Hausdorﬀspace, 81, 82,
89
connected, 72
Euclidean, 4, 30
implies ﬁrst countable, 38
ﬁnite, 93, 96
path connected, 72
simply connected, 262
logarithmic function, 20
long exact homology sequence,
311
long line, 88
longitude, 3
loop, 151
based at a point, 151
constant, 151
Lorentz metric, 14
lower bound, 341
main theorem
on compactness, 73
on connectedness, 67
manifold, 1, 4, 33
boundary, 35
classiﬁcation, 6
complex, 33
countable fundamental
group, 189
homology of, 334
is locally compact
Hausdorﬀ, 83
is locally path connected, 72
product of, 51
Riemannian, 8
smooth, 33
topological, 33
with boundary, 34, 334
2-dimensional, 191
zero-dimensional, 37
map, 341
mapping, 341
mapping cylinder, 167
Markov, A. A., 7
mathematical object, 338
maximal, 341
tree, 214
Mayer–Vietoris
sequence
cohomology, 335
simplicial, 325
singular, 309
theorem
cohomology, 335
simplicial, 325
singular, 292, 309
mechanics, classical, 12
member of a set, 338
membership, 338
mesh, 317
metric, 348
discrete, 348
Euclidean, 348
hyperbolic, 271
Lorentz, 14
space, 348
ﬁrst countable, 38
Hausdorﬀ, 31
second countable, 38
subspace of, 40
topology, 19
minimal, 341
M¨obius
band, 105, 176
group, 272
transformation, 272
modulo n, 356
Moise, Edwin, 105
monodromy theorem, 239
morphism, 170
induced, 172
motion, Newton’s laws of, 12
multiple-valued function, 8
multiplication
group, 352
of cosets, 355
of path classes, 153
of paths, 152
of words, 194

376
Index
N (set of natural numbers), 344
n-dimensional
manifold, 33
topological manifold, 33
n-holed torus, 129
universal covering, 275
n-manifold, 33
n-sphere, 44
singular homology, 309
n-torus, 51
as a coset space of Rn, 61
fundamental group, 189
n-tuple, ordered, 345
naive set theory, 337
natural numbers, 344
natural orientation, 106
naturality of connecting
homomorphisms, 312
nearness, 18
neighborhood, 18
basis, 32
countable, 32
nested, 77
Euclidean, 30
regular hyperbolic, 278
nested
cubes, 351
neighborhood basis, 77
sets, 76
Newton’s laws of motion, 12
nondegenerate base point, 212
nonorientable surface, 144
covering of, 253
norm, 89, 347
normal closure, 201
normal covering, 245
normal subgroup, 354
image, 356
north pole, 3, 45
nowhere dense, 85
nth homotopy group, 170
nth power map, 191, 235
null homotopic, 151
O(n) (orthogonal group), 11, 59,
60
object
in a category, 170
mathematical, 338
odd map, 253
odd permutation, 353
one-point compactiﬁcation, 89
one-point space, singular
homology, 299
one-point union, 55
one-to-one
correspondence, 342
function, 342
onto, 342
open
ball, 348
is an open set, 349
cover, 32, 73
in a metric space, 350
of a subset, 73
cube, 29
map, 24
product of, 62
vs. homeomorphism, 27
set
as a topological space, 19
criterion for continuity,
350
in a metric space, 348
in a topological space, 18
intersection, in a metric
space, 349
intersection, in a
topological space, 18
is a manifold, 34
is Hausdorﬀ, 31
is second countable, 33
union, in a metric space,
349
union, in a topological
space, 18
simplex, 93
star, 114
orbit, 60, 245

Index
377
criterion, 249
space, 61, 266
by free proper group
action, 268
order of a group, 353
order topology, 37
ordered
ﬁeld, 343
n-tuple, 345
pair, 340
set
partially, 341
totally, 37, 341
well, 88, 341
ordering
linear, 341
partial, 341
simple, 341
total, 341
orientability is combinatorially
invariant, 115
orientable
pseudomanifold, 334
simplicial complex, 107
surface, 144, 229
orientation
induced, 107
natural, 106
of a simplex, 105
of a simplicial complex, 107
oriented presentation, 144
oriented simplex, 106
origins, line with two, 62
orthogonal group, 11, 59, 60
special, 11
π1(X) (fundamental group), 155
π1(X, q) (fundamental group),
152
P2 (projective plane), 119
Pn (real projective space), 55
P(S) (power set), 339
pair, ordered, 340
pancakes, 234
parabola, 2
paraboloid, 3
parameters, 1
partial ordering, 341
partially ordered set, 341
particle, elementary, 14
partition, 52, 340
passing to the quotient, 56, 57
homomorphism, 356
pasting, 134
path, 69, 150
class, 151
class identity, 153
class inverse, 153
class multiplication, 153
associativity, 153
class product, 153
associativity, 153
component, 72
connected, 69
locally, 72
connectivity relation, 71
homotopic, 151
homotopy, 151
and composition, 158
is an equivalence relation,
151
lifting property, 238
of the circle, 181
multiplication, 152
grouping, 154
homotopy invariance, 152
product, 152
grouping, 154
homotopy invariance, 152
reverse, 153
periodic edge path, 119
periodic trajectory, 14
permutation, 342
even, 353
group, 353
odd, 353
plane, 3
curve, 2
geometry, 7
projective, 119

378
Index
Poincar´e
conjecture, 6
homomorphism, 305
Poincar´e, Henri, 4, 6
point, 18
at inﬁnity, ideal, 12
pointed
homotopy category, 173
topological category, 171
topological space, 171
polar coordinates, 3
pole
north, 3, 45
south, 45
polygon
geodesic, 273
regular geodesic, 274
polygonal presentation, 130
geometric realization, 131
topologically equivalent, 133
polygonal region, 123
polyhedron, 100
Euclidean, 94
fundamental group, 230
homology, 334
is Hausdorﬀ, 114
is locally path connected,
114
polynomial, 20
position, general, 92
positivity
of metric, 348
of norm, 89
power map, 191, 235
power set, 339
axiom, 339
partial ordering, 341
precompact, 82
presentation
and Seifert–Van Kampen
theorem, 211
of a group, 201, 202
polygonal, 130
geometric realization, 131
topologically equivalent,
133
standard, 133, 137
surface, 132
and fundamental group,
217
classiﬁcation, 137
product
Cartesian, 340, 346
ﬁnite, 346
inﬁnite, 346
direct, 353
dot, 347
free, 195
in a category, 174
uniqueness, 174
map, 50
of closed maps, 62
of compact spaces, 74
of covering maps, 253
of locally compact
Hausdorﬀspaces, 83
of manifolds, 51
of open maps, 62
of path classes, 153
of paths, 152
of quotient maps, 86
of topological groups, 59
of words, 194
open sets, 48
space, 48
connectedness, 67
fundamental group, 189
Hausdorﬀ, 50
second countable, 50
topology, 48
associativity, 50
basis, 48, 50
characteristic property, 49
inﬁnite, 49, 177
on Rn, 48
uniqueness, 49
projection
from a Cartesian product,
346

Index
379
from a product space, 50
is a quotient map, 62
in a category, 174
onto a quotient group, 355
onto a quotient space, 52
stereographic, 45, 187
and one-point
compactiﬁcation, 89
projective
plane, 119
covering, 253
Euler characteristic, 143
fundamental group, 220,
247
presentation, 133
quotient of disk, 122
quotient of sphere, 121
quotient of square, 122
space
as orbit space, 61
complex, 12, 62
covering, 253
homology, 334
is a manifold, 62
real, 55
transformation, 12
proper
face, 93
group action, 266
on locally compact
Hausdorﬀspace, 267
quotient, 268
local homeomorphism, 253
map, 84
is closed, 84
subset, 338
properly discontinuous group
action, 268
property, topological, 4
pseudomanifold, 334
Q (set of rational numbers), 344
quantum ﬁeld theory, 14
quotient
by free proper group action,
268
by group action, 61
descending to, 56, 57
group, 355
map, 52
characterization, 57
composition, 53
exponential, 61, 235
restriction, 53
of a compact space, 74
of a manifold, 269
of a topological group, 63
passing to, 56, 57
second countable, 54
space, 52
connectedness, 67
uniqueness, 57
topology, 52
characteristic property, 56
R (set of real numbers), 343
Rn (n-dimensional Euclidean
space), 347
R⟨S⟩(free vector space), 97
Rad´o, Tibor, 104
range, 341, 342
rank
of a ﬁnitely generated
abelian group, 206
of a free abelian group, 205
rational function, 20
rational numbers, 344
real line, 2
real numbers, 343
uniqueness, 343
real projective space, 55
is a manifold, 62
real vector spaces, category of,
171
realization, geometric, 97, 99
of a polygonal presentation,
131
reduced edge path, 101
reduced word, 195

380
Index
reduction algorithm, 196
reduction, elementary, 195
reﬂecting, 134
reﬂection map, 321
reﬂexive, 340
region, polygonal, 123
regular
Euclidean ball, 83
geodesic polygon, 274
hyperbolic neighborhood,
278
point, of vector ﬁeld, 192
relabeling, 133
relation, 340
equivalence, 52, 340
generated by a relation,
340
of a presentation, 202
relative homotopy, 151
relative topology, 40
relatively compact, 82
relativity, general, 14
relator, 201
reparametrization, 151
restriction, 342
continuity of, 21, 41
of quotient map, 53
retract, 160, 176
deformation, 161
strong deformation, 161
retraction, 160
deformation, 161
strong deformation, 161
reverse path, 153
revolution, surface of, 45
Riemann surface, 9
Riemannian geometry, 8
Riemannian manifold, 8
right
action, 59
of fundamental group, 245
coset, 354
inverse, 343, 346
translation, 59
right-handed, 107
rigid body, 13
RING (category of rings), 171
rings
category of, 171
commutative, category of,
171
rotating, 134
Russell’s paradox, 338, 339
Russell, Bertrand, 338
Sn (unit n-sphere), 44
sandwich
ham, 254
tofu, 254
saturated, 52
scheme, vertex, 96
Sch¨onﬂies theorem, 104
second category, 86
second countable, 32
metric space, 38
product space, 50
quotient, 54
subspace, 42
section, 184
local, 184, 236
of a covering map, 236
segment, line, 347
Seifert–Van Kampen theorem,
211
and presentations, 211
proof, 221
special cases, 212, 217
semilocally simply connected,
265
separation of a space, 65
sequence, 345
convergent
in a metric space, 349
in a topological space, 20
ﬁnite, 345
limit
in a discrete space, 20
in a metric space, 349
in a topological space, 20
in a trivial space, 20

Index
381
sequentially compact, 77
vs. compact, 78
vs. limit point compact, 77,
78
SET (category of sets), 171
set, 338
diﬀerence, 339
membership, 338
of all sets, 339
theory, naive, 337
sets, category of, 171
sgn, 353
sheet, 9, 237
short exact sequence, 296
shrinking lemma, 82
side
of a geodesic, 274
of a simplex, 108
SIMP (category of simplicial
complexes), 171
simple graph, 101
simple ordering, 341
simplex, 92
abstract, 96
aﬃne singular, 293
Euclidean, 96
open, 93
oriented, 106
singular, 292
standard, 292
simplices, see simplex
simplicial
boundary, 324
boundary operator, 323
chain, 323
complex
abstract, 96
dimension, 334
Euclidean, 93
fundamental group, 230
complexes, category of, 171
cycle, 324
homology groups, 324
of a simplex, 324
vs. singular, 326
isomorphism, 96
map, 93, 95
between abstract
complexes, 96
Mayer–Vietoris sequence,
325
simply connected, 156
covering, 261
locally, 262
semilocally, 265
sine curve, topologist’s, 69, 72,
88
singleton, 339
singular
boundary, 293, 294
boundary operator, 293
chain, 293
chain group, 293
cochain, 329
cohomology group, 329
cycle, 294
homology groups, 295
homotopy invariance, 300
of a contractible space,
303
of a disconnected space,
298
of a one-point space, 299
of spheres, 309
vs. simplicial, 326
zero-dimensional, 298
map, 292
Mayer–Vietoris theorem,
292
point, 12
isolated, 192
of vector ﬁeld, 192
simplex, 292
aﬃne, 293
subdivision operator, 316
size, not a topological property,
22
skeleton
of a Euclidean simplicial
complex, 95

382
Index
of an abstract simplicial
complex, 96
SL(n, C) (complex special linear
group), 11
SL(n, R) (special linear group),
11
Smale, Stephen, 5, 7
small chain, 315
smallest element, 341
smooth dynamical system, 13
smooth manifold, 33
SO(n) (special orthogonal
group), 11
solid geometry, 7
south pole, 45
space, 18
curve, 2
discrete, 19
Euclidean, 347
Hausdorﬀ, 31
identiﬁcation, 52
metric, 348
product, 48
quotient, 52
topological, 18
variable, 152
space-ﬁlling curve, 188
spacetime, 14
homogeneous and isotropic,
14
special linear group, 11
special loop, 190
special orthogonal group, 11
special unitary group, 11
speciﬁcation axiom, 338
sphere, 3, 44
Euler characteristic, 143
fundamental group, 188
is simply connected, 217
not a retract of the ball, 334
presentation, 133
quotient of disk, 120
quotient of square, 120
singular homology, 309
turning inside out, 5
unit, 23, 44
in R3, 3
with n handles, 129
square root, complex, 8
stable trajectory, 14
stack of pancakes, 234
standard
basis for Zn, 204
presentation, 133, 137
simplex, 292
star, open, 114
star-shaped, 162
Steinitz, Ernst, 112
stereographic projection, 45, 62,
187
and one-point
compactiﬁcation, 89
straight-line homotopy, 150
strictly increasing, 345
string, 15
theory, 14
strong deformation retract, 161
strong deformation retraction,
161
structure theorem, covering
group, 250
SU(n) (special unitary group),
11
subbasis, 36
subcategory, 171
full, 171
subcomplex
of a Euclidean simplicial
complex, 95
of an abstract simplicial
complex, 96
subcover, 32, 73, 350
countable, 32
subdividing, 133
subdivision, 109
barycentric, 110, 315
elementary, 112
operator, singular, 316
subgraph, 101
subgroup, 353

Index
383
normal, 354
of a cyclic group, 357
of a free abelian group, 205
of a topological group, 59,
61, 63
subsequence, 345
subset, 338
of a countable set, 344
proper, 338
subspace, 39, 40
aﬃne, 92
closed sets, 41
Hausdorﬀ, 42
of a metric space, 40
of a subspace, 41
second countable, 42
topology, 40
basis for, 42
characteristic property, 41
uniqueness, 47
sum
connected, 126
is a manifold, 126
with sphere, 129
direct, 177
in a category, 175
uniqueness, 175
in the category of groups,
199
in the topological category,
177
supremum, 343
surface, 3, 117, 119
classiﬁcation, 6
fundamental group of, 220
abelianized, 228
nonorientable, 144
of genus n, 144
of revolution, 45
orientable, 144
presentation, 132
and fundamental group,
217
classiﬁcation, 137
Riemann, 9
universal covering of, 282
surjective, 342
symmetric, 340
group, 353
symmetry of a metric, 348
T2 (torus), 51
Tn (n-torus), 51
terminal point of a path, 150
terminal vertex, 131
tetrahedron, 92
theta space, 162
Thurston geometrization
conjecture, 7
Thurston, William, 7
Tietze, Heinrich, 112, 203
time variable, 152
tofu sandwich theorem, 254
TOP (topological category), 171
TOP∗(pointed topological
category), 171
topological
boundary, 35
category, 171
category, pointed, 171
embedding, 40
group, 58
discrete, 58
discrete subgroup of, 270
fundamental group of, 191
product of, 59
quotient of, 63
subgroup of, 59, 63
universal covering space
of, 290
invariance
of Euler characteristic,
327
of homology groups, 296
of the fundamental group,
159
invariant, 6
manifold, 33
property, 4, 22
space, 18

384
Index
topologically equivalent, 4, 22
presentations, 133
topologist’s sine curve, 69, 72, 88
topology, 4, 18
algebraic, 6
discrete, 19
disjoint union, 37
Euclidean, 19
generated by a basis, 27
generated by a subbasis, 36
metric, 19
product, 48
quotient, 52
relative, 40
subspace, 40
trivial, 19
torsion
element, 205
free, 205
subgroup, 205
torus, 3, 51
n-dimensional, 51
as a coset space of Rn, 61
as a quotient of the square,
55, 79
coverings of, 270, 286
Euler characteristic, 143
fundamental group, 189, 220
homeomorphic to doughnut
surface, 51, 80
n-holed, 129
presentation, 133
total ordering, 341
totally ordered set, 37, 341
trajectory
periodic, 14
stable, 14
transformation
elementary, 133
linear, 20
transitive, 340
group action, 60
transitivity of covering group,
249
translation
left, 59, 63
right, 59
transpose of linear map, 173
transposition, 353
tree, 163
contractible, 163
maximal, 214
triangle inequality, 89, 348
for hyperbolic metric, 289
triangle, Euclidean, 7
triangulable, 100
triangulation, 100
of 1-manifolds, 102
of 2-manifolds, 104
of 3-manifolds, 105
trigonometric function, 20
trivial group, 353
trivial topology, 19
turning the sphere inside out, 5
twisted edge pair, 139
two origins, line with, 62
Tychonoﬀ’s theorem, 75
type, homotopy, 161

α Xα (disjoint union), 345

α Xα (union), 345
U(n) (unitary group), 11
U-small chain, 315
uncountable set, 344
unfolding, 135
union
axiom, 339
connectedness of, 67
countable, 344
disjoint, 340, 345
topology, 37
of an indexed collection, 345
of closed sets
in a metric space, 349
in a topological space, 24
of open sets
in a metric space, 349
in a topological space, 18
of sets, 339
unique lifting property, 237

Index
385
of the circle, 181
uniqueness
of abelianization, 231
of covering spaces, 260
of free abelian group, 208
of free group, 201
of free product, 199
of product topology, 49
of quotient spaces, 57
of subspace topology, 47
unit
ball in Rn, 22
circle, 45
interval, 54
sphere, 23, 44
unitary group, 11
special, 11
universal coeﬃcient theorem, 330
universal covering, 261
of n-holed torus, 275
of a topological group, 290
of compact surfaces, 282
space, 261
existence, 262
universal mapping properties,
174
upper bound, 341
upper half space, 34
variety, algebraic, 12
VECTC (category of complex
vector spaces), 171
VECTR (category of real vector
spaces), 171
vector ﬁeld, 192, 322
index, 192
vector space, 347
free, 97
vector spaces
complex, category of, 171
real, category of, 171
vertex
initial, 131
map, 95, 96
of a presentation, 131
of a simplex, 92
of an abstract simplicial
complex, 96
point, 124
scheme, 96
terminal, 131
vertices, see vertex
volume, 7, 254
wedge of spaces, 55
fundamental group, 212, 213
singular homology, 334
well-ordered, 88, 341
well-ordering theorem, 88, 346
winding number, 179, 182
word, 130, 194
empty, 194
problem, 203
reduced, 195
world sheet, 15
Z (set of integers), 344
Z/⟨n⟩(integers modulo n), 356
Z⟨S⟩(free abelian group), 204
zero-dimensional
Euclidean space, 31, 347
homology, 298
manifold, 37
zigzag lemma, 310
Zorn’s lemma, 347


