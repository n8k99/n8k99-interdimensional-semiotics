# Preface
This book is an introduction to manifolds at the beginning graduate level.
It contains the essential topological ideas that are needed for the further
study of manifolds, particularly in the context of differential geometry,
algebraic topology, and related fields. Its guiding philosophy is to develop
these ideas rigorously but economically, with minimal prerequisites and
plenty of geometric intuition. Here at the University of Washington, for
example, this text is used for the first third of a year-long course on the
geometry and topology of manifolds; the remaining two-thirds focuses on
smooth manifolds.
Therearemanysuperbtextsongeneralandalgebraictopologyavailable.
Why add another one to the catalog? The answer lies in my particular
visionofgraduateeducation—itismy(admittedlybiased)beliefthatevery
serious student of mathematics needs to know manifolds intimately, in the
samewaythatmoststudentscometoknowtheintegers,therealnumbers,
Euclidean spaces, groups, rings, and fields. Manifolds play a role in nearly
every major branch of mathematics (as I illustrate in Chapter 1), and
specialists in many fields find themselves using concepts and terminology
fromtopologyandmanifoldtheoryonadailybasis.Manifoldsarethuspart
of the basic vocabulary of mathematics, and need to be part of the basic
graduate education. The first steps must be topological, and are embodied
in this book; in most cases, they should be complemented by material on
smooth manifolds, vector fields, differential forms, and the like. (After all,
few of the really interesting applications of manifold theory are possible
without using tools from calculus.)
Of course, it is not realistic to expect all graduate students to take full-
yearcoursesingeneraltopology,algebraictopology,anddifferentialgeome-
try.Thus,althoughthisbooktouchesonagenerousportionofthematerial
that is typically included in much longer courses, the coverage is selective
and relatively concise, so that most of the book can be covered in a single
quarter or semester, leaving time in a year-long course for further study in
whatever direction best suits the instructor and the students. At U.W. we
follow it with a two-quarter sequence on smooth manifold theory; but it
could equally well lead into a full-blown course on algebraic topology.
It is easy to describe what this book is not. It is not a course on general
topology—manyofthetopicsthatarestandardinsuchacourseareignored
here, such as metrization theorems; infinite products and the Tychonoff
theorem; countability and separation axioms and the relationships among
them (other than second countability and the Hausdorff axiom, which are
part of the definition of manifolds); and function spaces. Nor is it a course
in algebraic topology—although I treat the fundamental group in detail,
thereisbarelyamentionofthehigherhomotopygroups,andthetreatment
of homology theory is extremely brief, meant mainly to give the flavor of
the theory and to lay some groundwork for the later introduction of de
Rhamcohomology.Itiscertainlynotacomprehensivecourseontopological
manifolds, which would have to include such topics as PL structures and
maps,transversality,intersectiontheory,cobordism,bundles,characteristic
classes,andlow-dimensionalgeometrictopology.Finally,itisnotintended
as a reference book, because few of the results are presented in their most
general or most complete form.
Perhaps the best way to summarize what this book is would be to say
that it represents, to a good approximation, my conception of the ideal
amount of topological knowledge that should be possessed by beginning
graduate students who are planning to go on to study smooth manifolds
and differential geometry. Experienced mathematicians will probably ob-
servethatmychoicesofmaterialandapproachhavebeeninfluencedbythe
factthatIamadifferentialgeometerandanalystbytrainingandpredilec-
tion, not a topologist. Thus I give special emphasis to topics that will be
of importance later in the study of smooth manifolds, such as group ac-
tions, orientations, and degree theory. (A few topological ideas that are
important for manifold theory, such as paracompactness and embedding
theorems, are omitted because they are better treated in the context of
smooth manifolds.) But despite my prejudices, I have tried to make the
book useful as a precursor to algebraic topology courses as well, and it
could easily serve as a prerequisite to a more extensive course in homology
and homotopy theory.
Prerequisites. The prerequisite for studying this book is, briefly stated,
a solid undergraduate degree in mathematics; but this probably deserves
some elaboration. Traditionally, “algebraic topology” has been seen as a
separate subject from “general topology,” and most courses in the former
begin with the assumption that the students have already completed a
course in the latter. However, the sad fact is that for a variety of reasons,
many undergraduate mathematics majors in the U.S. never take a course
in general topology. For that reason I have written this book without as-
sumingthatthereaderhashadanyexposuretotopologicalspaces.Onthe
otherhand,Idoassumeseveralessentialprerequisitesbeyondcalculusand
linearalgebra:basiclogicandsettheorysuchaswhatonewouldencounter
in any rigorous undergraduate analysis or algebra course; real analysis at
the level of Rudin’s Principles of Mathematical Analysis [Rud76], includ-
ing, in particular, a thorough understanding of metric spaces and their
continuous functions and compact subsets; and group theory at the level
of Hungerford’s Abstract Algebra: An Introduction [Hun90] or Herstein’s
Topics in Algebra [Her75]. Because it is vitally important that the reader
be comfortable with this prerequisite material, I have collected in the Ap-
pendix a summary of the main points that are used throughout the book,
togetherwitharepresentativecollectionofexercises.Theseexercises,which
should be relatively straightforward for anyone who has had the prerequi-
site courses, can be used by the student to refresh his or her knowledge, or
can be assigned by the instructor at the beginning of the course to make
sure that everyone starts with the same background.
Organization. The book is divided into thirteen chapters, which can be
grouped into an introduction and five major substantive sections.
The introduction (Chapter 1) is meant to whet the student’s appetite
and create a “big picture” into which the many details can later fit.
Thefirstmajorsection,Chapters2through4,isabriefandhighlyselec-
tive introduction to the ideas of general topology: topological spaces; their
subspaces, products, and quotients; and connectedness and compactness.
Of course, manifolds are the main examples and are emphasized through-
out. These chapters emphasize the ways in which topological spaces differ
from the more familiar Euclidean and metric spaces, and carefully develop
the machinery that will be needed later, such as quotient maps, local path
connectedness, and locally compact Hausdorff spaces.
The second major section, comprising Chapters 5 and 6, explores in de-
tailthemainexamplesthatmotivatetherestofthetheory:simplicialcom-
plexes, 1-manifolds, and 2-manifolds. Chapter 5 introduces simplicial com-
plexesintwoways—firstconcretely,aslocallyfinitecollectionsofsimplices
in Euclidean space that intersect nicely; and then abstractly, as collections
of finite vertex sets. Both approaches are useful: The concrete definition
helps students develop their geometric intuition, while the abstract point
of view emphasizes the fact that all statements about simplicial complexes
can be reduced to combinatorics. There are several reasons for introducing
simplicial complexes at this stage: They furnish a rich source of examples;
they give a very concrete way of thinking about orientations and the Euler
characteristic; they provide the concept of triangulability needed for the
classifications of 1-manifolds and 2-manifolds; and they set the stage for
the treatment of homology later. Chapter 6 begins by proving a classifica-
tion theorem for 1-manifolds using the triangulability theorem proved in
theprecedingchapter.Therestofthechapterisdevotedtoadetailedstudy
of 2-manifolds. After exploring the basic examples of surfaces—the sphere,
the torus, the projective plane, and their connected sums—I give a com-
plete proof of the classification theorem for compact surfaces, essentially
following the treatment in [Mas89].
The third major section, Chapters 7 through 10, is the core of the book.
Init,Igiveafairlycompleteandtraditionaltreatmentofthefundamental
group. Chapter 7 introduces the definitions and proves the topological and
homotopy invariance of the fundamental group. At the end of the chapter
I insert a brief introduction to category theory. Categories are not used in
a central way anywhere in the book, but it is natural to introduce them
after having proved the topological invariance of the fundamental group,
and it is useful for students to begin thinking in categorical terms early.
Chapter 8 gives a detailed proof that the fundamental group of the circle
is infinite cyclic. Because the techniques used here are the precursor and
motivation for the entire theory of covering spaces, I introduce some of
the terminology of the latter subject—evenly covered neighborhoods, local
sections, lifting—in the special case of the circle, and the proofs here form
a model for the proofs of more general theorems involving covering spaces
tocomeinalaterchapter.Chapter9isabriefdigressionintogrouptheory.
Although a basic acquaintance with group theory is an essential prerequi-
site, most undergraduate algebra courses do not treat free products, free
groups, presentations of groups, or free abelian groups, so I develop these
subjectsfromscratch.(Thematerialonfreeabeliangroupsisincludedpri-
marilyforuseinthetreatmentofhomologyinChapter13,butsomeofthe
results play a role also in classifying the coverings of the torus in Chapter
12.) The last chapter of this section gives the statement and proof of the
Seifert–VanKampentheorem,whichexpressesthefundamentalgroupofa
space in terms of the fundamental groups of its subsets, and describes sev-
eralapplicationsofthetheoremincludingcomputationofthefundamental
groups of graphs and of all the compact surfaces.
The fourth major section consists of two chapters on covering spaces.
Chapter11definescoveringspaces,givesafewexamples,anddevelopsthe
theory of the covering group. Much of the development goes rapidly here,
becauseitisparalleltowhatwasdoneearlierintheconcretecaseofthecir-
cle.TheostensiblegoalofChapter12istoprovetheclassificationtheorem
for coverings—that there is a one-to-one correspondence between isomor-
phism classes of coverings of X and conjugacy classes of subgroups of the
fundamentalgroupofX—butalongthewaytwootherideasaredeveloped
that are of central importance in their own right. The first is the notion of
theuniversalcoveringspace,togetherwithproofsthateverymanifoldhasa
universal covering and that the universal covering space covers every other
covering space. The second is the fact that the quotient of a manifold by
a free, proper action of a discrete group yields a manifold. These ideas are
appliedtoanumberofimportantexamples,includingclassifyingcoverings
of the torus and the lens spaces, and proving that surfaces of higher genus
are covered by the hyperbolic disk.
The fifth major section of the book consists of one chapter only, Chap-
ter 13, on homology theory. In order to cover some of the most important
applications of homology to manifolds in a reasonable time, I have chosen
a “low-tech” approach to the subject. I focus mainly on singular homology
because it is the most straightforward generalization of the fundamental
group. After defining the homology groups, I prove a few essential proper-
ties, including homotopy invariance and the Mayer–Vietoris theorem, with
a minimum of homological machinery. I could not resist including a (terri-
bly brief) introduction to simplicial homology, just because it immediately
yields the topological invariance of the Euler characteristic. The last sec-
tion of the chapter is a brief introduction to cohomology, mainly with field
coefficients, to serve as background for a treatment of de Rham theory in
a later course. In keeping with the overall philosophy of focusing only on
what is necessary for a basic understanding of manifolds, I do not even
mentionrelativehomology,homologywitharbitrarycoefficients,simplicial
approximation, or the axioms for a homology theory.
Althoughthisbookgrewoutofnotesdesignedforaone-quartergraduate
course, there is clearly too much material here to cover adequately in ten
weeks. It should be possible to cover all or most of it in a semester with
wellpreparedstudents.Thebookcouldevenbeusedforafull-yearcourse,
allowing the instructor to adopt a much more leisurely pace and to work
out some of the problems as examples in class.
Each instructor will have his or her own ideas about what to leave out
in order to fit the material into a short course. At the University of Wash-
ington, we typically do not cover the chapter on homology at all, and give
short shrift to some of the simplicial theory and some of the more involved
examples of covering maps. Others may wish to leave out some or all of
the material on covering spaces, or the classification of surfaces. With stu-
dents who have had a solid topology course, the first four chapters could
be skipped or assigned as outside reading.
Exercises and Problems. As is the case with any new mathematical mate-
rial, and perhaps even more than usual with material like this that is so
differentfromthemathematicsmoststudentshaveseenasundergraduates,
it is impossible to learn the subject without getting one’s hands dirty and
working out a large number of examples and problems. I have tried to give
thereaderampleopportunitytodosothroughoutthebook.Ineverychap-
ter, and especially in the early ones, there are “exercises” woven into the
text. Do not ignore them; without their solutions, the text is incomplete.
The reader should take each exercise as a signal to stop reading, pull out a
pencil and paper, and work out the answer before proceeding further. The
exercises are usually relatively easy, and typically involve proving minor
results or working out examples that are essential to the flow of the expo-
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
student a chance to grapple with more significant issues. The results of a
numberoftheproblemsareusedlaterinthetext.Therearemoreproblems
thanmoststudentscoulddoinaquarterorasemester,sotheinstructorwill
wanttodecidewhichonesaremostgermaneandassignthoseashomework.
Acknowledgments. ThoseofmycolleaguesattheUniversityofWashington
with whom I have discussed this material—Tom Duchamp, Judith Arms,
SteveMitchell,ScottOsborne,andEthanDevinatz—haveprovidedinvalu-
able help in sorting out what should go into this book and how it should
be presented. Each has had a strong influence on the way the book has
come out, for which I am deeply grateful. (On the other hand, it is likely
that none of them would wholeheartedly endorse all my choices regarding
which topics to treat and how to treat them, so they are not to be blamed
foranyawkwardnessesthatremain.)IwouldliketothankEthanDevinatz
in particular for having had the courage to use the book as a course text
whenitwasstillinaninchoatestate,andforhavingthegraceandpatience
to wait while I prepared chapters at the last minute for his course.
ThanksareduealsotoMarySheetz,whodidanexcellentjobproducing
some of the illustrations under the pressures of time and a finicky author.
My debt to the authors of several other textbooks will be obvious to
anyone who knows those books: William Massey’s Algebraic Topology:
An Introduction [Mas89], Allan Sieradski’s An Introduction to Topology
and Homotopy [Sie92], Glen Bredon’s Topology and Geometry, and James
Munkres’s Topology: A First Course [Mun75] and Elements of Algebraic
Topology [Mun84] are foremost among them.
Finally, I would like to thank my wife, Pm, for her forbearance and
unflagging support while I was spending far too much time with this book
and far too little with the family; without her help I unquestionably could
not have done it.
John M. Lee Seattle
