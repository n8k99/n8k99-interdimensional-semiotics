---
title: "Introduction_to_Topological_Manifolds"
type: "[[Concept]]"
domain: "[[The Commons]]"
Lifestage: "🌱 Seed"
---

To Pm,
sine qua non

---

![[Preface]]
---

Contents
[[Preface]] 
1 Introduction 1
What Are Manifolds? … … … … … … … … 1
Why Study Manifolds? … … … … … … … … 4
2 Topological Spaces 17
Topologies … … … … … … … … … … . 17
Bases … … … … … … … … … … … 27
Manifolds … … … … … … … … … … . 30
Problems … … … … … … … … … … . 36
3 New Spaces from Old 39
Subspaces … … … … … … … … … … . 39
Product Spaces … … … … … … … … … . 48
Quotient Spaces … … … … … … … … … 52
Group Actions … … … … … … … … … . 58
Problems … … … … … … … … … … . 62
4 Connectedness and Compactness 65
Connectedness … … … … … … … … … . 65
Compactness … … … … … … … … … . . 73
Locally Compact Hausdorff Spaces … … … … … . . 81
Problems … … … … … … … … … … . 88

---

xvi Contents
5 Simplicial Complexes 91
Euclidean Simplicial Complexes … … … … … … . 92
Abstract Simplicial Complexes … … … … … … . 96
Triangulation Theorems … … … … … … … . . 102
Orientations … … … … … … … … … … 105
Combinatorial Invariants… … … … … … … . . 109
Problems … … … … … … … … … … . 114
6 Curves and Surfaces 117
Classification of Curves … … … … … … … . . 118
Surfaces … … … … … … … … … … . . 119
Connected Sums … … … … … … … … … 126
Polygonal Presentations of Surfaces… … … … … . . 129
Classification of Surface Presentations … … … … … 137
Combinatorial Invariants… … … … … … … . . 142
Problems … … … … … … … … … … . 146
7 Homotopy and the Fundamental Group 147
Homotopy … … … … … … … … … … . 148
The Fundamental Group … … … … … … … . . 150
Homomorphisms Induced by Continuous Maps … … … . 158
Homotopy Equivalence … … … … … … … … 161
Higher Homotopy Groups … … … … … … … . 169
Categories and Functors … … … … … … … . . 170
Problems … … … … … … … … … … . 176
8 Circles and Spheres 179
The Fundamental Group of the Circle … … … … … 180
Proofs of the Lifting Lemmas … … … … … … . . 183
Fundamental Groups of Spheres… … … … … … . 187
Fundamental Groups of Product Spaces … … … … . . 188
Fundamental Groups of Manifolds … … … … … . . 189
Problems … … … … … … … … … … . 191
9 Some Group Theory 193
Free Products … … … … … … … … … . . 193
Free Groups … … … … … … … … … … 199
Presentations of Groups … … … … … … … . . 201
Free Abelian Groups … … … … … … … … . 203
Problems … … … … … … … … … … . 208
10 The Seifert–Van Kampen Theorem 209
Statement of the Theorem … … … … … … … . 210
Applications… … … … … … … … … … 212
Proof of the Theorem … … … … … … … … 221

---

Contents xvii
Distinguishing Manifolds … … … … … … … . . 227
Problems … … … … … … … … … … . 230
11 Covering Spaces 233
Definitions and Basic Properties … … … … … … 234
Covering Maps and the Fundamental Group … … … … 239
The Covering Group … … … … … … … … . 247
Problems … … … … … … … … … … . 253
12 Classification of Coverings 257
Covering Homomorphisms … … … … … … … . 258
The Universal Covering Space … … … … … … . . 261
Proper Group Actions … … … … … … … … 266
The Classification Theorem … … … … … … … 283
Problems … … … … … … … … … … . 289
13 Homology 291
Singular Homology Groups … … … … … … … 292
Homotopy Invariance … … … … … … … … . 300
Homology and the Fundamental Group … … … … . . 304
The Mayer–Vietoris Theorem … … … … … … . . 308
Applications… … … … … … … … … … 318
The Homology of a Simplicial Complex … … … … . . 323
Cohomology … … … … … … … … … … 329
Problems … … … … … … … … … … . 334
Appendix: Review of Prerequisites 337
Set Theory … … … … … … … … … … 337
Metric Spaces … … … … … … … … … . . 347
Group Theory… … … … … … … … … . . 352
References 359
Index 362

---

# Chapter 1-Introduction
Ac ourse on manifolds differs from most other introductory graduate mathematics courses in that the subject matter is often completely unfamiliar. Most beginning graduate students have had undergraduate courses in algebra and analysis, so that graduate courses in those areas are continuations of subjects they have already begun to study. But it is possible to get through an entire undergraduate mathematics education, at least in the United States, without ever hearing the word “manifold.”
One reason for this anomaly is that even the definition of manifolds involves rather a large number of technical details—for example, in this book the formal definition will not come until the end of Chapter 2. Since it is disconcerting to embark on such an adventure without even knowing what it is about, we devote this introductory chapter to a nonrigorous definition of manifolds, an informal exploration of some examples, and a consideration of where and why they arise in various branches of mathematics.
## What Are Manifolds?
Let us begin by describing informally how one should think about manifolds. The underlying idea is that manifolds are like curves and surfaces, except, perhaps, that they might be of higher dimension. Every manifold has a dimension, which is, roughly speaking, the number of independent numbers (or “parameters”) needed to specify a point. The prototype of
# 2 1. Introduction
FIGURE 1.1. Plane curves. 
FIGURE 1.2. Space curve.
an n-dimensional manifold is n-dimensional Euclidean space Rn, in which each point is an n-tuple of real numbers. An n-dimensional manifold is an object modeled locally on Rn; this means that it takes exactly n numbers to specify a point, at least if we do not stray too far from a given starting point. A physicist would say that an n-dimensional manifold is an object with n “degrees of freedom.” 
Manifolds of dimension 1 are commonly called curves (although they need not be “curved” in the ordinary sense of the word). The simplest example is the real line; other examples are provided by familiar plane curves such as circles, parabolas, or the graph of any continuous function of the form $$y =f(x)$$ 
(Figure1.1). 
Still other familiar 1-dimensional manifolds are space curves, which are often described parametrically by equations such as $$ \begin{aligned} (x,y,z) &= (f(t),g(t),h(t)) \\[6pt] \text{for some continuous functions }f,g,h. \end{aligned} $$
(Figure 1.2).
In each of these examples, a point on the curve can be unambiguously specified by a single real number. For example, a point on the real line is a real number. We might specify a point on the circle by its angle, a point on a graph by its $x$ coordinate, and a point on a parametrized curve by
its parameter t. Note that although a parameter value determines a point, different parameter values may correspond to the same point, as in the case of angles on the circle. But in every case, as long as we stay close to some initial point, there is a one-to-one correspondence between nearby real numbers and nearby points on the curve.

FIGURE 1.3. Doughnut surface.
Manifolds of dimension 2 are surfaces. The two most common examples are planes and spheres. (When mathematicians speak of a sphere, we invariably mean a spherical surface, which is 2-dimensional, not a solid ball, which is 3-dimensional.) Other familiar surfaces include cylinders, ellipsoids, paraboloids, and the doughnut-shaped surface in R3 obtained by revolving a circle around the z-axis (Figure 1.3). (This doughnut-shaped surface is often called a torus, but we will reserve that name for a slightly different but closely related object, to be introduced in the next chapter.) In these cases two coordinates are needed to determine a point. For example, on the plane we typically use Cartesian or polarcoordinates; on the sphere we might use latitude and longitude; while on the doughnut surface we might use two angles. As in the 1-dimensional case, the correspondence between points and pairs of numbers is in general only local.
The only higher-dimensional manifold that we can visualize is Euclidean 3-space. But it is not hard to construct subsets of higher-dimensional Euclidean spaces that might reasonably be called manifolds. First, any open subset of Rn is an n-manifold for obvious reasons. More interesting examples are obtained by using one or more equations to “cut out” lower-dimensional subsets. For example, the set of points $(x1,x2,x3,x4)$ in R4 satisfying the equation
$$(x1)2+(x2)2+(x3)2+(x4)2 =1$$ (1.1)
is called the (unit) 3-sphere. It is a 3-dimensional manifold because in a neighborhood of any given point it takes exactly three coordinates to specify a nearby point: Starting at, say, the “north pole” $$(0,0,0,1)$$, we can solve equation (1.1) for $x4$, and then each nearby point is uniquely determined by choosing appropriate (small) $(x1,x2,x3)$ coordinates and setting$x4 =(1−(x1)2−(x2)2−(x3)2)1/2$. Near other points, we may need to solve for different variables; but in each case three coordinates suffice. 

---

4 1. Introduction
The key feature of these examples is that an n-dimensional manifold
“looks like” Rn locally. To make sense of the intuitive notion of “looks
like,” we will say that two subsets of Euclidean spaces U ⊂ Rk, V ⊂ Rn
are topologically equivalent or homeomorphic (Greek for “same form”) if
there exists a one-to-one correspondence ϕ: U →V such that both ϕ and
its inverse are continuous maps. (Such a correspondence is called a home-
omorphism.) A subset M of some Euclidean space Rk is locally Euclidean
of dimension n if every point of M has a neighborhood in M that is topo-
logically equivalent to a ball in Rn.
Nowwecangiveapreliminarydefinitionofmanifolds.Ann-dimensional
manifold(n-manifoldforshort)isasubsetofsomeEuclideanspaceRk that
is locally Euclidean of dimension n. Later, after we have developed more
machinery,wewillgiveaconsiderablymoregeneraldefinition;butthisone
will get us started.
Why Study Manifolds?
What follows is an incomplete survey of some of the fields of mathematics
in which manifolds play an important role.
Topology
Roughlyspeaking,topologyisthebranchofmathematicsthatisconcerned
with properties of sets that are unchanged by “continuous deformations.”
More accurately, a topological property is one that is preserved by home-
omorphisms.
ThesubjectinitsmodernformwasinventedacenturyagobytheFrench
mathematician Henri Poincar´e, as an outgrowth of his attempts to classify
geometric objects that appear in analysis. In a seminal 1895 paper titled
Analysis Situs (theoldnamefortopology,Latinfor“analysisofposition”)
andaseriesofcompanionpapersin1899–1905,Poincar´elaidoutthemain
problems of topology and introduced an astonishing array of new ideas for
solvingthem.Asyoureadthisbook,youwillseethathisnameiswrittenall
overthesubject.Intheinterveningcentury,topologyhastakenontherole
of providing the foundations for just about every branch of mathematics
that has any use for a concept of “space.” (An excellent historical account
of the first six decades of the subject can be found in [Die89].)
Hereisasimplebuttellingexampleofthekindofproblemthattopology
wasinventedtosolve.Considertwosurfacesinspace:asphereandacube.
Itshouldnotbehardtoconvinceyourselfthatthecubecanbecontinuously
deformed into the sphere without tearing or collapsing it. It is not much
harder to come up with an explicit formula for a homeomorphism between
them (we will do so in Chapter 2). Similarly, with a little more work, you

---

Why Study Manifolds? 5
FIGURE 1.4. Deforming a doughnut into a coffee cup.
shouldbeabletoseehowadoughnutsurfacecanbecontinuouslydeformed
into the surface of a one-handled coffee cup, by stretching out one-half of
the doughnut to become the cup, and shrinking the other half to become
the handle (Figure 1.4). Once you decide on an explicit set of equations to
define a “coffee-cup surface” in R3, you could in principle come up with a
setofformulastodescribeahomeomorphismbetweenitandthedoughnut
surface. On the other hand, a little reflection will probably convince you
that there is no homeomorphism from the sphere to the doughnut surface:
Any such map would have to tear open a “hole” in the sphere, and thus
could not be continuous.
Itisusuallyrelativelystraightforward(thoughnotalwayseasy!)toprove
that two manifolds are topologically equivalent once you have convinced
yourself intuitively that they are: Just write down an explicit homeomor-
phism between them. What is much harder is to prove that two manifolds
are not homeomorphic—even when it seems “obvious” that they are not
as in the case of the sphere and the doughnut—because you would need to
show that no one, no matter how clever, could find such a map.
History abounds with examples of operations that mathematicians long
believedtobeimpossible,onlytobeprovedwrong.Hereisanexamplefrom
topology.Imagineasphericalsurfacecoloredwhiteontheoutsideandgray
ontheinside,andimaginethatitcanmovefreelyinspace,includingpassing
freely through itself. Under these conditions you could turn the sphere
insideoutbycontinuouslydeformingit,sothatthegraysideendsupfacing
out, but it seems obvious that in so doing you would have to introduce a
creasesomewhere.(Thereareprecisemathematicaldefinitionsoftheterms
“continuouslydeforming”and“creases,”butyoudonotneedtoknowthem
to get the general idea.) The simplest way to proceed would be to push
the northern hemisphere down and the southern hemisphere up, allowing
them to pass through each other, until the two hemispheres had switched
places (Figure 1.5); but this would introduce a crease along the equator.
The topologist Stephen Smale stunned the mathematical community in
1958 [Sma58] when he proved it was possible to turn the sphere inside out
without introducing any creases. Several ways to do this are beautifully
illustrated in video recordings [Max77, LMM94, SFL98].

---

6 1. Introduction
FIGURE 1.5. Turning a sphere inside out (with a crease).
The usual way to prove that two manifolds are not topologically equiv-
alent is by finding topological invariants: properties (which could be num-
bers or other mathematical objects such as groups, matrices, polynomials,
or vector spaces) that are preserved by homeomorphisms. If two manifolds
have different invariants, they cannot be homeomorphic.
It is evident from the examples above that geometric properties such as
circumferenceandareaarenottopologicalinvariants,becausetheyarenot
generallypreservedbyhomeomorphisms.Intuitively,thepropertythatdis-
tinguishes the sphere from the doughnut surface is the fact that the latter
has a “hole,” while the former does not. But it turns out that giving a
precise definition of what is meant by a hole takes rather a lot of work.
One invariant that is commonly used to count holes in a manifold is called
the fundamental group of the manifold, which is a group (in the algebraic
sense) attached to each manifold in such a way that homeomorphic man-
ifolds have isomorphic groups. Then the “size” of the fundamental group
is a measure of the number of holes possessed by the manifold. The study
of the fundamental group will occupy a major portion of this book. It is
the starting point for algebraic topology, which is the subject that studies
topological properties of manifolds (or other geometric objects) by attach-
ingalgebraicstructuressuchasgroupsandringstotheminatopologically
invariant way.
One of the most important problems of topology is the problem of clas-
sifyingmanifolds.Ideally,onewouldliketoproducealistofn-dimensional
manifolds, and a theorem that says every n-dimensional manifold is home-
omorphic to exactly one on the list, together with a list of computable
topological invariants that could be used to decide where on the list any
given manifold belongs. Precisely such a theorem is known for surfaces:
It says that every compact surface is homeomorphic to a sphere, or to a
doughnut surface with a finite number of holes, or to a connected sum of
projective planes. (We will define these terms and prove the theorem in
Chapter 6.)
For higher-dimensional manifolds, the situation is much more compli-
cated.Forexample,Poincar´econjecturedaround1900thatanycompact3-

---

Why Study Manifolds? 7
manifoldwhosefundamentalgroupisthetrivial(one-element)groupmust
be homeomorphic to the 3-sphere. For a long time, topologists thought of
this as the simplest first step in a potential classification of 3-manifolds.
Butalthoughanalogousconjectureshavebeenmadeforhigher-dimensional
manifolds and were proved in the intervening years (for 5-manifolds and
higher by Stephen Smale in 1961 [Sma61], and for 4-manifolds by Michael
Freedman in 1982 [Fre82]), the original Poincar´e conjecture remains as of
this writing a preeminent unsolved problem in topology. The best hope for
a classification of 3-manifolds is the geometrization conjecture made in the
1970s by William Thurston (see [Sco83, Thu97] for an explanation), which
says, roughly, that every compact 3-manifold can be cut into finitely many
pieces each of which admits one of eight (mostly non-Euclidean) geometric
structures. Since the manifolds with geometric structures are much better
understood, a proof of this conjecture would go a long way toward provid-
ing a complete classification of 3-manifolds; in particular, it would imply
that the Poincar´e conjecture is true.
Indimensions4andhigher,ontheotherhand,thereisnohopeforacom-
pleteclassification:Itwasprovedin1958byA.A.Markovthatthereisno
algorithmforclassifyingmanifoldsofdimensiongreaterthan3(see[Sti93]).
Nonetheless, there is much that can be said using sophisticated combina-
tions of techniques from algebraic topology, differential geometry, partial
differentialequations,andalgebraicgeometry,andspectacularprogresswas
made in the last half of the twentieth century in understanding the vari-
ety of manifolds that exist. The topology of 4-manifolds, in particular, is
currently a highly active field of research.
Geometry
TheprincipalobjectsofstudyinEuclideanplanegeometry,asyouencoun-
tered it in secondary school, are figures constructed from portions of lines,
circles, and other curves—in other words, 1-manifolds. Similarly, solid ge-
ometry is concerned with figures made from portions of planes, spheres,
and other 2-manifolds. The properties that are of interest are those that
are invariant under rigid motions. These include simple properties such as
lengths,angles,areas,andvolumes,aswellasmoresophisticatedproperties
derivedfromthemsuchascurvature.Thecurvatureofacurveorsurfaceis
aquantitativemeasureofhowitbendsandinwhatdirections;forexample,
apositivelycurvedsurfaceis“bowl-shaped,”whileanegativelycurvedone
is “saddle-shaped.”
Geometric theorems involving curves and surfaces range from the trivial
totheverydeep.Atypicaltheoremyouhaveundoubtedlyseenbeforeisthe
angle-sumtheorem:ThesumoftheinterioranglesofanyEuclideantriangle
is π radians. This seemingly trivial result has profound generalizations to
thestudyofcurvedsurfaces,whereanglesmayadduptomoreorlessthan
π depending on the curvature of the surface. The high point of surface

---

8 1. Introduction
theory is the Gauss–Bonnet theorem: For a closed, bounded surface in R3,
thistheoremexpressestherelationshipbetweenthetotalcurvature(i.e.,the
integral of curvature with respect to area) and the number of holes it has.
If the surface is topologically equivalent to an n-holed doughnut surface,
the theorem says that the total curvature is exactly equal to 4π −4πn.
In the case n = 1 this implies that no matter how a one-holed doughnut
surface is bent or stretched, the regions of positive and negative curvature
will always precisely cancel each other out so that the total curvature is
zero.
The introduction of manifolds has allowed the study of geometry to be
carried into higher dimensions. The appropriate setting for studying geo-
metricpropertiesinarbitrarydimensionsisthatofRiemannian manifolds,
which are manifolds on which there is a rule for measuring distances and
angles,subjecttocertainnaturalrestrictionstoensurethatthesequantities
behave analogously to their Euclidean counterparts. The properties of in-
terest are those that are invariant under isometries, or distance-preserving
transformations. For example, one can study the relationship between the
curvatureofann-dimensionalRiemannianmanifold(alocalproperty)and
its global topological type. A typical theorem is that a complete Riemann-
ian n-manifold whose curvature is everywhere larger than some fixed posi-
tivenumbermustbecompactandhaveafinitefundamentalgroup(nottoo
many holes). The search for such relationships is one of the principal ac-
tivitiesinRiemanniangeometry,athrivingfieldofcontemporaryresearch.
See Chapter 1 of [Lee97] for an informal introduction to the subject.
Complex Analysis
Complexanalysisisthestudyofholomorphic(i.e.,complexanalytic)func-
tions. Some such functions are naturally “multiple-valued.” A typical ex-
ample is the complex square root. Except for zero, every complex number
hastwodistinctsquareroots.Butunlikethecaseofpositiverealnumbers,
where we can always √unambiguously choose the positive square root to
denote by the symbol x, it is not possible to define a global continuous
square root function on the complex plane. To see why, write z in polar
c√oordinates a√s z = reiθ. Then the two square roots of z can be written
reiθ/2 and rei(θ/2+π).Asθ increasesfrom0to2π,thefirstsquareroot
goes from the positive real axis through the upper half-plane to the neg-
ative real axis, while the second goes from the negative real axis through
the lower half-plane to the positive real axis. Thus whichever continuous
square root function we start with on the positive real axis, we are forced
to choose the other after having made one circuit around the origin.
Eventhougha“two-valuedfunction”isproperlyconsideredasarelation
and not really a function at all, we can define the graph of such a relation
in an unambiguous way. To warm up with a simpler example, consider the
two-valued square root “function” on the nonnegative real axis. Its graph

---

Why Study Manifolds? 9
u
u2 =x
x
FIGURE 1.6. Graph of the two branches of the real square root.
√
is defined to be the set of pairs (x,u) ∈ R×R such that u = ± x, or
equivalently u2 =x. This is a parabola opening in the positive x direction
(Figure 1.6), which we can think of as the two “branches” of the square
root.
Similarly, the graph of the two-valued complex square root “function”
is the set of pairs (z,w) ∈ C×C such that w2 = z. Over each small disk
U ⊂ C that does not contain 0, this graph has two branches or “sheets,”
correspondingtothetwopossiblecontinuouschoicesofsquarerootfunction
on U (Figure 1.7). If you start on one sheet above the positive real axis
andpassoncearoundtheorigininthecounterclockwisedirection,youend
upontheothersheet.Goingaroundoncemorebringsyoubacktothefirst
sheet.
ItturnsoutthatthisgraphinC2isa2-dimensionalmanifold,ofaspecial
type called a Riemann surface—this is essentially a 2-manifold on which
there is some way to define holomorphic functions. Riemann surfaces are
of great importance in complex analysis, since any holomorphic function
gives rise to a Riemann surface by a procedure analogous to the one we
sketched above. The surface we constructed turns out to be topologically
equivalent to a plane, but more complicated functions can give rise to
m√orecomplicatedsurfaces.Forexample,thetwo-valued“function”f(z)=
± z3−z yields a Riemann surface that is homeomorphic to a plane with
one “handle” attached.
One of the fundamental tasks of complex analysis is to understand the
topological type (number of “holes” or “handles”) of the Riemann surface

---

10 1. Introduction
w
√
w = reiθ/2
y
U
√
w = rei(θ/2+π)
x
FIGURE 1.7. Two branches of the complex square root.
of a given function, and how it relates to the analytic properties of the
function.
Algebra
Oneofthemostimportantobjectsstudiedinabstractalgebraisthegeneral
linear group GL(n,R), which is the group of n×n invertible real matrices.
As a set, it can be identified with a subset of n2-dimensional Euclidean
space, simply by stringing all the matrix entries out in a row. Since a
matrixisinvertibleifandonlyifitsdeterminantisnonzero,GL(n,R)isan
opensubsetofRn2 ,andisthereforeann2-dimensionalmanifold.Similarly,
the complex general linear group GL(n,C) is the group of n×n invertible
complex matrices; it is a 2n2-manifold, because we can identify Cn2 with
R2n2
.
A Lie group is a group (in the algebraic sense) that is also a manifold,
togetherwithsometechnicalconditionstoensurethatthegroupstructure
and the manifold structure are compatible with each other. They play a
central role in differential geometry, representation theory, and mathemat-
ical physics, among many other fields. The most important Lie groups are
subgroups of the real and complex general linear groups. Some commonly

---

Why Study Manifolds? 11
FIGURE 1.8. A plane curve with disconnected pieces.
encountered examples are the special linear group SL(n,R) ⊂ GL(n,R),
consisting of matrices with determinant 1; the orthogonal group O(n) ⊂
GL(n,R),consistingofmatriceswhosecolumnsareorthonormal;thespecial
orthogonal group SO(n) = O(n)∩SL(n,R); and their complex analogues,
the complex special linear group SL(n,C) ⊂ GL(n,C), the unitary group
U(n)⊂GL(n,C), and the special unitary group SU(n)=U(n)∩SL(n,C).
ItisimportanttounderstandthetopologicalstructureofaLiegroupand
howitstopologicalstructurerelatestoitsalgebraicstructure.Forexample,
it can be shown that SO(2) is topologically equivalent to a circle, SU(2)
is topologically equivalent to the 3-sphere, and any connected abelian Lie
groupistopologicallyequivalenttoaCartesianproductofcirclesandlines.
Liegroupsprovidearichsourceofexamplesofmanifoldsinalldimensions.
Algebraic Geometry
Algebraic geometers study the geometric properties of solution sets to sys-
tems of polynomial equations. Many of the basic questions of algebraic
geometry can be posed very naturally in the elementary context of plane
curves defined by polynomial equations. For example: How many intersec-
tion points can one expect between two plane curves defined by polyno-
mials of degrees k and l? (Not more than kl, but sometimes fewer.) How
many disconnected “pieces” does the solution set to a particular polyno-
mialequationhave(Figure1.8)?Doesaplanecurvehaveanyselfcrossings
(Figure 1.9) or “cusps” (points where the tangent vector does not vary
continuously—Figure 1.10)?
Buttherealpowerofalgebraicgeometrybecomesevidentonlywhenone
focusesonpolynomialswithcoefficientsinanalgebraically closedfield(one
in which every polynomial decomposes into a product of linear factors),
since polynomial equations always have the expected number of solutions
(counted with multiplicity) in that case. The most deeply studied case is
the complex field; in this context the solution set to a system of complex

---

12 1. Introduction
FIGURE 1.9. A self crossing. FIGURE 1.10. A cusp.
polynomials in n variables is a certain geometric object in Cn called an
algebraic variety, which (except for a small subset where there might be
self crossings, cusps, or more complicated kinds of behavior) is a manifold.
The subject becomes even more interesting if one enlarges Cn by adding
“ideal points at infinity” where parallel lines or asymptotic curves can be
thoughtofasmeeting;theresultingspaceiscalledcomplexprojectivespace,
and is an extremely important manifold in its own right.
The properties of interest are those that are invariant under projective
transformations (the natural changes of coordinates on projective space).
One can ask such questions as these: Is a given variety a manifold or does
it have singular points (points where it fails to be a manifold)? If it is
a manifold, what is its topological type? If it is not a manifold, what is
the geometric structure of its singular set, and how does that set change
whenonevariesthecoefficientsofthepolynomialsslightly?Iftwovarieties
are homeomorphic, are they equivalent under a projective transformation?
How many times and in what way do two or more varieties intersect?
Algebraic geometry has contributed a prodigious supply of examples of
manifolds. In particular, much of the recent progress in understanding 4-
dimensionalmanifoldshasbeendrivenbythewealthofexamplesthatarise
as algebraic varieties.
Classical Mechanics
Classical mechanics is the study of systems that obey Newton’s laws of
motion. The positions of all the objects in the system at any given time
can be described by a set of numbers, or coordinates; typically, these are
not independent of each other but instead must satisfy some relations.
The relations can usually be interpreted as defining a manifold in some
Euclidean space.

---

Why Study Manifolds? 13
Q
θ
R
P
d
PQ
FIGURE 1.11. A rigid body in space.
For example, consider a rigid body moving through space under the
influence of gravity. If we choose three noncollinear points P, Q, and R on
thebody(Figure1.11),thepositionofthebodyiscompletelyspecifiedonce
weknowthecoordinatesofthesethreepoints,whichcorrespondtoapoint
in R9. However, the positions of the three points cannot all be specified
arbitrarily: Because the body is rigid, they are subject to the constraint
that the distances between pairs of points are fixed. Thus, to determine
the position of the body, we can arbitrarily specify the coordinates of P
in space (three parameters), and then we can specify the position of Q
by giving, say, its latitude and longitude on the sphere of radius d , the
PQ
fixed distance between P and Q (two more parameters). Finally, having
determined the position of the two points P and Q, the only remaining
freedom is to rotate R around the line PQ; so we can specify the position
of R by giving the angle θ that the plane PQR makes with some reference
plane(onemoreparameter).Thusthesetofpossiblepositionsofthebody
is a certain 6-dimensional manifold M ⊂R9.
Newton’ssecondlawofmotionexpressestheaccelerationoftheobject—
that is, the second derivatives of the coordinates of P, Q, R—in terms of
the force of gravity, which is a certain function of the object’s position.
This can be interpreted as a system of second-order ordinary differential
equations for the position coordinates, whose solutions are all the possible
paths the rigid body can take on the manifold M.
The study of classical mechanics can thus be interpreted as the study of
ordinarydifferentialequationsonmanifolds,alsoknownassmooth dynam-
ical systems. A wealth of interesting questions arise in this subject: How

---

14 1. Introduction
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
called a Lorentz metric; and this metric satisfies a system of partial differ-
entialequationscalledtheEinsteinfieldequations.Gravitationaleffectsare
then interpreted as manifestations of the curvature of the Lorentz metric.
In order to describe the global structure of the universe, its history, and
its possible futures, it is important to understand first of all what kinds
of 4-manifolds exist and what kinds of Lorentz metrics they can carry.
There are especially interesting relationships between the local geometry
of spacetime (as reflected in the local distribution of matter and energy)
and the global topological structure of the universe; these relationships
are similar to those described above for Riemannian manifolds, but are
morecomplicatedbecauseoftheintroductionofforcesandmotionintothe
picture.Inparticular,ifweassumethatonacosmicscaletheuniverselooks
approximatelythesameatallpointsandinalldirections(suchaspacetime
issaidtobehomogeneousandisotropic),thenitturnsoutthereisacritical
value for the average density of matter and energy in the universe: Above
this density, the universe closes up on itself spatially and will collapse to a
point singularity in a finite time (the “big crunch”); below it, the universe
extendsinfinitelyfarinalldirectionsandwillexpandforever.Interestingly,
physicists’bestcurrentestimatesplacetheaveragedensityrathernearthe
critical value, and they have so far been unable to determine whether it
is above or below it, so they do not know whether the universe will go on
existing forever or not.
Quantum Field Theory
Thetheoryofelementaryparticleinteractions,calledquantumfieldtheory,
has become increasingly geometric in recent decades. In particular, the
latest attempts to unify quantum theory and gravitation have led to ever
moreinterestingandexoticgeometricstructures.Theapproachtoquantum
gravity that is currently considered most promising by many physicists is
string theory, in which manifolds appear in several different starring roles.
First, in order to obtain a consistent theory, it seems to be necessary to
assumethatspacetimehasmorethanfourdimensions.Weexperienceonly

---

Why Study Manifolds? 15
four of them directly, because the dimensions beyond four are so tightly
“curledup”thattheyarenotvisibleonamacroscopicscale,muchasalong
but microscopically narrow cylinder would appear to be one-dimensional
whenviewedfromfarenoughaway.Thetopologicalpropertiesoftheman-
ifold that appears as the “cross section” of the curled-up dimensions have
such a profound effect on the observable dynamics of the resulting quan-
tum field theory that it is possible to rule out most cross sections a priori.
It currently appears that a consistent theory can be constructed only if
the cross section is a certain kind of 6-dimensional manifold known as a
Calabi–Yau manifold. These developments in physics have stimulated pro-
found developments in the mathematical understanding of 6-manifolds in
general and Calabi-Yau manifolds in particular.
Anotherrolethatmanifoldsplayinstringtheoryisindescribingthehis-
tory of an elementary particle. One of the central tenets of string theory is
thatparticlesshouldberepresentednotaspoints,butastiny1-dimensional
objects(“strings”)movingthroughspacetime.Asaparticlemoves,ittraces
out a 2-dimensional manifold called its world sheet. Physical phenomena
arisefromtheinteractionsamongthesedifferenttopologicalandgeometric
structures: the world sheet, the Calabi-Yau cross section, and the macro-
scopic four-dimensional spacetime that we see.
Manifolds are used in many more areas of mathematics than the ones
listed here, but this brief survey should be enough to show you that mani-
folds have a rich assortment of applications. It is time to get to work.

---

2
Topological Spaces
In this chapter we begin our study in earnest. The first order of business
is to build up enough machinery to give a proper definition of manifolds.
The chief problem with the preliminary definition given in Chapter 1 is
that it depends on having an “ambient Euclidean space” in which our n-
manifold lives. This introduces a great deal of extraneous structure that is
irrelevant to our purposes. Instead, we would like to view a manifold as a
mathematical object in its own right, not as a subset of some larger space.
The key concept that makes this possible is that of a “topological space,”
which is the main topic of this chapter.
Webeginbydefiningtopologicalspaces,motivatedbytheopensetcrite-
rionforcontinuityinmetricspaces.Afterthedefinitionweintroducesome
oftheimportantelementarynotionsassociatedwithtopologicalspacessuch
as convergence, continuity, homeomorphisms, closures, interiors, and exte-
riors, and then explore how to construct topologies from bases. At the end
of the chapter we give the official definition of a manifold as a topological
space with special properties.
Topologies
One of the most useful tools in analysis is the concept of a metric space.
(See the Appendix for a brief review of metric space theory.) The most
important examples, of course, are (subsets of) Euclidean spaces with the

---

18 2. Topological Spaces
Euclideanmetric,butmanyothers,suchasfunctionspaces,arisefrequently
in analysis.
Our goal in this book is to study manifolds and those of their properties
that are preserved by homeomorphisms (continuous maps with continuous
inverses). To accomplish this, we could choose to view our manifolds as
metric spaces. However, a metric still contains extraneous information. It
isobviousthatahomeomorphismbetweenmetricspacesneednotpreserve
distances (just think of the obvious homeomorphism between two spheres
ofdifferentradii).Sowewillpushtheprocessofabstractionastepfurther,
andcomeupwithakindof“space”withoutdistancesinwhichcontinuous
functions still make sense.
The key motivation behind the definition of this new kind of space is
the open set criterion for continuity (Lemma A.5 in the Appendix), which
shows that continuous functions between metric spaces can be detected
knowing only the open sets. Motivated by this observation, we make the
followingdefinition.AtopologyonasetX isacollectionT ofsubsetsofX,
called open sets, satisfying the following properties:
(i) X and ∅ are elements of T.
(ii) T is closed under finite intersections: If U1,…,U
n
∈ T, then their
intersection U1 ∩···∩U
n
is in T.
(iii) T is closed under arbitrary unions: If {U α } α∈A is any(cid:2)(finite or in-
finite) collection of elements of T, then their union U is in
α∈A α
T.
A pair (X,T) consisting of a set X and a topology T on X is called a
topological space. The elements of a topological space are usually called
its points. Since we will rarely have occasion to discuss any other type
of space in this book, we will sometimes follow the common practice of
callingatopologicalspacesimplyaspace.Asiscommoninmathematicsin
discussingasetendowedwithaparticularkindofstructure,ifthetopology
is understood from the context, we will typically omit it from the notation
and simply say “X is a topological space” or “X is a space.”
Asidefromthesimplicityoftheopensetcriterionforcontinuity,theother
reason for choosing open sets as the primary objects in the definition of a
topologicalspaceisthattheygiveusaqualitativewaytodetect“nearness”
to a point without necessarily having a quantitative measure of nearness
as we would in a metric space. If X is a topological space and q ∈ X,
a neighborhood of q is just an open set containing q. More generally, a
neighborhood of a subset K ⊂ X is an open set containing K. (In some
books, the word neighborhood is used in the more general sense of a set
containing an open set containing q; but for us neighborhoods will always
be open.) We think of something being true “near q” if it is true in some
(or every, depending on the context) neighborhood of q.
The following exercises give some simple examples of topological spaces.

---

Topologies 19
{{1},{2,3},{1,2,3},∅} Discrete topology Trivial topology
FIGURE 2.1. Topologies on {1,2,3}.
Exercise 2.1. Showthateachofthefollowingisatopologicalspace.(See
Figure 2.1.)
(a) Let X denote the set {1,2,3}, and declare the open sets to be {1},
{2,3}, {1,2,3}, and the empty set.
(b) AnysetX whatsoever,withT={all subsets of X}.Thisiscalledthe
discrete topology on X, and (X,T) is called a discrete space.
(c) Any set X, with T={∅,X}. This is called the trivial topology on X.
(d) Any metric space (M,d), with T equal to the collection of all subsets
of M that are open in the metric space sense. This topology is called
the metric topology on M.
Metric spaces provide a rich source of examples of topological spaces. In
fact,alargepercentageofthetopologicalspaceswewillneedtoconsiderare
actually subsets of Euclidean spaces Rn, with the metric topology induced
by the Euclidean metric (which we call the Euclidean topology). Unless we
specify otherwise, subsets of Rn will always be considered as topological
spaces with this topology. Thus our intuition regarding topological spaces
will rely heavily on our understanding of subsets of Euclidean space.
Another important class of examples of topological spaces is obtained
by taking open subsets of other spaces. If X is a topological space, and
Y is any open subset of X, then we can define a topology on Y just by
declaring the open sets of Y to be those open sets of X that are contained
in Y. It is trivial to check that the three defining properties of a topology
are satisfied. (In the next chapter, we will show how to put a topology on
any subset of a topological space.)
Convergence and Continuity
Theprimaryreasontopologicalspaceswereinventedwasthattheyprovide
the most general setting for studying the notions of convergence and con-
tinuity. For this reason, it is appropriate to introduce these concepts next.
We begin with convergence.
The definition of convergence of a sequence of points in a metric space
(see the Appendix) is really just a fancy way of saying that as we go far

---

20 2. Topological Spaces
enoughoutinthesequence,thepointsofthesequencebecome“arbitrarily
close” to q.
Intopologicalspaces,weuseneighborhoodstoencodethenotionof“ar-
bitrarily close.” Thus, if X is a topological space and {q } is any sequence
i
of points in X, we say that the sequence converges to q ∈ X, and q is the
limit of the sequence, if for every neighborhood U of q there exists N such
that q ∈U for all i≥N. Symbolically, this is denoted by either q →q or
i i
lim i→∞q
i
=q.
Exercise 2.2. Show that in a metric space, this topological definition of
convergence is equivalent to the metric space definition.
Forthetypesoftopologicalspaceswewillbechieflyinterestedin(mostly
manifolds), convergent sequences behave very much the same way we are
used to from our experience with Euclidean space. Nevertheless, it is good
to be aware that for some of the stranger examples of topological spaces,
convergence can sometimes have an unintuitive meaning, as the following
exercises show.
Exercise 2.3.
(a) Let X be a discrete topological space. Show that the only convergent
sequences in X are the ones that are “eventually constant,” that is,
sequences {qi } such that qi =q for all i greater than some N.
(b) Let Y be a trivial topological space (that is, a set with the trivial
topology {∅,Y}). Show that every sequence in Y converges to every
point of Y.
Attheendofthischapterwewilldescribearestrictedclassoftopological
spaces(Hausdorffspaces)forwhichthepathologicalbehaviorof (b)cannot
occur.
Next we address the most important topological concept of all: continu-
ous maps. If X and Y are topological spaces, a map f: X → Y is said to
be continuous if for every open set U ⊂Y, f−1(U) is open in X.
The open set criterion (Lemma A.5) for continuity in metric spaces says
preciselythatamapbetweenmetricspacesiscontinuousinthissenseifand
only if it is continuous in the usual ε-δ sense. Therefore, all the maps that
youknowtobecontinuousfrommetricspacetheoryarealsocontinuousas
mapsoftopologicalspaces.ExamplesincludepolynomialfunctionsfromR
to R, linear transformations from Rn to Rk, and, more generally, any map
from a subset of Rn to Rk whose component functions are continuous in
the ordinary sense, such as polynomial, exponential, rational, logarithmic,
absolute value, and trigonometric functions (where they are defined), and
functions built up from these by composition.
Thenextlemmagivessomeelementarybutimportantpropertiesofcon-
tinuous maps. The ease with which properties like this can be proved is
one of the virtues of defining continuity in terms of open sets.

---

Topologies 21
Lemma 2.1. Let X, Y, and Z be topological spaces.
(a) Any constant map f: X →Y is continuous.
(b) The identity map Id: X →X is continuous.
(c) If f: X → Y is continuous, so is the restriction of f to any open
subset of X.
(d) If f: X → Y and g: Y → Z are continuous, so is their composition
g◦f: X →Z.
Proof. We will prove (d) and leave the other parts as exercises. We have
to show that if U is any open subset of Z, then (g◦f)−1(U) is an open
subset of X. By elementary set-theoretic considerations, (g ◦f)−1(U) =
f−1(g−1(U)). Applying the definition of continuity to g, g−1(U) is open;
and then doing the same for f shows that f−1(g−1(U)) is open.
Exercise 2.4. Prove parts (a)–(c) of Lemma 2.1.
Inmetricspacesitmakessensetotalkaboutamapbeing“continuousat
apoint”(f: M1 →M2 iscontinuousatx∈M1 ifforallε>0,thereexists
δ > 0 such that for each y ∈ M1, d1(y,x) < δ implies d2(f(y),f(x)) < ε),
and a map is continuous if and only if it is continuous at every point. In
topological spaces, continuity at a point is generally not a very useful con-
cept.However,itisanimportantfactthatcontinuityisa“local”property,
in the sense that a map is continuous if and only if it is continuous in a
neighborhoodofeverypoint.Theprecisestatementisgiveninthefollowing
important lemma.
Lemma 2.2 (Local Criterion for Continuity). Amapf: X →Y be-
tween topological spaces is continuous if and only if each point of X has a
neighborhood on which (the restriction of) f is continuous.
Proof. If f is continuous, we may simply take each neighborhood to be X
itself.Conversely,supposef iscontinuousinaneighborhoodofeachpoint,
andlet U ⊂Y beanyopenset;wehavetoshowthat f−1(U)isopen.Any
point x∈f−1(U) has a neighborhood V on which f is continuous (Figure
x
2.2). Continuity of f| implies, in particular, that (f| )−1(U) is open in
Vx Vx
V , and therefore also open in X. Unwinding the definitions, we see that
x
(f| )−1(U)={x∈V :f(x)∈U}=f−1(U)∩V ,
Vx x x
which contains x and is contained in f−1(U). Since f−1(U) is the union of
all such open sets as x ranges over f−1(U), it follows that f−1(U) is open,
as desired.

---

22 2. Topological Spaces
X
f
Y
V
x
U
f−1(U) x
FIGURE 2.2. Local criterion for continuity.
If X and Y are topological spaces, a homeomorphism from X to Y is
defined to be a continuous bijective map ϕ: X → Y with continuous in-
verse. If there exists a homeomorphism between X and Y, we say that
X and Y are homeomorphic or topologically equivalent. Sometimes this is
abbreviated X ≈Y.
Exercise 2.5. Show that “homeomorphic” is an equivalence relation.
The homeomorphism relation is the most fundamental relation in topol-
ogy. In fact, as we mentioned in Chapter 1, “topological properties” are
exactly those that are preserved by homeomorphisms.
Here are a few explicit examples of homeomorphisms that you should
keep in mind.
Example 2.3. Any open ball in Rn is homeomorphic to any other open
ball; the homeomorphism can easily be constructed as a composition of
translations x(cid:10)→x+x0 and dilations x(cid:10)→cx. Similarly, all spheres in Rn
are homeomorphic to each other. These examples illustrate that “size” is
not a topological property.
Example 2.4. Let Bn denote the open unit ball B1(0) ⊂ Rn, and define
a map F: Bn →Rn by
x
y =F(x)= .
1−|x|2
Note that |F(x)|=|x|/(1−|x|2)→∞ as |x|→1. It is straightforward to
check that the inverse of F is given by
2y
x=F−1(y)= (cid:3) .
1+ 1+4|y|2
Thus F is a homeomorphism, so Rn is homeomorphic to Bn. This shows
that “boundedness” is not a topological property.
Example 2.5. Another illustrative example is the homeomorphism be-
tween a cube and a sphere alluded to in Chapter 1. Let S2 = {x ∈

---

Topologies 23
FIGURE 2.3. Deforming a cube into a sphere.
R3 : |x| = 1} denote the unit sphere in R3, and set C = {(x,y,z) :
max(|x|,|y|,|z|) = 1}, which is the cubical surface of side 2 centered at
the origin. Let ϕ: C →S2 be the map that projects each point on C radi-
ally inward to the sphere (Figure 2.3). More precisely, given a pointq ∈C,
ϕ(q)istheunitvectorinthedirectionofq.Thusϕisgivenbytheformula
(x,y,z)
ϕ(x,y,z)= (cid:3) ,
x2+y2+z2
which is continuous by the usual arguments of elementary analysis. The
next exercise shows that ϕ is a homeomorphism. This example demon-
strates that “corners” are not topological properties.
Exercise 2.6. Show that the map ϕ: C → S2 is a homeomorphism by
showing that its inverse can be written
ϕ−1(x,y,z)= (x,y,z) .
max(|x|,|y|,|z|)
In the definition of a homeomorphism, it is important to note that al-
though the assumption that ϕ is bijective guarantees that the inverse map
ϕ−1 exists for set-theoretic reasons, continuity of ϕ−1 is not automatic.
Thenextexercisegivesanexampleofacontinuousbijectionwhoseinverse
is not continuous.
Exercise 2.7. Let X denote the half-open interval [0,1) ⊂ R, and let S1
denote the unit circle in R2 (both with the Euclidean metric topologies, of
course). Define a map a: X → S1 by a(t) = (cos2πt,sin2πt) (Figure 2.4).
Show that a is continuous and bijective but not a homeomorphism.

---

24 2. Topological Spaces
a
FIGURE 2.4. A map that is bijective but not a homeomorphism.
A map f: X → Y (continuous or not) is said to be an open map if for
any open set U ⊂X, the image set f(U) is open in Y. A map can be open
but not continuous, continuous but not open, both, or neither.
There is a generalization of homeomorphisms that is often useful. We
say that a continuous map f: X →Y between topological spaces is a local
homeomorphismifeverypointx∈X hasaneighborhoodU ⊂X suchthat
f(U) is an open subset of Y and f| : U →f(U) is a homeomorphism.
U
Exercise 2.8.
(a) Show that every local homeomorphism is an open map.
(b) Show that every homeomorphism is a local homeomorphism.
(c) Show that a bijective continuous open map is a homeomorphism.
(d) Show that a bijective local homeomorphism is a homeomorphism.
Closed Sets
Becauseoftheimportanceofneighborhoodsinunderstandingatopological
space and its continuous maps and convergent sequences, the definition of
a topological space takes open sets as the primary objects. There is also a
complementary notion that is nearly as important.
AsubsetF ofatopologicalspaceX issaidtobeclosedifitscomplement
X(cid:3)F isopen.Fromthedefinitionoftopologicalspaces,severalproperties
follow immediately:
(i) X and ∅ are closed.
(ii) Finite unions of closed sets are closed.
(iii) Arbitrary intersections of closed sets are closed.
AtopologyonasetX canbedefinedbydescribingthecollectionofclosed
sets, as long as they satisfy these three properties; the open sets are then
just those sets whose complements are closed.
Here are some examples of closed subsets of familiar topological spaces.

---

Topologies 25
Example 2.6 (Closed Sets).
(a) Any closed interval [a,b] ⊂ R is a closed set, as are the half-infinite
closed intervals [a,∞) and (−∞,b].
(b) Any closed ball in a metric space is a closed set (Exercise A.11(b) in
the Appendix).
(c) Every subset of a discrete space is closed.
It is important to be aware that just as in metric spaces, “closed” is not
thesameas“notopen”—setscanbebothopenandclosed,orneitheropen
nor closed. For example, in any topological space X, the sets X and ∅ are
both open and closed. On the other hand, the half-open interval [0,1) is
neither open nor closed in R.
Continuity can be detected by closed sets as well as open ones.
Lemma 2.7. A map between topological spaces is continuous if and only
if the inverse image of every closed set is closed.
Exercise 2.9. Prove Lemma 2.7.
Given any set A ⊂ X, we define several related sets as follows. The
closure of A in X, denoted by A, is the set
(cid:4)
A= {B ⊂X :B ⊃A and B is closed in X}.
The interior of A, written IntA, is
(cid:5)
IntA= {C ⊂X :C ⊂A and C is open in X}.
It is obvious from the properties of open and closed sets that A is closed
and IntA is open. In words, A is “the smallest closed set containing A,”
and IntA is “the largest open set contained in A.”
We also define the exterior of A, written ExtA, as
ExtA=X(cid:3)A,
and the boundary of A, written ∂A, as
∂A=X(cid:3)(IntA∪ExtA).
It follows immediately from the definitions that for any subset A ⊂ X,
the whole space X is equal to the disjoint union of IntA, ExtA, and ∂A.
The set A always contains all of its interior points and none of its exterior
points, and may contain all, some, or none of its boundary points.
For many purposes, it is useful to have alternative characterizations of
open and closed sets, and of the interior, exterior, closure, and boundary
of a given set. The following lemma gives such characterizations. Some of
theseareprobablyfamiliartoyoufromyourstudyofEuclideanandmetric
spaces. See Figure 2.5 for illustrations of some of these characterizations.

---

26 2. Topological Spaces
ExtA
IntA
A
∂A
FIGURE 2.5. Interior, exterior, and boundary points.
Lemma 2.8. Let X be a topological space and A⊂X any subset.
(a) A point q is in the interior of A if and only if q has a neighborhood
contained in A.
(b) A point q is in the exterior of A if and only if q has a neighborhood
contained in X(cid:3)A.
(c) A point q is in the boundary of A if and only if every neighborhood
of q contains both a point of A and a point of X(cid:3)A.
(d) IntA and ExtA are open in X, while ∂A is closed in X.
(e) A is open if and only if A=IntA.
(f) A is closed if and only if it contains all its boundary points, which is
true if and only if A=IntA∪∂A.
(g) A=A∪∂A=IntA∪∂A.
Exercise 2.10. Prove Lemma 2.8.
Given a topological space X and a set A ⊂ X, we say that a point
q ∈ X is a limit point of A if every neighborhood of q contains a point of
A other than q (which might or might not itself be in A). Limit points are
also sometimes called accumulation points or cluster points. For example,
if X =R and A=(0,1), then every point in [0,1] is a limit point of A. If
we let B ={1/n}∞ ⊂R, then 0 is the only limit point of B.
n=1
Exercise 2.11. Show that a set A in a topological space is closed if and
only if it contains all of its limit points.
A subset A of a topological space X is said to be dense in X if A=X.

---

Bases 27
Exercise 2.12. Show that a subset A ⊂ X is dense if and only if every
nonempty open set in X contains a point of A.
Exercise 2.13. Show that Rn has a countable dense subset.
Analogous to open maps are closed maps: A map f: X → Y is said to
be closed if it takes closed sets in X to closed sets in Y.
Exercise 2.14. Show that a bijective continuous map is a homeomor-
phism if and only if it is open if and only if it is closed.
Bases
To define a topology on a given set, it is often convenient to single out
some “special” open sets and use them to define the rest of the open sets.
Forexample,themetrictopologyisdefinedbyfirstdefiningballsandthen
declaring a set to be open if it contains a ball around each of its points.
This idea can be generalized easily to arbitrary topological spaces, as in
the next definition.
Suppose X is any set. A basis in X is a collection B of subsets of X
satisfying the following conditions:
(i) (cid:2)Every element of X is in some element of B; in other words, X =
B.
B∈B
(ii) If B1,B2 ∈B and x∈B1 ∩B2, there exists an element B3 ∈B such
that x∈B3 ⊂B1 ∩B2.
Proposition 2.9. Let B be a basis in a set X, and let T be the collection
of all unions of elements of B. Then T is a topology on X.
This topology T is called the topology generated by B. Before we prove
the proposition, it will be useful to have an alternative characterization of
T, analogous to the definition of open sets in a metric space in terms of
balls. Given X and a collection B of subsets of X, we say that a subset
U ⊂ X satisfies the basis criterion with respect to B if for every x ∈ U,
there exists B ∈B such that x∈B ⊂U.
Lemma 2.10. Suppose B is a basis in X. Then the collection T defined in
Proposition 2.9 is precisely the set of all subsets of X that satisfy the basis
criterion with respect to B.
Proof. Let U ⊂ X, and suppose first that U satisfies the basis criterion.
Let
(cid:5)
V = {B ∈B:B ⊂U}.

---

28 2. Topological Spaces
U2
B2
U1
B3
B1
x
FIGURE 2.6. Proof that U1 ∩U2 satisfies the basis criterion.
Obviously, V ∈T, since V is by definition a union of basis sets. Thus if we
can show that U = V, it will follow that U ∈ T. Clearly, V ⊂ U, because
V is a union of subsets of U. To show that U ⊂V, let x∈U be arbitrary;
sinceU satisfiesthebasiscriterion,theremustexistabasissetB ∈Bsuch
that x∈B ⊂U. It follows immediately that x∈V, so we are done.
Conversely,supposethatU ∈T.Thism(cid:2)eansthatU isaunionofelements
of B, i.e., for some subset A ⊂ B, U = B. In other words, x ∈ U if
B∈A
and only if x∈B for some B ∈A. In particular, x∈B ⊂U, so U satisfies
the basis criterion.
Proof of Proposition 2.9. We need to show that T satis(cid:2)fies the three defin-
ing conditions for a topology. First, the fact that X = B means that
B∈B
X ∈T.TheemptysetisalsoinT trivially.(Itisthe“unionofnoelements
of B”!) A union of elements of T is a union of unions of elements of B, and
thereforeisitselfaunionofelementsofB;thus T isclosedunderarbitrary
unions.
Finally, to show that T is closed under finite intersections, suppose first
that U1,U2 ∈ T. Then, for any x ∈ U1 ∩U2, the basis criterion says that
thereexistbasiselementsB1,B2 ∈Bsuchthatx∈B1 ⊂U1 andx∈B2 ⊂
U2 (Figure2.6).Butthenpart(ii)ofthedefinitionofbasisguaranteesthat
there exists B3 ∈B such that x∈B3 ⊂B1 ∩B2 ⊂U1 ∩U2. Thus U1 ∩U2
satisfies the basis criterion, so it is again in T. This shows that T is closed
under pairwise intersections, and closure under finite intersections follows
easily by induction.
It often happens that we are given a particular topological space X
together with a collection B of open subsets of X, and we would like to
know whether B forms a basis for the topology of X. On the face of it,
this would require showing first that B satisfies the two conditions in the

---

Bases 29
definition of a basis, and then that each open subset of X is a union of
elements of B (or alternatively satisfies the basis criterion). But as the
following lemma shows, once we know that the sets in B are open subsets
with respect to some topology, showing that they actually are a basis for
that topology is much easier.
Lemma 2.11. Suppose X is a topological space, and B is a collection of
open subsets of X. If every open subset of X satisfies the basis criterion
with respect to B, then B is a basis for the topology of X.
Proof. By Lemma 2.10, all we need to show is that B satisfies the two
defining conditions for a basis.
Forthefirstcondition,sinceX itselfisanopensubset,thebasiscriterion
tells us that any point x∈X is in some element B ∈B; thus the union of
all the elements of B is X.
For the second condition, suppose B1 and B2 are elements of B and
x∈B1 ∩B2.ThebasiscriterionappliedtoB1 ∩B2(whichistheintersection
of two open subsets of X and therefore open) guarantees the existence of
B3 ∈B such that x∈B3 ⊂B1 ∩B2.
The next exercise describes bases for the topologies of Exercise 2.1. The
precedinglemmamakesthejobofshowingthattheyareindeedbasesquite
straightforward.
Exercise 2.15. In each of the following cases, prove that the given set B
is a basis for the given topology.
(a) M is a metric space with the metric topology, and B is the collection
of all open balls in M.
(b) X is a set with the discrete topology, and B is the collection of all
one-point subsets of X.
(c) X is a set with the trivial topology, and B={X}.
Exercise 2.16. Show that each of the following collections B i is a basis
for the Euclidean topology on Rn.
(a) B 1 = {Cs(x) : x ∈ Rn and s > 0}, where Cs(x) is the open cube of
side s around x:
Cs(x)={y=(y1,…,yn):|xi −yi |<s/2, i=1,…,n}.
(b) B 2 ={Br(x): r is rational and x has rational coordinates}.
When we have a basis for a topology on Y, it is sufficient (and often
mucheasier)tocheckcontinuityofmapsintoY usingonlybasisopensets,
as the following lemma shows.

---

30 2. Topological Spaces
Lemma 2.12. Let X and Y be topological spaces and let B be a basis for
Y. A map f: X → Y is continuous if and only if for every basis open set
B ∈B, f−1(B) is open in X.
Proof. Clearly, if f is continuous, the inverse image of every basis open set
is open. Conversely, suppose f−1(B) is open for every B ∈ B. Let U ⊂ Y
be open, and let x∈f−1(U). By the basis criterion, there is a basis set B
such that f(x) ∈ B ⊂ U. This implies that x ∈ f−1(B) ⊂ f−1(U), which
means that x has a neighborhood contained in f−1(U). Since this is true
for every x∈U, U is the union of all these neighborhoods as x ranges over
points of U, and therefore is open.
Manifolds
We are almost ready to give the official definition of manifolds. We need
just a few more preliminary definitions. The first one is easy, and captures
very precisely the intuitive idea that a manifold should look “locally” like
Euclidean space. Let X be a topological space. A topological space M
is said to be locally Euclidean of dimension n if every point q ∈ M has
a neighborhood that is homeomorphic to an open subset of Rn. Such a
neighborhood is called a Euclidean neighborhood of q.
Forsomepurposes,itisusefultobemorespecificaboutthekindofopen
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
(Example2.4),properties(a)and(b)areequivalent,soweneedonlyprove
(a).
Given any point q ∈ M, let U be a neighborhood of q that admits a
homeomorphism ϕ: U → V, where V is an open subset of Rn. The fact
that V is open means that there is some open ball B around ϕ(q) that is
contained in V, and then ϕ−1(B) is a neighborhood of q homeomorphic to
an open ball.

---

Manifolds 31
IfM islocallyEuclideanofdimensionn,ahomeomorphismfromanopen
subset U ⊂M to an open subset of Rn is called a coordinate chart (or just
a chart) on U. We will call any open subset of M that is homeomorphic
to a ball in Rn a Euclidean ball in M. (When M has dimension 2, we will
sometimes use the term Euclidean disk.) The preceding lemma shows that
everypointinalocallyEuclideanspacehasaEuclideanballneighborhood.
The definition of locally Euclidean spaces makes sense even when n=0.
Since R0 is by convention a single point, Lemma 2.13(b) implies that a
space is locally Euclidean of dimension 0 if and only if each point has a
neighborhoodhomeomorphictoaone-pointspace,orinotherwordsifand
only if the space is discrete.
There are two other properties that we will include in the definition of
manifolds, to rule out “pathological” spaces that might otherwise pass as
manifolds.
Hausdorff Spaces
The first property we want to introduce ensures that there are “enough”
opensets,sothatneighborhoodsbehavemoreorlessthewayourintuition
derived from Euclidean and metric spaces leads us to expect. For example,
inametricspace,aone-pointset{q}isalwaysclosed,becausearoundevery
pointotherthanqthereisaballthatdoesnotincludeq.Moregenerally,any
two points in a metric space always have disjoint neighborhoods. However,
these properties do not always hold in topological spaces. Consider the set
{1,2,3} with the topology {∅,{1},{2,3},{1,2,3}} (Figure 2.1). In this
case 2 and 3 do not have disjoint neighborhoods, since every open set that
contains one also contains the other. Moreover, the set {2} is not closed,
because its complement is not open.
The problem with this example is that there are too few open sets, so
neighborhoodsdonothavethesameintuitivemeaningtheyhaveinmetric
spaces. In our study of manifolds, we will want to rule out such “patholog-
ical” spaces, so we make the following definition. A topological space X is
said to be a Hausdorff space if given any pair of distinct points q1,q2 ∈X,
there exist neighborhoods U1 of q1 and U2 of q2 with U1 ∩U2 = ∅. This
property is often summarized by saying “open sets separate points.”
Any metric space is Hausdorff. (If d(q1,q2) = r, then the open balls of
radius r/2 around q1 and q2 are disjoint by the triangle inequality.) More
generally, any open subset of a Hausdorff space is Hausdorff: If V ⊂ X is
open in the Hausdorff space X, and q1,q2 are distinct points in V, then in
X thereareopensetsU1,U2 separatingq1 andq2,andthesetsU1 ∩V and
U2 ∩V are open in V, disjoint, and contain q1 and q2, respectively.
Hausdorff spaces have many of the properties that we expect of metric
spaces, such as those expressed in the following lemma.
Lemma 2.14. Let X be a Hausdorff space.

---

32 2. Topological Spaces
(a) Every one-point set in X is closed.
(b) If a sequence {x } in X converges to a limit x ∈ X, the limit is
i
unique.
Proof. For part (a), choose any q0 ∈ X. Given p (cid:14)= q0, the Hausdorff
property says that there exist disjoint neighborhoods U
p
of q0 and V
p
of p.
This means that the complement of {q0 } is equal to the union of the open
sets V
p
as p ranges over X(cid:3){q0 }, which is open, so {q0 } is closed.
To prove that limits are unique, suppose that x and x(cid:5) are two distinct
limits of the sequence {x }. By the Hausdorff property, there exist disjoint
i
neighborhoodsU ofxandU(cid:5) ofx(cid:5).Bydefinitionofconvergence,thereexist
N,N(cid:5) suchthati≥N impliesx ∈U andi≥N(cid:5) impliesx ∈U(cid:5).Butsince
i i
U and U(cid:5) are disjoint, this is a contradiction when i≥max(N,N(cid:5)).
Exercise 2.17. Show that the only Hausdorff topology on a finite set is
the discrete topology.
The non-Hausdorff example above involving {1,2,3} is obviously con-
trived, and has little relevance to our study of manifolds. But in Problem
3-8 at the end of the next chapter you will see a space that would be a
manifold except for the fact that it fails to be Hausdorff.
Second Countability
Whereas the Hausdorff property ensures that there are enough open sets,
the next property we will introduce ensures that there are not too many.
Wesaythatatopologicalspaceissecond countableifitadmitsacountable
basis.
As the “second” in the name second countable suggests, there is also
another weaker notion of countability. It relies on the following definition:
If X is a space and q ∈X, a collection B of neighborhoods of q is called a
q
neighborhood basis at q if every neighborhood of q contains some B ∈ B .
q
X is said to be first countable if there exists a countable neighborhood
basis at each point. Second countability implies first countability: Given a
countablebasisforX,thecollectionofbasisopensetscontainingq iseasily
seen to be a countable neighborhood basis at q.
Oneofthewaysinwhichsecondcountabilityisoftenusedisinreducing
thenumberofopensetsoneneedsto“cover”aspace.IfX isanytopological
space, a collection U of subsets of X is said to cover X, or to be a cover of
X, if every point in X is in one of the sets of U. An open cover of X is a
collection of open sets that covers X. Given any cover U, a subcover of U
is a subset of U that is still a cover.
Lemma 2.15. If X is a second countable space, every open cover of X
has a countable subcover.

---

Manifolds 33
Proof. Let B be a countable basis for X, and let U be an arbitrary open
cover of X. Let B(cid:5) denote the subset of B consisting of those basis sets
that are entirely contained in some element of U. Because any subset of a
countable set is countable, B(cid:5) is a countable set.
Now, for each element B ∈ B(cid:5), choose an element U ∈ U such that
B
B ⊂ U (this is possible by the way we defined B(cid:5)). The collection U(cid:5) =
B
{U : B ∈ B(cid:5)} is a countable subset of U; the lemma will be proved if we
B
can show that it still covers X.
Ifx∈X isarbitrary,thenx∈U0 forsomeopensetU0 ∈U.Bythebasis
criterion for U0, there is some B ∈ B such that x ∈ B ⊂ U0. This means,
in particular, that B ∈ B(cid:5), and therefore there is a set U ∈ U(cid:5) such that
B
x∈B ⊂U . This shows that U(cid:5) is a cover and completes the proof.
B
Most “reasonable” spaces are second countable. For example, it follows
from Exercise 2.16(b) above that Rn is second countable. Moreover, any
opensubsetU ofasecondcountablespaceX issecondcountable:Starting
with a countable basis for X, just throw away all the elements of the basis
that do not lie in U; then it is easy to check that the remaining basis sets
form a countable basis for the topology of U.
In Problems 3-7 and 4-6 we will see examples of spaces that would be
manifolds except for the failure of second countability.
Definition of Manifolds
We come now to the culmination of this chapter: the official definition of
manifolds.
An n-dimensional topological manifold is a second countable Hausdorff
spacethatislocallyEuclideanofdimension n.Sincetheonlykindofman-
ifolds we will be considering in this book are topological manifolds, we
will usually simply call them n-dimensional manifolds, or n-manifolds, or
evenjustmanifoldsifthedimensionisunderstoodorirrelevant.(Theterm
“topological manifold” is usually used only to emphasize that the kind
of manifold under consideration is the kind we have defined here, which
is a topological space with special properties, rather than other kinds of
manifolds that can be defined, such as “smooth manifolds” or “complex
manifolds.” We will not treat any of these other kinds of manifolds in this
book.)
A shorthand notation that is in common use is to write “let Mn be a
manifold”tomean“letM beamanifoldofdimensionn.”Thesuperscriptn
isnotpartofthenameofthemanifold,andisusuallydroppedafterthefirst
time the manifold is introduced. One must be a bit careful to distinguish
this notation from the n-fold Cartesian product Mn = M ×···×M, but
it is usually clear from the context which is meant. We will not use this
shorthand in this book, but you should be aware of it because you will
encounter it in your reading.

---

34 2. Topological Spaces
FIGURE 2.7. A manifold with boundary.
The most obvious example of an n-manifold is Rn itself. More gener-
ally, any open subset of Rn—or in fact of any n-manifold—is again an
n-manifold, as the next lemma shows.
Lemma 2.16. Any open subset of an n-manifold is an n-manifold.
Proof. Let M be an n-manifold, and let V be an open subset of M. Any
q ∈V has a neighborhood (in M) that is homeomorphic to an open subset
ofRn;theintersectionofthatneighborhoodwithV isstillopen,stillhome-
omorphic to an open subset of Rn, and lies in V, so V is locally Euclidean.
We remarked above that any open subset of a Hausdorff space is Haus-
dorffandanyopensubsetofasecondcountablespaceissecondcountable.
Therefore V is an n-manifold.
In the next few chapters we will develop many more examples of mani-
folds.
Manifolds with Boundary
Forsomepurposesitisusefulalsotohavethefollowingmoregeneralnotion.
An n-dimensional manifold with boundary is a second countable Hausdorff
space in which every point has a neighborhood homeomorphic to an open
subset of the n-dimensional upper half space Hn = {(x1,…,x
n
) ∈ Rn :
x ≥0}. Just as in the case of manifolds, we will call any homeomorphism
n
from an open subset U of M to an open subset of Hn a chart on U.
Example 2.17 (Manifolds with Boundary). TheupperhalfspaceHn
itself is obviously a manifold with boundary, as is any closed interval in R,
any closed disk in R2, or in fact a closed ball in any Euclidean space (see
Figure2.7).(Thisisnothardtoseeintuitively.Youcanprobablyconstruct
appropriate charts yourself, or you can wait until Chapter 3 and use the
ones suggested in Problem 3-4.)
The boundary of Hn in Rn is the set of points where x = 0. If M is a
n
manifold with boundary, a point that is in the inverse image of ∂Hn under
some chart is called a boundary point of M, and a point that is in the
inverse image of IntHn is called an interior point. The boundary of M (the

---

Manifolds 35
set of all its boundary points) is denoted by ∂M; similarly, its interior is
denoted by IntM.
Note that this use of the terms “boundary” and “interior” is distinct
from their use earlier in this chapter in reference to subsets of topological
spaces:IfM isamanifoldwithboundary,itsboundaryasasubsetofitself
is always empty, even though its boundary as a manifold with boundary
may not be. Usually the distinction will be clear from the context, but if
necessary we can always distinguish the two meanings by referring to the
topological boundary or the manifold boundary as appropriate.
There is a subtlety about this definition that might not be immediately
evident. Although the interior and boundary of a manifold with boundary
M are well-defined subsets, and it might seem intuitively rather obvious
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

---

36 2. Topological Spaces
Problems
2-1. Let (X1,T 1) and (X2,T 2) be topological spaces and let f: X1 →X2
be a bijective map. Show that f is a homeomorphism if and only
if f(T 1) = T 2 in the sense that U ∈ T 1 if and only if f(U) ∈ T 2.
[This shows, roughly speaking, that the topology is precisely the in-
formation preserved by homeomorphisms, and justifies the definition
of topological spaces as the right setting for studying properties pre-
served by homeomorphisms.]
2-2. Suppose X is a set, and B is any collection of subsets of X whose
union equals X. Let T be the collection of all unions of finite inter-
sections of elements of B. (Note that the empty set is the union of
the empty collection of sets.)
(a) ShowthatT isatopology.(Itiscalledthetopology generated by
B, and B is called a subbasis for T.)
(b) Show that T is the “smallest” topology for which all the sets in
Bareopen;moreprecisely,showthatT istheintersectionofall
topologies containing B.
2-3. Let X be an infinite set. Consider the following collections of subsets
of X:
T 1 ={U ⊂X :X(cid:3)U is finite or is all of X};
T 2 ={U ⊂X :X(cid:3)U is infinite or is empty};
T 3 ={U ⊂X :X(cid:3)U is countable or is all of X}.
For each collection, determine whether it is a topology.
2-4. Let X ={1,2,3}. Give a list of topologies on X such that any topol-
ogy on X is homeomorphic to exactly one on your list.
2-5. Let X = R2 as a set, but with the topology determined by the fol-
lowing basis:
B={sets of the form {(c,y):a<y <b}, for fixed a,b,c∈R}.
Determine which (if either) of the identity maps X → R2, R2 → X
is continuous.
2-6. Let X be a discrete space, Y be a space with the trivial topology,
and Z be any topological space. Show that any maps f: X → Z
and g: Z →Y are continuous. If Z is Hausdorff, show that the only
continuous maps h: Y →Z are constant maps.
2-7. Give examples of maps between subsets of the plane (with the Eu-
clidean topology) that are

---

Problems 37
(a) open but not closed or continuous;
(b) closed but not open or continuous;
(c) continuous but neither open nor closed;
(d) continuous and open but not closed;
(e) continuous and closed but not open;
(f) open and closed but not continuous.
2-8. Let f: X →Y be a continuous map between topological spaces, and
letBbeabasisforthetopologyofX.Letf(B)denotethecollection
{f(B) : B ∈ B} of subsets of Y. If f is surjective and open, show
that f(B) is a basis for the topology of Y.
2-9. Suppose we are given an indexed collection of nonempty(cid:6)topological
spaces {X α } α∈A . Declare a subset of the disjoint union α∈A X α to
be open if and only if its intersection with each X is open.
α
(cid:6)
(a) Show that this is a topology on X , called the disjoint
α∈A α
union topology.
(b) Show that a subset of the disjoint union is closed if and only if
its intersection with each X is closed.
α
(c) I(cid:6)f each X
α
is an n-manifold, show that the disjoint union
X is an n-manifold if and only if the index set A is
α∈A α
countable.
2-10. Suppose X is locally Euclidean of dimension n, and f: X → Y is
a surjective local homeomorphism. Show that Y is also locally Eu-
clidean of dimension n.
2-11. Show that a topological space is a 0-manifold if and only if it is a
countable discrete space.
2-12. LetX beatotallyorderedset(seetheAppendix),andassumethatX
has at least two elements. For any a∈X, define sets L(a),R(a)⊂X
by
L(a)={c∈X :c<a},
R(a)={c∈X :c>a}.
GiveX thetopologygeneratedbythesubbasis{L(a),R(a):a∈X},
called the order topology.
(a) Show that each set of the form (a,b) is open in X and each set
oftheform[a,b]isclosed(where(a,b)and[a,b]aredefinedjust
as in R).
(b) Show that X is Hausdorff.

---

38 2. Topological Spaces
(c) Showthatforanya,b∈X,(a,b)⊂[a,b].Underwhatconditions
does equality hold?
2-13. Let X be a second countable topological space. Show that every col-
lection of disjoint open subsets of X is countable.
2-14. ShowthatlocallyEuclideanspacesandmetricspacesarefirstcount-
able.
2-15. (a) Show that every second countable space has a countable dense
subset.
(b) Show that a metric space is second countable if and only if it
has a countable dense subset.
2-16. Let X be a first countable space.
(a) ForanysetA⊂X andanypointp∈X,showthatp∈Aifand
only if there is a sequence {p }∞ in A such that p →p.
n n=1 n
(b) Show that for any space Y, a map f: X → Y is continuous
if and only if f takes convergent sequences in X to convergent
sequences in Y.
2-17. Show that any manifold has a basis of Euclidean balls.
2-18. Suppose M is an n-dimensional manifold with boundary. Show that
IntM isann-manifoldand∂M isan(n−1)-manifold(withoutbound-
ary).

---

3
New Spaces from Old
Inthischapterweintroducethreestandardwaysofconstructingnewtopo-
logical spaces from given ones: subspaces, product spaces, and quotient
spaces. We will explore how various topological properties are affected by
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
Let X be a space, and let A ⊂ X be any subset. We define a topology
T on A by
A
T ={U ⊂A:U =A∩V for some open set V ⊂X}.
A
Inotherwords,theopensetsofT aretheintersectionswithAoftheopen
A
sets of X (Figure 3.1).
Exercise 3.1. Prove that T A is a topology on A.

---

40 3. New Spaces from Old
X
U
V
A
FIGURE 3.1. An open set in the subspace A.
0 1 2 3
0…11 1 1
1
54 3 2
B C
FIGURE 3.2. Subspaces of R.
ThetopologyT iscalledthesubspacetopology(orsometimestherelative
A
topology) on A. A subset of a topological space X is called a subspace of
X if it is endowed with the subspace topology. Henceforth, whenever we
mention a subset of a topological space, we will always consider it as a
topological space with the subspace topology unless otherwise specified.
Exercise 3.2. Let M be a metric space, and let A ⊂ M be any subset.
Show that the subspace topology on A is the same as the metric topology
obtained by restricting the metric of M to points in A.
Example 3.1. Consider the subspaces B = [0,1] ∪ (2,3) and C =
{1/n}∞ of R (Figure 3.2). Notice that the set [0,1] is not open in R.
n=1
But it is an open subset of B, because [0,1] is the intersection with B
of the open interval (−1,2). In C, the one-point sets {1/n} are all open
(why?), so the subspace topology on B is discrete.
Theseexamplesillustratethatopennessandclosednessarenotproperties
of a set by itself, but rather of a set in relation to a particular topological
space.
An injective continuous map that is a homeomorphism onto its image
(in the subspace topology) is called a topological embedding. If f: A → X
issuchamap,wecanthinkoftheimagesetf(A)asahomeomorphiccopy
of A embedded in X.

---

Subspaces 41
Example 3.2. Let a: [0,1)→R2 be the map a(s)=(cos2πs,sin2πs). In
Exercise 2.7, you showed that a is not a homeomorphism onto its image
in the subspace topology (which is the same as the metric topology by
Exercise 3.2), so it is an example of a map that is continuous and injective
but not an embedding. However, the restriction of a to any interval [0,b)
for 0<b<1 is an embedding.
The first property we will prove about the subspace topology is so fun-
damental that, in a sense we will explain later, it completely characterizes
the subspace topology among all the possible topologies on a subset. For
anysubsetA⊂X,ι : A(cid:9)→X denotestheinclusionmapofAintoX (see
A
the Appendix).
Theorem 3.3 (Characteristic Property of Subspace Topologies).
SupposeA⊂X isasubspace.ForanytopologicalspaceY,amapf: Y →A
is continuous if and only if the following composite map from Y to X is
continuous:
Y
−f→A(cid:9)→ιA
X.
Proof. Directly from the definitions of continuity and the subspace topol-
ogy,
f: Y →A is continuous
⇐⇒ for all U ⊂ A, f−1(U) ⊂ Y
open open
⇐⇒ for all V ⊂ X, f−1(V ∩A) ⊂ Y
open open
⇐⇒ for all V ⊂ X, (ι ◦f)−1(V) ⊂ Y
A
open open
⇐⇒ ι ◦f: Y →X is continuous.
A
Proposition 3.4 (Other Properties of the Subspace Topology).
Suppose A is a subspace of the topological space X.
(a) The inclusion map ι : A (cid:9)→ X is continuous, and in fact is a topo-
A
logical embedding.
(b) If f: X →Y is continuous, then its restriction to A is continuous.
(c) If f: X →Y is continuous, then f: X →f(X) is continuous.
(d) TheclosedsubsetsofAarepreciselytheintersectionsofAwithclosed
subsets of X.
(e) If B ⊂ A is a subspace of A, then B is a subspace of X; in other
words, the subspace topologies that B inherits from A and from X
agree.

---

42 3. New Spaces from Old
A
V
X
U
B
W
FIGURE 3.3. A subspace of a subspace.
(f) If B ⊂A⊂X, B is open in A, and A is open in X, then B is open
in X.
(g) If B is a basis for the topology of X, then
B ={B∩A:B ∈B}
A
is a basis for the topology of A.
(h) Any subspace of a Hausdorff space is Hausdorff.
(i) Any subspace of a second countable space is second countable.
Proof. Part (a) follows immediately from the characteristic property, just
by taking Y to be equal to A and f to be the identity map. Then (b)
followsfrom(a),sincef| =f◦ι .Part(c)followsfromthecharacteristic
A A
property because the hypothesis says that ι f(X) ◦f: X →Y is continuous,
where ι f(X) is the inclusion of f(X) into Y.
Forpart(e),letU ⊂B beanysubset.Forthepurposesofthisproof,we
sayU is open in B relative to AifU isopeninthesubspacetopologythat
B inherits from A; U is open in B relative to X is defined similarly. Then
we argue as follows (Figure 3.3):

---

Subspaces 43
V
U
X
B
q
A
FIGURE 3.4. A basis open set for a subspace.
U is open in B relative to A
⇐⇒ U =B∩V for some V ⊂ A
open
⇐⇒ U =B∩V, where V =A∩W, W ⊂ X
open
⇐⇒ U =B∩A∩W for some W ⊂ X
open
⇐⇒ U =B∩W for some W ⊂ X (since B ⊂A)
open
⇐⇒ U is open in B relative to X.
To prove (g), we have to show that every open subset of A satisfies the
basis criterion with respect to B . Let U be an open subset of A, and let
A
q ∈ U. Then by definition U = A∩V for some open subset V ⊂ X. By
the basis criterion for V, there is an element B ∈ B such that q ∈ B ⊂ V
(Figure 3.4). It then follows that q ∈B∩A⊂U with B∩A∈B .
A
Parts (d), (f), (h), and (i) are left as an exercise.
Exercise 3.3. Complete the proof of Proposition 3.4.
We can now produce many examples of manifolds as subspaces of Eu-
clidean spaces. In particular, since the Hausdorff property and second
countability are hereditary by parts (h) and (i) of the preceding propo-
sition, to show that a subspace of Rn is a manifold we need only verify the
locally Euclidean condition.
We begin with a very general construction.
Example 3.5. IfU ⊂Rn isanopensetandf: U →Rk isanycontinuous
map, the graph of f (Figure 3.5) is the set

---

44 3. New Spaces from Old
y1,… ,y
k
Γ(f)
x2,…,x
n
x1 U
FIGURE 3.5. The graph of a continuous function.
Γ(f)={(x,y)=(x1,…,x
n
,y1,…,y
k
)∈Rn+k :x∈U and y =f(x)}.
To verify that Γ(f) is locally Euclidean, we construct an explicit homeo-
morphism between U and Γ(f). Let Φ : U →Γ(f) be the map
f
Φ (x)=(x,f(x)).
f
It is continuous because f is, and it is easily seen that its inverse is the
restriction to Γ(f) of the map π(x,y) = x (the projection onto the first
n coordinates), which is continuous by Proposition 3.4(b). Thus Φ is a
f
topological embedding. In particular, Γ(f) is (globally) homeomorphic to
the open set U ⊂Rn, so it is an n-manifold.
Example 3.6. Our next examples are arguably the most important man-
ifolds of all, so it is worth taking some time to understand them well. The
(unit) n-sphere is the set
Sn ={x∈Rn+1 :|x|=1}.

---

Subspaces 45
Inlowdimensions,spheresareeasytovisualize:S0 isthetwo-pointdiscrete
space {±1} ⊂ R; S1 is the unit circle in the plane; and S2 is the familiar
sphericalsurfaceofradius1inR3.Inthecaseofthecircle,itisoftenmore
convenient to identify the plane R2 with the set C of complex numbers by
the correspondence (x,y) ↔ x+iy, and think of the circle as the set of
complex numbers with unit modulus:
S1 ={z ∈C:|z|=1}.
To see that Sn is a manifold, we need to show that each point has a
Euclidean neighborhood. The most straightforward way is to show that
each point has a neighborhood in which Sn is the graph of a continuous
function. For each i = 1,…,n + 1, let U + denote the subset of Rn+1
i
where x > 0, and U − the set where x < 0. If x is any point in Sn, some
i i i
± ±
coordinate x must be nonzero there, so the sets U , … , U cover a
i 1 n+1
neighborhood of Sn. On U ± , we can solve the equation |x| = 1 for x and
i i
find that x∈Sn∩U ± if and only if
i
(cid:3)
x
i
=± 1−(x1)2−···−(x i−1)2−(x i+1)2−···−(x n+1)2.
In other words, the portion of Sn in U ± is the graph of a continuous
i
function, and is therefore locally Euclidean. This proves that Sn is an n-
manifold.
Here is another useful way to show that Sn is a manifold. Consider both
Rn and Sn as subsets of Rn+1 (identifying Rn with the set of points whose
x n+1 coordinateiszero),andletN =(0,…,0,1)denotethe“northpole.”
Define stereographic projection σ :Sn(cid:3){N}→Rn to be the map given by
σ(x1,…,x n+1)= (x
1
1
−
,..
x
.
n
,
+
x
1
n ) .
Geometrically, it sends a point x ∈ Sn (cid:3){N} to the point u ∈ Rn where
the line from N to x intersects Rn (Figure 3.6), as you can easily check. It
is a homeomorphism, because it has an inverse given by
σ−1(u1,…,u
n
)=
(2u1,…
|u
,2
|2
u
+
n
,
1
|u|2−1)
.
Thus Sn(cid:3){N} is homeomorphic to Rn. In particular, this provides a Eu-
clidean neighborhood of every point of Sn except N, and the analogous
projection from the south pole works in a neighborhood of N.
Example 3.7. Finally,considerthedoughnut surfaceD,whichisthesur-
face of revolution in R3 defined by revolving the circle (y−2)2 +z2 = 1
(calledthegeneratingcircle)aroundthez-axis(Figu(cid:3)re3.7).Itischaracter-
ized by the equation (r−2)2+z2 =1, where r = x2+y2. This surface
canbeparametrizedbytwoanglesθ (measuredaroundthez axisfromthe

---

46 3. New Spaces from Old
N
x
u=σ(x)
FIGURE 3.6. Stereographic projection.
xz-plane) and ϕ (measured around the generating circle from the horizon-
tallyoutwarddirection).Itismoreconvenientforcalculationstomakethe
substitutions ϕ=2πu and θ =2πv, and define a map F: R2 →D by
F(u,v)=((2+cos2πu)cos2πv,(2+cos2πu)sin2πv,sin2πu). (3.1)
This maps the plane onto D. It is not one-to-one, since F(u+k,v+l) =
F(u,v)foranypairofintegers(k,l).However,F isinjectiveifitisrestricted
toasmallenoughneighborhoodofanypoint(u0,v0),andastraightforward
calculation shows that a local inverse in a neighborhood of (u0,v0) can be
constructed from the formulas
1 z 1 y
u= tan−1 +k; v = tan−1 +l;
2π r−2 2π x
1 r−2 1 x
u= cot−1 +k; v = cot−1 +l
2π z 2π y
for suitable choices of k,l. Thus D is a 2-manifold.
The next lemma is similar to the local criterion for continuity of Lemma
2.2, in that it asserts the global continuity of a map that is known to be
continuous on certain subsets. In this case, however, the subsets must be
closed, and there can be only finitely many of them. This lemma will turn
out to be extremely useful in our investigations of surfaces.
Lemma 3.8 (Gluing Lemma). Let X be a topological space, and sup-
pose X = A1 ∪···∪A
k
, where each A
i
is closed in X. For each i, let

---

Subspaces 47
z
y
ϕ
θ
x
FIGURE 3.7. A doughnut surface of revolution.
f i : A i → Y be a continuous map such that f i | Ai ∩Aj = f j | Ai ∩Aj . There
exists a unique continuous map f: X →Y such that f| =f for each i.
Ai i
Exercise 3.4. Prove Lemma 3.8.
In choosing a topology for a subset A ⊂ X, there are two competing
priorities:Wewouldliketheinclusionmap A(cid:9)→X tobecontinuous(from
whichitfollowsbycompositionthattherestrictionto Aofanycontinuous
map f: X → Y is continuous); and we would also like continuous maps
intoX whoseimageshappentolieinAalsotobecontinuousasmapsinto
A. For the first requirement, A needs to have enough open sets, while for
the second it should not have too many. The subspace topology is chosen
as the optimal compromise between these requirements.
As we will see several times in this chapter, natural topologies like the
subspacetopologycanusuallybecharacterizedintermsofwhichmapsare
continuouswithrespecttothem.Thisiswhythe“characteristicproperty”
of the subspace topology (Theorem 3.3) is so named. The next lemma
makes this precise.
Theorem 3.9 (Uniqueness of the Subspace Topology). Suppose A
is a subset of a topological space X. The subspace topology on A is the
unique topology for which the characteristic property holds.

---

48 3. New Spaces from Old
Proof. Suppose we are given an arbitrary topology on A that is known to
satisfy the characteristic property. For this proof, let A denote A with
g
the given topology, and let A denote A with the subspace topology. To
s
show that the given topology is equal to the subspace topology, it suffices
to show that the identity map of A is a homeomorphism between A and
g
A , by Problem 2-1.
s
First we note that the inclusion map from A into X is continuous, as
g
follows:Sincetheidentitymapofanyspaceiscontinuous,thecharacteristic
property applied to the composition
A −I→d A (cid:9)→X
g g
implies that this composite map is continuous; but this composition is just
the inclusion A (cid:9)→ X itself. Of course, the inclusion map A (cid:9)→ X is
g s
also continuous, because it is the inclusion map of a subspace (Proposition
3.4(a)).
Now consider the two composite maps
A −
Id
→sgA (cid:9)→
ιg
X,
s g
A − Id →gsA (cid:9)→ιs X.
g s
Here both Id and Id represent the identity map of A, and ι and ι
gs sg s g
represent inclusion of A into X; we decorate them with subscripts only for
the purpose of discussing their continuity.
Note that ι ◦Id = ι , and ι ◦Id = ι , both of which we have just
g sg s s gs g
showntobecontinuous.Thus,applyingthecharacteristicpropertytoeach
of the compositions above, we conclude that both Id and its inverse Id
sg gs
are continuous. Therefore, Id is a homeomorphism.
sg
Product Spaces
SupposeX1,…,X
n
aretopologicalspaces.WedefineabasisintheirCarte-
sian product X1 ×···×X
n
by
B={U1 ×···×U
n
:U
i
is open in X
i
, i=1,…,n}.
Exercise 3.5. Prove that B is a basis.
ThetopologygeneratedbyBiscalledtheproducttopology,andthespace
X1 ×···×X
n
withtheproducttopologyiscalledaproductspace.Thebasis
open sets of the form U1 ×···×U
n
are called product open sets.
Forexample,intheplaneR2 =R×R,theproducttopologyisgenerated
bysetsoftheform I×J,where I and J areopensetsin R.Atypicalsuch
set is an open rectangle.

---

Product Spaces 49
Exercise 3.6. ShowthattheproducttopologyonRn =R×···×Risthe
same as the metric topology induced by the Euclidean distance function.
The product topology can also be defined in the more general setting of
infinite products, with a slightly more complicated definition. We will not
need to use infinite products in this book, but the general definition of the
product topology is given in Problem 7-12. For more information, consult
[Sie92] or [Mun75].
The characteristic property relates continuity of a map into a product
spacetocontinuityofitscomponentfunctions.Inthespecialcaseofamap
from Rn to Rm, this reduces to a familiar result from advanced calculus.
Theorem 3.10 (Characteristic Property of Product Topologies).
Let X1 ×···×X
n
be a product space. For any topological space B, a map
f: B → X1 ×···×X
n
is continuous if and only if each of its component
functions f =π ◦f is continuous:
i i
X1 ×···×X
n
(cid:3)(cid:4)
(cid:3)
f (cid:3) π i
(cid:3) (cid:5)
(cid:2)
B X .
f i
i
Proof. Since it suffices to check continuity on basis open sets,
f is continuous
⇐⇒ f−1(U1 ×···×U
n
) ⊂ B for all U
i
⊂ X
i
open open
⇐⇒ f
1
−1 (U1)∩···∩f
n
−1(U
n
)
op
⊂
en
B for all U
i op
⊂
en
X
i
.
If each f is continuous, the set in the last line above is the intersection of
i
finitely many open sets and is therefore open in B, which shows that f is
continuous. Conversely, if f is continuous, choose j between 1 and n and
take U = X for all i except i =j. Then f −1 (U ) = B when i (cid:14)= j, so the
i i i i
−1
argument above shows that f (U ) is open in B whenever U is open in
j j j
X , or in other words, f is continuous.
j j
It follows from the characteristic property that if f1,f2: X → C are
complex-valuedcontinuousfunctions,thentheirsum(f1+f2)(x)=f1(x)+
f2(x) is continuous, because it is the composition of the maps f: X →C2
given by f(x)=(f1(x),f2(x)) and s: C2 →C given by s(w,z)=w+z. A
similar remark applies to the product (f1f2)(x)=f1(x)f2(x).
Just as in the case of the subspace topology, the product topology is
uniquely determined by its characteristic property.
Theorem 3.11 (Uniqueness of the Product Topology). Let X1,
… , X
n
be topological spaces. The product topology on X1 ×···×X
n
is the
unique topology that satisfies the characteristic property.

---

50 3. New Spaces from Old
Proof. Suppose that X1 ×···×X
n
is endowed with some topology that
satisfiesthecharacteristicproperty.Firstwenotethattheprojectionmaps
π arecontinuous(ineithertopology)bythecharacteristicpropertyapplied
i
to the identity map of X1 ×···×X
n
. Now inserting X1 ×···×X
n
with
the product topology in place of B shows that the identity map from the
product topology to the given topology is continuous, and reversing roles
showsthatitsinverseisalsocontinuous.Thusthetwotopologiesareequal.
Proposition 3.12 (Other Properties of the Product Topology).
Let X1, … , X
n
be topological spaces.
(a) The projection maps π
i
: X1 ×···×X
n
→X
i
are all continuous.
(b) The product topology is “associative” in the sense that the three prod-
uct topologies X1 ×X2 ×X3, (X1 ×X2)×X3, and X1 ×(X2 ×X3)
on the set X1 ×X2 ×X3 are all equal.
(c) For any i and any points x
j
∈ X
j
, j (cid:14)= i, the map f
i
: X
i
→ X1 ×
···×X given by
n
f
i
(x)=(x1,…,x i−1,x,x i+1,…,x
n
)
is a topological embedding of X into the product space.
i
(d) If for each i, B is a basis for the topology of X , then the set
i i
{B1 ×···×B
n
:B
i
∈B
i
}
is a basis for the product topology on X1 ×···×X
n
.
(e) If A is a subspace of X for i = 1,…,n, the product topology and
i i
the subspace topology on A1 ×···×A
n
⊂X1 ×···×X
n
are equal.
(f) If each X
i
is Hausdorff, so is X1 ×···×X
n
.
(g) If each X
i
is second countable, so is X1 ×···×X
n
.
Exercise 3.7. Prove Proposition 3.12.
Iff : X →Y aremaps(continuousornot)fori=1,…,k,theirproduct
i i i
map is
f1 ×···×f
k
: X1 ×···×X
k
→Y1 ×···×Y
k
given by
f1 ×···×f
k
(x1,…,x
k
)=(f1(x1),…,f
k
(x
k
)).

---

Product Spaces 51
Proposition 3.13. A product of continuous maps is continuous, and a
product of homeomorphisms is a homeomorphism.
Proof. Becauseitsufficestocheckthattheinverseimagesofbasisopensets
areopen,thefirstclaimfollowsfromthefactthat(f1 ×···×f
k
)−1(U1 ×···×
U
k
) is just the product of the open sets f1(U1), … , f
k
(U
k
). The second
claim follows from the first, because the inverse of a bijective product map
is itself a product map.
Product spaces provide us with another rich source of examples of man-
ifolds. The key is the following proposition.
Proposition 3.14. IfM1,…,M
k
aremanifoldsofdimensionsn1,…,n
k
,
respectively, the product space M1 ×···×M
k
is a manifold of dimension
n1+···+n
k
.
Proof. Proposition 3.12 shows that the product is Hausdorff and second
countable, so only the locally Euclidean property needs to be checked.
Given any point q = (q1,…,q
k
) ∈ M1 ×···×M
k
, for each i there exists
a neighborhood U of q and a homeomorphism ϕ from U to an open
i i i i
subsetofRni.Bytheprecedinglemma,theproductmapϕ1 ×···×ϕ
k
isa
homeomorphismfromaneighborhoodofqtoanopensetinRn1+···+nk.
AparticularlyimportantexampleistheproductmanifoldTn =S1×···×
S1, which is an n-dimensional manifold called the n-torus. In particular,
the 2-torus is usually just called the torus. Because S1 is a subspace of
R2, T2 can be considered as a subspace of R4 by Proposition 3.12(e): It
is just the set of points (x1,x2,x3,x4) ∈ R4 such that (x1)2 +(x2)2 = 1
and (x3)2+(x4)2 = 1. As the next lemma shows, T2 is homeomorphic to
a familiar surface.
Lemma 3.15. The torus T2 is homeomorphic to the doughnut surface D
of Example 3.7.
Proof. The key idea is that both surfaces are parametrized by two angles.
For D, the angles are ϕ = 2πu and θ = 2πv as in (3.1); for T2, they are
the angles in the two circles. Although one must be careful using angle
functions because they cannot be defined continuously on a whole circle,
with some care we can eliminate the angles altogether and come up with
formulas that are manifestly continuous.
Withthisinmind,wewritex1 =cosθ,x2 =sinθ,x3 =cosϕ,x4 =sinϕ.
Substituting into (3.1) suggests defining a map G: T2 →D by
G(x1,x2,x3,x4)=((2+x3)x1, (2+x3)x2, x4).
This is obviously continuous, and a little algebra shows that G maps T2
into D. To see that it is a homeomorphism, just check that its inverse is

---

52 3. New Spaces from Old
given by
G−1(x,y,z)=(x/r, y/r, r−2, z),
(cid:3)
where r = x2+y2 as in Example 3.7.
Quotient Spaces
Our third technique for constructing new topological spaces from old ones
is somewhat more involved than the preceding two. It is a way to identify
some points in a given topological space with each other, to obtain a new,
smaller space.
LetX beatopologicalspace,Y beanyset,andπ: X →Y beasurjective
map.DefineatopologyonY bydeclaringasubsetU ⊂Y tobeopenifand
only if π−1(U) is open in X. This is called the quotient topology induced
by the map π.
Exercise 3.8. Show that the quotient topology is indeed a topology.
More generally, if X and Y are topological spaces, a map π: X → Y
is called a quotient map if it is surjective and continuous and Y has the
quotient topology induced by π. If π is known to be surjective, this is the
same as saying that U is open in Y if and only if π−1(U) is open in X.
An easy example to keep in mind is the map π: Rn+k → Rn given
by projection onto the first n coordinates. It is straightforward to check
directly from the definition that it is a quotient map.
Themostcommonsourceofquotientmapsisthefollowingconstruction.
Let ∼ be an equivalence relation on a topological space X (see the Ap-
pendix). For each q ∈ X let [q] denote the equivalence class of q, and let
X/∼ denote the set of equivalence classes: This is a partition of X, which
is a decomposition of X into a collection of disjoint subsets whose union
is X. Let π: X →X/∼ be the natural projection sending each element of
X to its equivalence class. Then X/∼ together with the quotient topology
determined by π is called the quotient space (or sometimes identification
space)ofX bythegivenequivalencerelation.Thequotientmapπ iscalled
the projection.
Alternatively, a quotient space can be defined by explicitly giving a par-
titionofX.Whetheragivenquotientspaceisdefinedintermsofanequiv-
alence relation or a partition is a matter of convenience.
If π: X → Y is a quotient map, a subset U ⊂ X is said to be saturated
(with respect to π) if U = π−1(V) for some subset V ⊂ Y. (In fact, you
can check that U is saturated if and only if U = π−1(π(U)).) If Y is a
quotient space determined by an equivalence relation, the saturated sets
are those that are unions of equivalence classes. More generally, for any

---

Quotient Spaces 53
quotient map π: X → Y, a subset π−1(y) ⊂ X for y ∈ Y is called a fiber
of π; a saturated set is one that is a union of fibers.
Althoughquotientmapsdonotalwaystakeopensetstoopensets,there
is a useful alternative characterization of quotient maps in terms of satu-
rated open sets.
Lemma 3.16. A continuous surjective map π: X →Y is a quotient map
if and only if it takes saturated open sets to open sets, or saturated closed
sets to closed sets.
Exercise 3.9. Prove Lemma 3.16.
Lemma 3.17. Suppose f: X →Y is a quotient map. The restriction of f
to any saturated open or closed set is a quotient map.
Exercise 3.10. Prove Lemma 3.17.
Itisnotalwaysatrivialmattertocheckthatacontinuoussurjectivemap
is a quotient map—it may well not be, as the following example shows.
Example 3.18. Consider the map a: [0,1)→S1 defined (in complex no-
tation) by a(s)=e2πis. It is surjective and continuous, but not a quotient
map, because [0,1) is a saturated open subset of [0,1) whose image is not
2
open in S1.
The following lemma gives two very useful sufficient conditions for a
surjective continuous map to be a quotient map.
Lemma 3.19. If π: X →Y is a surjective continuous map that is also an
open or closed map, then it is a quotient map.
Proof. If π is open, it takes saturated open sets to open sets (because it
takes all open sets to open sets). If π is closed, it takes saturated closed
sets to closed sets. In either case, it is a quotient map by Lemma 3.16.
One simple property of quotient maps is that they behave well with
respect to composition.
Lemma 3.20 (Composition Property of Quotient Maps). Sup-
pose π1: X → Y and π2: Y → Z are quotient maps. Then their
composition π2 ◦π1: X →Z is also a quotient map.
Proof. Just note that U ⊂ Z is open if and only if π −1 (U) is open in Y,
2
whichistrueifandonlyifπ
1
−1 (π
2
−1 (U))=(π2 ◦π1)−1(U)isopeninX.
Asithappens,quotientspacesdonotgenerallybehavewellwithrespect
to products, subspaces, bases, or topological properties such as locally Eu-
clidean, Hausdorff, or second countable. In particular, quotient spaces of
manifoldsaregenerallynotmanifolds.In fact,itisnotdifficulttoconstruct

---

54 3. New Spaces from Old
FIGURE 3.8. A quotient of B2. FIGURE 3.9. A quotient of I×I.
aquotientspaceofamanifoldthatsatisfiesallthedefinitionsofamanifold
except that it is not Hausdorff (see Problem 3-8). Thus if we wish to prove
that a given quotient space is a manifold, we have to prove at least the
locally Euclidean and Hausdorff properties directly.
The following lemma shows that in many cases this is sufficient. In par-
ticular,itshowsthataquotientofamanifoldisagainamanifold,provided
that it is locally Euclidean and Hausdorff.
Lemma 3.21. Suppose P is a second countable space and π: P →M is a
quotient map. If M is locally Euclidean, it is second countable.
Proof. Let U be a covering of M by Euclidean balls. The collection
{π−1(U) : U ∈ U} is an open cover of P, which has a countable sub-
coverbyLemma2.15.IfweletU(cid:5) ⊂UdenoteacountablesubsetofUsuch
that {π−1(U) : U ∈ U(cid:5)} covers P, then U(cid:5) is a countable cover of M by
Euclidean balls. Each such ball has a countable basis, and the union of all
these bases is a countable basis for M.
Becausequotientspacesareprobablylessfamiliartoyouthansubspaces
or products, we will introduce a number of examples before going any
farther.
Example 3.22. The map α: [0,1]→S1 given by α(s)=e2πis is a closed
map and therefore a quotient map.
Example 3.23. Let B2 denote the closed unit disk in R2. Let ∼ be the
equivalencerelationonB2 generatedby(x,y)∼(−x,y)forall(x,y)∈∂B2
(Figure 3.8). (You can think of this space as being obtained from B2 by
“pasting” the left half of the boundary to the right half.) We will see in
Chapter 6 that B2/∼ is homeomorphic to S2.
Example 3.24. Let I = [0,1] denote the closed unit interval in the real
line; we will generally just call this the unit interval. Define an equivalence
relation on the square I ×I by setting (x,0) ∼ (x,1) for all x ∈ I, and
(0,y) ∼ (1,y) for all y ∈ I (Figure 3.9). This can be visualized as the
space obtained by gluing the top boundary segment of the square to the

---

Quotient Spaces 55
FIGURE 3.10. Wedge of two lines. FIGURE3.11.Wedgeoftwocircles.
bottom to form a cylinder, and then gluing the left-hand boundary circle
of the resulting cylinder to the right-hand one. Later we will see that the
resulting quotient space is homeomorphic to the torus.
Example 3.25. Let X1,…,X
k
be topological spaces, and let q
i
∈ X
i
.
The wedge of X1,…,X
k
(also called their one-point union), written X1 ∨
···∨X
k
, is the quotient space obtained from X1 (cid:20)···(cid:20)X
k
by identifying
q1 ∼ ··· ∼ q
k
. In other words, we glue the spaces together by identifying
all their distinguished points together. For example, the wedge R∨R is
homeomorphictotheunionofthex-axisandthey-axisintheplane(Figure
3.10), and the wedge S1∨S1 is homeomorphic to the figure eight space E
consisting of the union of the two circles of radius 1 centered at (0,1) and
(0,−1) in the plane (Figure 3.11). A wedge of finitely many copies of S1 is
sometimes called a bouquet of circles.
Example 3.26. Define an equivalence relation on R by declaring x∼y if
x and y differ by an integer. We will see below that the resulting quotient
space is homeomorphic to the circle.
Example 3.27. Consider the map q: Rn+1(cid:3){0}→Sn defined by q(x)=
x/|x|. Observe that q is continuous and surjective, and the fibers of q are
raysinRn+1(cid:3){0}.Thusthesaturatedsetsaretheunionsofrays,anditis
easytocheckthatq takessaturatedopensetstoopensetsandistherefore
a quotient map.
Example 3.28. Define Pn, the real projective space of dimension n, to be
thesetof1-dimensionallinearsubspaces(linesthroughtheorigin)inRn+1.
There is a natural map π: Rn+1 (cid:3){0} → Pn defined by sending a point
x to its span. We topologize Pn by giving it the quotient topology with
respect to this map.

---

56 3. New Spaces from Old
Thisspacecanalsobeviewedinanotherway.Ifwedefineanequivalence
relationonRn+1(cid:3){0}bydeclaringtwopointsx,ytobeequivalentifx=λy
for some nonzero real number λ, then there is an obvious identification
between Pn and the set of equivalence classes. Under this identification,
the map π defined above is just the map sending a point to its equivalence
class.
The Characteristic Property of the Quotient Topology
Thecharacteristicpropertyofthequotienttopologyisevenmoreimportant
than those of the subspace or product topologies.
Theorem 3.29 (Characteristic Property of Quotient Topologies).
Let π: X → Y be a quotient map. For any topological space B, a map
f: Y → B is continuous if and only if the composite map f ◦ π is
continuous:
X
(cid:6)
π (cid:6) f ◦π
(cid:6)
(cid:5) (cid:6)(cid:7)
(cid:2)
Y B.
f
Proof. Iff iscontinuous,f◦π iscontinuousbycomposition.Conversely,if
f◦π iscontinuousandU ⊂B isopen,thenπ−1(f−1(U))=(f◦π)−1(U)is
openinX,whichimpliesf−1(U)isopeninY bydefinitionofthequotient
topology. Thus f is continuous.
Thecharacteristicpropertyhasthefollowingextremelyimportantcorol-
lary:
Corollary 3.30 (Passing to the Quotient). Suppose π: X → Y is a
quotient map, B is a topological space, and f: X → B is any continuous
map that is constant on the fibers of π (i.e., if π(p) = π(q), then f(p) =
f(q)). Then there exists a unique continuous map f (cid:7) : Y → B such that
f =f
(cid:7)◦π:
X
(cid:6)
π (cid:6) f
(cid:6)
(cid:5) (cid:6)(cid:7)
(cid:2)
Y B.
(cid:7)
f
(cid:7)
Proof. The existence and uniqueness of f follow from elementary set the-
ory: Given q ∈Y, there is some p∈X such that π(p)=q, and we can set
(cid:7) (cid:7)
f(q)=f(p)foranysuchp.Thehypothesisonf guaranteesthatf isunique

---

Quotient Spaces 57
(cid:7)
andwell-defined.Continuityoff isthenimmediatefromthecharacteristic
property.
In the situation of the preceding corollary, we say that the map f passes
to the quotient or descends to the quotient.
In the case of quotient spaces, there are two slightly different ways of
phrasing the uniqueness associated with the characteristic property. The
first one says that the characteristic property uniquely characterizes quo-
tient maps.
Theorem 3.31 (Characterization of Quotient Maps). LetX andY
be topological spaces, and let π: X → Y be any surjective map. Then π is
a quotient map if and only if the characteristic property holds.
Proof. Ifπisaquotientmap,thecharacteristicpropertyholdsbyTheorem
3.29. Conversely, suppose π has the characteristic property. Applying the
characteristic property to the diagram
X
(cid:6)
π (cid:6) π
(cid:6)
(cid:5) (cid:6)(cid:7)
(cid:2)
Y Y
Id
shows that π is continuous because the identity is. To show that π is a
quotientmap,wewillshowthatY withthegiventopologyishomeomorphic
to Y with the quotient topology. As before, let Y and Y denote Y with
g q
the given and quotient topologies, respectively, and let Id , Id , π , and
gq qg q
π have the obvious meanings. Then the characteristic property applied to
g
the two diagrams
X X
(cid:6) (cid:6)
π (cid:6) π π (cid:6) π
g q q g
(cid:6) (cid:6)
(cid:5) (cid:6)(cid:7) (cid:5) (cid:6)(cid:7)
(cid:2) (cid:2)
Y Y Y Y
g Id q q Id g
gq qg
showsthatId andId arebothcontinuous,fromwhichtheresultfollows.
qg gq
The second uniqueness result says that quotient spaces are uniquely de-
terminated up to homeomorphism by the identifications made by their quo-
tient maps.
Corollary 3.32 (Uniqueness of Quotient Spaces). Suppose
π1: X → Y1 and π2: X → Y2 are quotient maps that make the
same identifications (i.e., π1(p) = π1(q) if and only if π2(p) = π2(q)).
Then there is a unique homeomorphism ϕ: Y1 →Y2 such that ϕ◦π1 =π2.

---

58 3. New Spaces from Old
Proof. By Corollary 3.30, both π1 and π2 pass uniquely to the quotient as
in the following diagrams:
X X
(cid:6) (cid:6)
π1 (cid:6) π2 π2 (cid:6) π1
(cid:6) (cid:6)
(cid:5) (cid:6)(cid:7) (cid:5) (cid:6)(cid:7)
(cid:2) (cid:2)
Y1
π(cid:8)
2
Y2 Y2
π(cid:8)
1
Y1.
Sincebothdiagramsabovecommute,itfollowsthatπ(cid:8) 1 ◦(π(cid:8) 2 ◦π1)=π(cid:8) 1 ◦π2 =
π1. Consider another diagram:
X
(cid:6)
π1 (cid:6) π1
(cid:6)
(cid:5) (cid:6)(cid:7)
(cid:2)
Y1 Y1.
If the bottom arrow is interpreted as either π(cid:8) 1 ◦π(cid:8) 2 or the identity map of
Y1, this diagram will commute; by the uniqueness part of Corollary 3.30,
these maps must be equal. Similarly, π(cid:8) 2 ◦π(cid:8) 1 is the identity on Y2. Thus
ϕ=π(cid:8) 2 is the required homeomorphism, and it is the unique such map by
the uniqueness statement of Corollary 3.30.
Group Actions
Ournextconstructionisafar-reachinggeneralizationofExamples3.26and
3.28. A topological group is a group G endowed with a topology such that
the maps μ: G×G→G and ι: G→G given by
μ(g1,g2)=g1g2, ι(g)=g−1
arecontinuous,wheretheproductandinversearethoseofthegroupstruc-
true of G. A discrete group is a topological group that has the discrete
topology.
Example 3.33. Each of the following is a topological group.
- The real line R with its additive group structure and the Euclidean
topology.
- The set R∗ =R(cid:3){0} of nonzero real numbers under multiplication,
with the subspace topology.
- The set C∗ = C(cid:3){0} of nonzero complex numbers under complex
multiplication, with the subspace topology.

---

Group Actions 59
- Thegeneral linear groupGL(n,R),whichisthesetofn×ninvertible
realmatricesundermatrixmultiplication,withthesubspacetopology
inherited from
Rn2
.
- Any group with the discrete topology.
Exercise 3.11. Verify that each of the above examples is a topological
group.
Lemma 3.34. Any subgroup of a topological group is a topological group
with the subspace topology. Any finite product of topological groups is a
topological group with the direct product group structure and the product
topology.
Exercise 3.12. Prove Lemma 3.34.
In view of Lemma 3.34, each of the following is a topological group:
- Euclidean space Rn as a group under vector addition.
- The circle S1 ⊂C∗ under complex multiplication, with the subspace
topology.
- The n-torus Tn =S1×···×S1 with the direct product group struc-
true.
- The orthogonal group O(n), which is the subgroup of GL(n,R) con-
sisting of matrices A such that AAt is the identity.
IfGisatopologicalgroupandg ∈G,thelefttranslationmapL : G→G
g
defined by L (g(cid:5)) = gg(cid:5) is continuous, because it is the restriction of the
g
multiplication map to {g}×G. Because L ◦L = Id , left translation
g g−1 G
by any element of g is a homeomorphism of G. Similarly, right translation
R (g(cid:5))=g(cid:5)g is also a homeomorphism.
g
Suppose G is a group and X is a topological space. A left action of G
·
on X is a map G×X → X, written (g,x) (cid:10)→ g x, with the following
properties:
· · ·
(i) For any x∈X and any g1,g2 ∈G, g1 (g2 x)=(g1g2) x.
·
(ii) For all x∈X, 1 x=x.
·
Similarly, a right action is a map X×G→X, written (x,g)(cid:10)→x g, with
· ·
thesamepropertiesexceptthatcompositionworksinreverse:(x g1) g2 =
·
x (g1g2).Anyrightactiondeterminesaleftactioninacanonicalway,and
vice versa, by the correspondence
g · x=x · g−1.

---

60 3. New Spaces from Old
Thus for many purposes, the choice of left or right action is a matter of
taste. We usually choose to focus on left actions because the composi-
tion law mimics composition of functions, and unless we specify otherwise,
groups will always be understood to act on the left. However, we will see
some situations in which an action appears naturally as a right action.
If G is a topological group, an action of G on a space X is said to be
continuousifthemapG×X →X iscontinuous.Thismeans,inparticular,
·
thatforeachg ∈Gthemapx(cid:10)→g xiscontinuousfromX toitself,because
itistherestrictionoftheactiontothesubspace{g}×X ⊂G×X.In fact,
each such map is a homeomorphism, because the definition of a group
action guarantees that it has a continuous inverse x (cid:10)→ g−1 · x. When G
is discrete, it is easy to check that the action is continuous if and only if
·
x(cid:10)→g x is continuous for each g ∈G.
· ·
For any x ∈ X, the set G x = {g x : g ∈ G} is called the orbit of x.
Theactionissaidtobetransitiveifforeverypairofpoints x,y ∈X,there
·
is a group element g such that g x=y or equivalently if the only orbit is
the entire space X. It is said to be free if the only element of G that has
·
any fixed points is the identity, i.e., g x=x for some x implies g =1.
Example 3.35 (Continuous Group Actions).
(a) ThegenerallineargroupGL(n,R)actscontinuouslyontheleftonRn
by matrix multiplication, each vector in Rn considered as a column
matrix. Because any nonzero vector in Rn can be taken to any other
by a linear transformation, there are only two orbits: Rn(cid:3){0} and
{0}.
(b) The orthogonal group O(n) acts continuously on Rn by matrix mul-
tiplication as well; this is just the restriction of the action in part
(a)toO(n)×Rn ⊂GL(n,R)×Rn.Sinceorthogonaltransformations
preservelengthsofvectors,andanyvectorcanbetakentoanyother
of the same length by an orthogonal transformation, the orbits are
{0} and the spheres centered at 0.
(c) The restriction of the action of O(n) to the unit sphere in Rn yields
a transitive action on Sn−1.
(d) The group R∗ acts on Rn(cid:3){0} by scalar multiplication. The action
isfree,andtheorbitsarethelinesthroughtheorigin(withtheorigin
removed).
(e) Any topological group G acts freely and transitively on itself on the
left by left translation: g · g(cid:5) = L (g(cid:5)) = gg(cid:5). Similarly, G acts on
g
itself on the right by right translation.
Given an action of G on a space X, we define an equivalence relation on
·
X by setting x1 ∼ x2 if there is an element g ∈ G such that g x1 = x2.

---

Group Actions 61
The equivalence classes are precisely the orbits of the group action. The
resulting quotient space is denoted by X/G, and is called the orbit space
of the action. If the action is transitive, the orbit space is a single point, so
only nontransitive actions yield interesting examples.
Exercise 3.13. Verify that the real projective space Pn of Example 3.28
istheorbitspaceoftheactionofR∗ onRn+1(cid:3){0}byscalarmultiplication.
Aparticularlyimportantspecialcaseariseswhenweconsiderasubgroup
Γ of a topological group G (with the subspace topology). Group multipli-
cation on the left or right defines a left or right action of Γ on G; it is just
the restriction of the action of G on itself to Γ×G or G×Γ. This action
is continuous and free, but in general not transitive. An orbit of the right
action of Γ on G is a set of the form {gγ : γ ∈ Γ}, which is precisely the
left coset gΓ. Thus the orbit space of the right action of Γ on G is the set
G/Γ of left cosets with the quotient topology. This quotient space is called
the(left) coset spaceofGbyΓ.(Itisunfortunatebutunavoidablethatthe
right action produces a left coset space and vice versa. If G is abelian, the
situation is simpler, because then the left action and right action of Γ are
equal to each other.)
Example 3.36. As an application, let us consider the coset space R/Z.
Because Z (with the discrete topology) is a subgroup of the topological
groupR,thereisanaturalfreecontinuousactionofZonRbytranslation:
·
n x = n+x. (Because R is abelian, we might as well consider it as a
left action.) The orbits are exactly the equivalence classes of the relation
defined in Example 3.26 above, x ∼ y if and only if x−y ∈ Z. Thus the
quotient space of that example is the same as the coset space R/Z.
Consider also the map ε: R→S1 defined by
ε(s)=e2πis.
It is straightforward to check that this is a local homeomorphism and thus
an open map, so it is a quotient map. Because it makes the same identifi-
cations as the quotient map R → R/Z, the uniqueness of quotient spaces
tellsusthatR/ZishomeomorphictoS1.(Wewillbereturningtothismap
ε, which we call the exponential quotient map, extensively in this book.)
Moregenerally,thediscretesubgroupZnactsfreelyonRnbytranslation.
By similar reasoning, the quotient space Rn/Zn is homeomorphic to the
n-torus Tn =S1×···×S1.
We will see more examples of this technique in the next few chapters.

---

62 3. New Spaces from Old
Problems
3-1. Showthatafiniteproductofopenmapsisopen,andafiniteproduct
of closed maps is closed.
3-2. By considering the space X = [0,1] ⊂ R, and the sets A0 = {0},
A = [1/(i+1),1/i] for i = 1,2,…, show that the gluing lemma
i
(Lemma3.8)isfalseif{A1,…,A
k
}isreplacedbyaninfinitesequence
of closed sets.
3-3. Formulatea“characteristicproperty”forthedisjointuniontopology
(Problem 2-9) and prove that the disjoint union topology is uniquely
characterized by it.
3-4. Use stereographic projection to show that any closed ball in Rn is an
n-dimensional manifold with boundary.
3-5. Let X be a topological space. The diagonal of X ×X is the subset
Δ={(x,x):x∈X}⊂X×X.ShowthatX isHausdorffifandonly
if Δ is closed in X×X.
3-6. If X1,…,X
k
are topological spaces, show that the projections
π
i
: X1 ×···×X
k
→X
i
are quotient maps.
3-7. Let M =R ×R, where R is the set R with the discrete topology.
d d
(a) Show that M is homeomorphic to the space X of Problem 2-5.
(b) Show that M is locally Euclidean (of what dimension?) and
Hausdorff, but not second countable.
3-8. Let X be the subset R×{0}∪R×{1} of R2. Define an equivalence
relation on X by declaring (x,0) ∼ (x,1) if x (cid:14)= 0. Show that the
quotient space X/∼ is locally Euclidean and second countable, but
not Hausdorff. (This space is called the line with two origins.)
3-9. Lemma 3.17 showed that the restriction of a quotient map to a satu-
rated open set is still a quotient map. Show that the “saturated”
hypothesis is necessary, by giving an example of a quotient map
f: X →Y andanopensubsetU ⊂X suchthatf| issurjectivebut
U
not a quotient map.
3-10. Show that real projective space Pn is an n-manifold. [Hint: Consider
the subsets U ⊂Rn+1 where x =1.]
i i
3-11. Let CPn denote the set of all 1-dimensional complex subspaces of
Cn+1,calledn-dimensional complex projective space.TopologizeCPn
as the quotient Cn+1 (cid:3){0}/C∗, where C∗ is the group of nonzero
complex numbers acting by scalar multiplication. Show that CPn is
a 2n-manifold. [Hint: Mimic what you did in Problem 3-10.]

---

Problems 63
3-12. Let G be a topological group and let H ⊂ G be a subgroup. Show
that H is also a subgroup.
3-13. If G is a group that is also a topological space, show that G is a
topologicalgroupifandonlyifthemapG×G→Ggivenby(x,y)(cid:10)→
xy−1 is continuous.
3-14. Let G be a topological group and Γ⊂G be a subgroup.
(a) For any g ∈ G, show that left translation L : G → G passes
g
tothequotientG/Γanddefinesahomeomorphismof G/Γwith
itself.
(b) AtopologicalspaceX issaidtobehomogeneousifforanyx,y ∈
X, there is a homeomorphism ϕ: X → X taking x to y. Show
that every coset space is homogeneous.
3-15. Let G be a topological group acting continuously on a topological
space X.
(a) Show that the quotient map π: X →X/G is open.
(b) Show that X/G is Hausdorff if and only if the orbit relation
·
{(x1,x2)∈X×X :x2 =g x1 for some g ∈G}
is closed in X×X.
3-16. If Γ is a normal subgroup of the topological group G, show that the
coset space G/Γ is a topological group. [Hint: It might be helpful to
use Problems 3-1 and 3-15(a).]

---

4
Connectedness and Compactness
In this chapter we treat two topological properties that will be of central
importance in our study of manifolds: connectedness and compactness.
The definition of connectedness is formulated so that connected spaces
will behave similarly to intervals in the real line, so, for example, a contin-
uous real-valued function on a connected space satisfies the intermediate
value theorem. Similarly, compactness is defined so that compact spaces
willhavemanyofthesamepropertiesenjoyedbyclosedandboundedsub-
sets of Euclidean spaces. In particular, continuous real-valued functions on
compact sets always achieve their maxima and minima.
Connectedness
One of the most important elementary facts about continuous functions is
the intermediate value theorem: If f is a continuous real-valued function
defined on a closed bounded interval [a,b], then f takes on every value be-
tweenf(a)andf(b).Thekeyideahereisthe“connectedness”ofintervals.
In this section we generalize this concept to topological spaces.
Definitions and Basic Properties
IfX isatopologicalspace,aseparationofX isapairofnonempty,disjoint,
opensubsetsU,V ⊂X suchthatX =U∪V.WesaythatX isdisconnected
if there exists a separation of X, and connected otherwise.

---

66 4. Connectedness and Compactness
FIGURE 4.1. Union of two disks. FIGURE 4.2. The x-axis minus 0.
Bythisdefinition,connectednessisapropertyofaspace,notaproperty
of subsets like openness or closedness. We can also talk about connected
subsets of a topological space, by which we always mean connected in the
subspace topology. In this context we can also consider a separation of A
to be a pair of open subsets U,V ⊂ X whose intersections with A are
nonempty and disjoint, and whose union contains A: This is equivalent to
the original definition because the open subsets of A are exactly the open
subsets of X intersected with A.
Example 4.1. Each of the following subspaces of the plane is discon-
nected.
(a) X istheunionofthetwodisjointcloseddisksB1(2,0)andB1(−2,0)
(Figure 4.1). Each of the disks is open in X, so the pair of disks is a
separation of X.
(b) Y is the x-axis minus the origin (Figure 4.2). The two sets {(x,0) :
x>0} and {(x,0):x<0} separate Y.
(c) Z isthesetofpointswithrationalcoordinates.Aseparationisgiven
by, say, {(x,y):x<π} and {(x,y):x>π}.
On the other hand, it is intuitively clear that the open and closed unit
disks, the circle, the whole plane, and the x-axis are all connected, at least
in the everyday sense of the word. Proving it, however, is not so easy,
because we would have to show that it is impossible to find a separation.
We will soon come up with an easy technique for proving connectedness
that will work in most practical cases, including that of manifolds.
Here is a useful alternative characterization of connectedness.
Proposition 4.2. A space X is connected if and only if the only subsets
of X that are both open and closed in X are ∅ and X itself.
Proof. Suppose first that X is connected, and assume that U ⊂X is open
andclosed.ThenV =X(cid:3)U isalsoopenandclosed.IfbothU andV were
nonempty, then {U,V} would be a separation of X; therefore, either V is
empty, which means that U =X, or U is empty.

---

Connectedness 67
Conversely, if X is disconnected, we can write X =U ∪V where U and
V are nonempty, open, and disjoint. This implies that U is open, closed,
not empty, and not equal to X.
The most important feature of connectedness is that continuous images
of connected sets are connected.
Theorem 4.3 (Main Theorem on Connectedness). Let X,Y be
topological spaces and let f: X → Y be a continuous map. If X is con-
nected, then f(X) is connected.
Proof. Suppose f(X) is not connected. Then there exist open sets U,V ⊂
Y whose intersections with f(X) are nonempty and disjoint and whose
union contains f(X). It follows immediately that {f−1(U),f−1(V)} is a
separation of X, so X is not connected.
Proposition 4.4 (Properties of Connected Sets).
(a) Suppose X is any space and U,V are disjoint open subsets of X. If
A is a connected subset of X contained in U ∪V, then either A⊂U
or A⊂V.
(b) SupposeX isanyspaceandA⊂X isconnected.ThenAisconnected.
(c) Let X be a space, and let {B α } α∈A be a(cid:2)ny collection of connected
subspaces with a point in common. Then B is connected.
α∈A α
(d) Any product of finitely many connected spaces is connected.
(e) Any quotient space of a connected space is connected.
Proof. For part (a), if A contained points in both U and V, then {A∩
U,A∩V} would be a separation of A.
To prove part (b), suppose U and V are disjoint open subsets of X that
separate A. By (a), A is contained in one of the sets, say A ⊂ U. Each
point of V has a neighborhood (namely V) disjoint from A, so every point
of V is exterior to A. Therefore, A ⊂ U, which means that A∩V = ∅, a
contradiction.
For part (c), let(cid:2)q be a point contained in each B
α
, and suppose {U,V}
is a separation of B . Suppose without loss of generality that q lies
α∈A α
in U. By part (a), each B must be entirely contained in U, and thus so is
α
their union.
Forpart(d),sinceX1 ×···×X
k
=(X1 ×···×X k−1)×X
k
,byinductionit
sufficestoconsideraproductoftwospaces.ThusletX andY beconnected,
andsuppose{U,V}isaseparationofX×Y.Chooseanypoint(x0,y0)∈U.
The set {x0 }×Y is connected because it is homeomorphic to Y; since it
contains the point (x0,y0)∈U, it must be entirely contained in U by part
(a). For each y ∈ Y, the set X ×{y} is also connected and has a point

---

68 4. Connectedness and Compactness
U V
a c b
FIGURE 4.3. Proof that an interval is connected.
(x0,y) ∈ U, so it must also be contained in U. Since the sets X ×{y}
exhaust X×Y, the result follows.
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
are open subsets U,V ⊂R that separate J. Choose a∈U ∩J, b∈V ∩J,
and assume (interchanging U and V if necessary) that a<b (Figure 4.3).
Then [a,b] ⊂ J because J is an interval. Since U and V are both open in
R, there exists ε>0 such that [a,a+ε)⊂U ∩J and (b−ε,b]⊂V ∩J.
Letc=sup(U∩[a,b]).Byourchoiceofε,a+ε≤c≤b−ε.Inparticular,
c is between a and b, so c∈J ⊂U ∪V. But if c were in U, it would have
a neighborhood (c−δ,c+δ)⊂U, which would contradict the definition of
c. Similarly, c∈V leads to a contradiction. Therefore, J is connected.
Conversely,assumethatJ isnotaninterval.Thismeansthatthereexist
a < c < b with a,b ∈ J but c (cid:14)∈ J. Then the sets (−∞,c) and (c,∞)
separate J, so J is not connected.
Animmediateconsequenceofthispropositionisthefollowinggeneralized
intermediate value theorem.
Theorem 4.6 (Intermediate Value Theorem). Suppose X is a con-
nected topological space, and f is a continuous real-valued function on X.
If p,q ∈X, then f takes on all values between f(p) and f(q).
Proof. The image set f(X) is connected, so it must be an interval.

---

Connectedness 69
Path Connectedness
Now we can give a simple but powerful sufficient condition for connected-
ness, based on the following definitions. Let X be a topological space and
p,q ∈X. A path in X from p to q is a continuous map f: [0,1]→X such
that f(0) = p and f(1) = q. We say that X is path connected if for every
p,q ∈X, there is a path in X from p to q.
Theorem 4.7. Path connectedness implies connectedness.
Proof. SupposethatX ispathconnectedbutnotconnected,andlet{U,V}
be a separation of X. We can choose p∈U and q ∈V (since neither set is
empty), and find a path f from p to q in X. Then f−1(U) and f−1(V) are
disjoint open subsets of [0,1] that cover [0,1]; moreover, 0 ∈ f−1(U) and
1∈f−1(V),soneithersetisempty.Thisimpliesthat[0,1]isdisconnected,
which is a contradiction.
Example 4.8. The following spaces are all easily shown to be path con-
nected, and therefore they are connected.
(a) Rn.
(b) Any subset B ⊂Rn that is convex, which means that for any x,x(cid:5) ∈
B, the line segment from x to x(cid:5) lies entirely in B.
(c) Rn(cid:3){0} for n≥2.
Example 4.9. The following spaces are also connected.
(a) Sn forn≥1,becauseitisaquotientspaceofRn+1(cid:3){0}byExample
3.27.
(b) The n-torus Tn, because it is a product of connected spaces.
On the other hand, path connectedness is stronger in general than con-
nectedness. Here is an example of a space that is connected but not path
connected.
Example 4.10. Define subsets of the plane by
A={(x,y):x=0 and y ∈[−1,1]};
B ={(x,y):y =sin(1/x) and x∈(0,1]}.
Let X = A∪B (Figure 4.4). X is called the topologist’s sine curve. In
Problem 4-5 you will show that it is connected but not path connected.

---

70 4. Connectedness and Compactness
B
A
FIGURE 4.4. The topologists’s sine curve.
Components and Path Components
Look back at Example 4.1. Our first example of a disconnected set, the
union of two disjoint closed disks, could be separated in only one way,
becauseanyotherseparationwouldinduceaseparationofoneoftheclosed
disks, which is path connected. The same reasoning applies to the second
example, the x-axis minus the origin. The set of rational points in the
plane,however,admitsinfinitelymanypossibleseparations.Identifyingthe
possible separations of a space amounts to finding “maximal” connected
subsets, a concept we now explore more fully.
Let X be a topological space. Define a relation on X, called the connec-
tivity relation, by saying that p∼q if there exists a connected subset of X
containing both p and q.
Lemma 4.11. The connectivity relation is an equivalence relation.
Proof. It is reflexive because {q} is a connected subset containing q, and
symmetric because p ∼ q and q ∼ p both mean that there is a connected
subset containing p and q. To prove transitivity, suppose p∼q and q ∼r,
which means that there are connected subsets A containing {p,q} and B
containing {q,r}. Since A and B have the point q in common, A∪B is
connected by Proposition 4.4(c). Thus A∪B is a connected set containing
{p,r}, so p∼r.
The equivalence classes in X under the connectivity relation are called
the components of X.

---

Connectedness 71
Lemma 4.12. The components of X are exactly the maximal connected
subsets of X, that is, connected sets that are not contained in any larger
connected set.
Proof. Given q ∈X, let A be the component of X containing q, and let B
be the union of all connected sets containing q. Then B itself is connected
by Proposition 4.4(c), and is thus a maximal connected subset. If p ∈ B,
thenp,qlieintheconnectedsubsetB,sop∼qandthusp∈A.Conversely,
if p∈A, then p∼q, so p lies in some connected subset containing q. Since
B is the union of all such subsets, p∈B.
Example 4.13. Consider the disconnected subsets of Example 4.1.
(a) ThecomponentsofX (theunionoftwodisjointcloseddisks)arethe
two disks themselves.
(b) The components of Y (the x-axis minus the origin) are the positive
x-axis and the negative x-axis.
(c) InthesetZ ofpointswithrationalcoordinates,ifpandq aredistinct
points of Z, they must differ in one of their coordinates, say their
x-coordinates. Choosing an irrational number α between the two x-
coordinates, the sets where x < α and x > α give a separation of Z
in which p and q lie in different subsets. Therefore, p and q cannot
both be contained in any connected subset, so p is not equivalent to
q. Thus the components of Z are the one-point subsets.
Proposition 4.14 (Properties of Components). Let X be any space.
(a) Each component of X is closed in X.
(b) Any connected subset of X is contained in a single component.
Proof. If B is any component of X, it follows from Proposition 4.4(b)
that B is a connected set containing B. Since components are maximal
connected sets, B =B, so B is closed.
Suppose A ⊂ X is connected. Since the components cover X, A has a
point in common with some component B. By Proposition 4.4(c) A∪B is
connected, so by maximality of B, it must be equal to B. This means that
A⊂B.
Althoughcomponentsarealwaysclosed,theymaynotbeopeningeneral,
sotheydonotnecessarilyseparatethespace.ConsiderthesetZ ofrational
points in the plane, for example: Its components are single points, which
are not open sets.
Wecanalsoapplytheconstructionusedtodefinecomponentswithpath
connectedness in place of connectedness. Define the path connectivity rela-
tion for points p,q in a space X by saying p ∼ q if there is a path in X
p
from p to q.

---

72 4. Connectedness and Compactness
Exercise 4.1. Show that ∼ is an equivalence relation.
p
The equivalence classes under ∼ are called the path components of X.
p
Proposition 4.15 (Properties of Path Components). Let X be any
space.
(a) Each path component is contained in a single component, and each
component is a disjoint union of path components.
(b) If A ⊂ X is path connected, then A is contained in a single path
component.
Exercise 4.2. Prove Proposition 4.15.
WesaythataspaceX islocallyconnectedifitadmitsabasisofconnected
open sets, and locally path connected if it admits a basis of path connected
open sets. To put it more concretely, for any p∈X and any neighborhood
U of p, p has a (path) connected neighborhood contained in U. Clearly,
any locally path connected space is locally connected.
A space can be connected but not locally connected, as is, for example,
thetopologist’ssinecurve(seeProblem4-5);anditcanbelocallyconnected
but not connected, as is the disjoint union of two closed disks.
Lemma 4.16. Let X be any space.
(a) If X is locally connected, then each component of X is open.
(b) If X is locally path connected, then each path component of X is
open, its path components are the same as its components, and it is
connected if and only if it is path connected.
Proof. FirstassumethatX islocallyconnected,andletAbeacomponent
of X. If p ∈ A, then p has a connected neighborhood U by local connect-
edness, and this neighborhood must lie entirely in A by Lemma 4.14(b).
Thus every point of A has a neighborhood in A; in other words, A is open.
NowassumethatX islocallypathconnected.Thesameargument,with
“connected” replaced by “path connected,” shows that each path compo-
nent is open. Let q ∈ X, and let A be the component containing q, and
B the path component. By Proposition 4.15(a), we know that B ⊂A and
A can be written as a disjoint union of path components, each of which is
open in X and thus in A. If B is not the only path component in A, then
the pair {B,A(cid:3)B} is a separation of A, which is a contradiction because
Aisconnected.ThisprovesthatA=B.Finally,X beingconnectedmeans
it has only one component, which by the above argument is the same as
havingonlyonepathcomponent,whichinturnisequivalenttobeingpath
connected.

---

Compactness 73
Proposition 4.17. Every manifold is locally path connected.
Exercise 4.3. Prove Proposition 4.17.
This proposition means that in our work with manifolds we can use
connectedness and path connectedness interchangeably. This will simplify
many arguments because path connectedness is so much easier to check.
Compactness
Another fundamental fact about continuous functions is the extreme value
theorem (Theorem A.10 in the Appendix): A continuous real-valued func-
tiononaclosed,boundedsubsetofRn attainsitsmaximumandminimum
values.
Thistheorem,ofcourse,failsingeneralformetricspaces,and“bounded”
doesnotevenmakesenseintopologicalspaces.Buttheessentialpropertyof
closedandboundedsubsetsofRn thatmakestheproofwork,compactness,
makessenseinarbitrarytopologicalspaces.Thispropertyisthesubjectof
the rest of this chapter.
Definitions and Basic Properties
Recall that an open cover of a space X is a collection U of open subsets of
X whose union is X, and a subcover of U is a subcollection of U that still
covers X. A topological space X is said to be compact if every open cover
of X has a finite subcover; or in other words, if given any open cover U of
X,therearefinitelymanysetsU1,…,U
k
∈UsuchthatX =U1 ∪···∪U
k
.
As in the case of connectedness, when we say that a subset A of a topo-
logical space X is compact, we always mean with respect to the subspace
topology unless otherwise specified. A subspace A ⊂ X is compact if and
only if given any collection of open subsets of X whose union contains A
(which we also call an open cover of A), there is a finite subcover.
Themostimportantfactaboutcompactspacesisthatcontinuousimages
of compact spaces are compact.
Theorem 4.18 (Main Theorem on Compactness). Let X,Y be
topological spaces and let f: X →Y be a continuous map. If X is compact,
then f(X) is compact.
Proof. Let U be an open cover of f(X). (As noted in the remark above,
we can take the elements of U either to be open subsets of f(X) in the
subspacetopology,ortobeopensubsetsofY whoseunioncontainsf(X).)
ForeachU ∈U,f−1(U)isanopensubsetofX.SinceUcoversf(X),every
point of X is in some set f−1(U), so the collection {f−1(U):U ∈U} is an
open cover of X. By compactness of X, some finite number of these, say

---

74 4. Connectedness and Compactness
U
p1
A
p1 V p1
U
q
V
p2 V p2
U
p2
FIGURE 4.5. The case B ={q}.
{f−1(U1),…,f−1(U
k
)}, cover X. Then it follows that {U1,…,U
k
} cover
f(X).
Proposition 4.19 (Properties of Compact Spaces).
(a) Every closed subset of a compact space is compact.
(b) In a Hausdorff space X, compact sets can be separated by open sets.
That is, if A,B ⊂X are disjoint compact subsets, there exist disjoint
open sets U,V ⊂X such that A⊂U and B ⊂V.
(c) Every compact subset of a Hausdorff space is closed.
(d) Every finite product of compact spaces is compact.
(e) Every quotient of a compact space is compact.
Proof. For part (a), let U be a cover of A by open subsets of X.
Then U ∪ {X (cid:3) A} is an open cover of X, which has a finite subcover
{U1,…,U
k
,X(cid:3)A}. Therefore, A must be covered by the finite collection
{U1,…,U
k
}.
To prove (b), first consider the case in which B = {q} is a one-point
set. For each p ∈ A, there exist disjoint open sets U containing p and V
p p
containing q by the Hausdorff property. The collection {U : p ∈ A} is an
p
open cover of A, so it has a finite subcover: Call it {U ,…,U } (Figure
p1 pk
4.5). Let U = U ∪···∪U and V = V ∩···∩V . Then U and V are
p1 pk p1 pk
disjoint open sets with A⊂U and {q}⊂V, so this case is proved.
Next consider the case of a general compact subset B. The argument
above shows that for each q ∈B there exist disjoint open subsets U ,V ⊂
q q
X such that A ⊂ U and q ∈ V . By compactness of B, finitely many of
q q
these, say {V ,…,V }, cover B. Then setting U =U ∩···∩U and
q1 qm q1 qm
V =V ∪···∪V proves the result.
q1 qm

---

Compactness 75
Y
U1
U2
X
x
U3
FIGURE 4.6. Finding a finite cover of the strip Zx ×Y.
For (c), suppose X is Hausdorff and A ⊂ X is compact. For any point
q ∈ X (cid:3)A, by part (b) there exist disjoint open sets U containing A and
V containing q. In particular, V is a neighborhood of q disjoint from A, so
every such q is exterior to A. This means that A is closed.
Toprove(d),itsufficesbyinductiontoconsideraproductX×Y oftwo
compact spaces. Let U be an open cover of X ×Y. Choose any x ∈ X.
The “slice” {x}×Y is homeomorphic to Y, so finitely many of the sets
of U cover it, say U1,…,U
k
(Figure 4.6). Because product open sets are
a basis for the product topology, for each y ∈ Y there is a product open
set V ×W ⊂ X ×Y such that (x,y) ∈ V ×W ⊂ U1 ∪···∪U
k
. Finitely
many of these product sets cover {x}×Y, say V1 ×W1,…,V
m
×W
m
. If
we set Z
x
=V1 ∩···∩V
m
, then it is evident that the whole “strip” Z
x
×Y
is actually contained in U1 ∪···∪U
k
.
Thus we have shown the following: For each x∈X, there exists an open
subsetZ ⊂X suchthatZ ×Y iscoveredbyfinitelymanyofthesetsinU.
x x
The collection {Z :x∈X} is an open cover of X, which by compactness
x
hasafinitesubcover,say{Z ,…,Z }.SincefinitelymanysetsofUcover
x1 xk
eachstripZ ×Y,andfinitelymanysuchstripscoverX×Y,wearedone.
xi
Finally, part (e) is immediate from Theorem 4.18, since a quotient of a
compact space is the image of a compact space by a continuous map.
Part (d) is actually true in the more general context of infinite products
(see [Sie92] or [Mun75]); in its general form, it is known as Tychonoff’s
theorem.

---

76 4. Connectedness and Compactness
Exercise 4.4. LetXbeacompactspace,andsuppose{Fn }isacountable
collectionofnonemptyclosedsubse(cid:9)tsofXthatarenested,whichmeansthat
Fn ⊃Fn+1 for each n. Show that
n
Fn is nonempty.
One of the main applications of compactness is the following generaliza-
tion of the extreme value theorem of elementary calculus.
Theorem 4.20 (Extreme Value Theorem). If X is a compact space
and f: X →R is continuous, then f is bounded and attains its maximum
and minimum values on X.
Proof. By the main theorem on compactness, f(X) is a compact subset of
R,sobyPropositionA.6itisclosedandbounded.Inparticular,itcontains
its supremum and infimum.
The next lemma expresses an important property of compact metric
spaces, which we will use frequently later in the book. Recall that the di-
ameterofasetS inametricspaceisdefinedtobediam(S)=sup{d(x,y):
x,y ∈S}. If U is an open cover of a metric space, a number δ >0 is called
a Lebesgue number for the cover if any set whose diameter is less than δ is
contained in one of the sets U ∈U.
Lemma 4.21 (Lebesgue Number Lemma). Any open cover of a
compact metric space has a Lebesgue number.
Proof. LetUbeanopencoverofthecompactmetricspace M.Eachpoint
x∈M is in some set U ∈U. Since U is open, there is some r(x)>0 such
that B2r(x)(x) ⊂ U. The balls {B r(x)(x) : x ∈ M} form an open cover of
M, so finitely many of them, say B r(x1)(x1),…,B r(xn )(x n ), cover M.
Wewillshowthatδ =min{r(x1),…,r(x
n
)}isaLebesguenumberforU.
To see why, suppose S ⊂M is a nonempty set whose diameter is less than
δ. Let y be any point of S; then there is some x i such that y ∈ B r(xi )(x i )
(Figure 4.7). It suffices to show that any other point of S is in B2r(xi )(x
i
),
since the latter set is by construction contained in some U ∈ U. If z ∈ S,
the triangle inequality gives
d(z,x )≤d(z,y)+d(y,x )<δ+r(x )≤2r(x ),
i i i i
which proves the claim.
Sequential and Limit Point Compactness
The definition of compactness in terms of open covers lends itself to sim-
ple proofs of some rather powerful theorems, but it does not convey much
intuitive content. There are two other properties that are equivalent to
compactness for manifolds and metric spaces (though not for arbitrary
topological spaces), and that give a more vivid picture of what compact-
ness really means. A space X is said to be limit point compact if every

---

Compactness 77
U 2r(x i )
x r(x )
i i
S y
z
FIGURE 4.7. Proof of the Lebesgue number lemma.
infinite subset of X has a limit point in X, and sequentially compact if
every sequence of points in X has a subsequence that converges to a point
in X.
Proposition 4.22. Compactness implies limit point compactness.
Proof. Suppose X is compact, and let S ⊂ X be an infinite subset. If S
hasnolimitpoint,theneverypointx∈X hasaneighborhoodU suchthat
U ∩S is either empty or {x}. Finitely many of these neighborhoods cover
X.Butsinceeachsuchneighborhoodcontainsatmostonepointof S,this
implies that S is finite, which is a contradiction.
Problem 4-7 shows that the converse of this proposition is not true in
general.
Lemma 4.23. For first countable Hausdorff spaces, limit point compact-
ness implies sequential compactness.
Proof. Suppose X is first countable, Hausdorff, and limit point compact,
and let {p } be any sequence of points in X. If the sequence takes on only
n
finitelymanyvalues,thenithasaconstantsubsequence,whichiscertainly
convergent. So we may suppose it takes on infinitely many values.
By hypothesis the set of values {p } has a limit point q ∈ X. If q is
n
actuallyequaltop forinfinitelymanyvaluesofn,againthereisaconstant
n
subsequence and we are done; so by discarding finitely many terms at the
beginningofthesequenceifnecessarywemayassumep (cid:14)=qforalln.First
n
countability of X means that there is a countable neighborhood basis atq,
say {B
n
: n = 1,2,…}. By replacing B
n
with B1 ∩···∩B
n
if necessary,
we may assume that the neighborhood basis is nested: B1 ⊃B2 ⊃···. For

---

78 4. Connectedness and Compactness
such a neighborhood basis, it is easy to see that any subsequence {p }
ni
such that p ∈B converges to q.
ni i
Since q is a limit point, we can choose n1 such that p
n1
∈ B1. Suppose
by induction that we have chosen n1 < n2 < ··· < n
k
with p
ni
∈ B
i
. By
theHausdorffproperty,q hasaneighborhoodU disjointfromthefiniteset
{p n : 1 ≤ n ≤ n k }, and by definition of limit point there is some n k+1
(necessarily greater than n
k
) such that p
nk+1
∈U ∩B k+1. This completes
the induction, and proves that there is a subsequence {p } converging to
ni
q.
Thenextresultshowsthatformanifoldsandmostoftheotherspaceswe
willbeconsideringinthisbook,wecanuseallthreenotionsofcompactness
interchangeably.
Proposition 4.24. For metric spaces and second countable Hausdorff
spaces, compactness, limit point compactness, and sequential compactness
are all equivalent.
Proof. We have shown that compactness implies limit point compactness
for all spaces, and limit point compactness implies sequential compactness
for first countable Hausdorff spaces, which include both metric spaces and
second countable Hausdorff spaces. So it remains to show that a metric
space or second countable Hausdorff space that is sequentially compact is
actually compact.
Suppose first that X is second countable and sequentially compact. (For
this part we do not need the Hausdorff property.) Any open cover U of
X has a countable subcover {U : n = 1,2,…} by Lemma 2.15. Suppose
n
that no finite subcollection of U ’s covers X. This means that for each
n
n there exists q
n
∈ X such that q
n
(cid:14)∈ U1 ∪···∪U
n
. By hypothesis, the
sequence {q } has a convergent subsequence q → q. Now, q ∈ U for
n nk m
somembecausetheU ’scoverX,andthenconvergenceofthesubsequence
n
means that there exists some N such that q ∈ U whenever k ≥ N.
nk m
But by construction, q
nk
(cid:14)∈ U1 ∪ ··· ∪ U
m
as soon as n
k
≥ m, which
is a contradiction. This proves that finitely many of the U ’s cover X.
n
Therefore, second countable sequentially compact spaces are compact.
Finally, let M be a sequentially compact metric space. We will show
that M is second countable, which by the above argument implies that M
iscompact.FromProblem2-15,itsufficestoshowthatM hasacountable
dense subset.
The key idea is to show first that sequential compactness implies the
following weak form of compactness for metric spaces: For each ε>0, the
opencoverofM consistingofallε-ballshasafinitesubcover.Supposethis
is not true for some ε. Construct a sequence as follows. Let q1 ∈ M be
arbitrary. Since B
ε
(q1) (cid:14)= M, there is a point q2 (cid:14)∈ B
ε
(q1). Similarly, since
B
ε
(q1)∪B
ε
(q2) (cid:14)= M, there is a point q3 in neither of the two preceding
ε-balls. Proceeding by induction, we construct a sequence {q } such that
n

---

Compactness 79
for each n,
q n+1 (cid:14)∈B ε (q1)∪···∪B ε (q n ). (4.1)
Replacing this sequence by a convergent subsequence (which still satisfies
(4.1)),wecanassumeq →q ∈M.SinceconvergentsequencesareCauchy,
n
as soon as n is large enough we have d(q n+1,q
n
) < ε, which contradicts
(4.1).
Now, for each n let q
(n)
,…,q
(n)
be finitely many points such that the
1 kn
balls of radius 1/n around these points cover M. The collection of points
{q (n)} is countable, and is easily seen to be dense. This shows that M is
i
second countable and completes the proof.
Exercise 4.5. Show that every compact metric space is complete.
The Closed Map Lemma
The next lemma, though simple, is among the most useful results in this
entire chapter.
Lemma 4.25 (Closed Map Lemma). Suppose F is a continuous map
from a compact space to a Hausdorff space.
(a) F is a closed map.
(b) If F is surjective, it is a quotient map.
(c) If F is injective, it is a topological embedding.
(d) If F is bijective, it is a homeomorphism.
Proof. Let F: X → Y be such a map. If A ⊂ X is closed, it is com-
pact, since any closed subset of a compact space is compact (Proposition
4.19(a)). Therefore, F(A) is compact by the main theorem on compact-
ness, and closed in Y because compact subsets of Hausdorff spaces are
closed(Proposition4.19(c)).ThisshowsthatF isaclosedmap.Ifinaddi-
tion F is surjective, it is a quotient map by Lemma 3.19. If it is bijective,
the fact that it is closed implies that its inverse is continuous, so it is a
homeomorphism (Exercise 2.14). Finally, if F is injective, it is bijective
onto its image, so the fact that it is an embedding follows from (d).
Here are some immediate applications of the closed map lemma.
In Example 3.24 we constructed a quotient space of the square I ×I
by gluing the side boundary segments together and the top and bottom
boundarysegmentstogether,andweclaimedthatitwashomeomorphicto
thetorus.Hereisaproof.Constructanothermapq: I×I →T2 bysetting
q(u,v)=(cos2πu,sin2πu,cos2πv,sin2πv).Bytheclosedmaplemma,this
is a quotient map. Since it makes the same identifications as the quotient

---

80 4. Connectedness and Compactness
mapwestartedwith,theoriginalquotientofI×I mustbehomeomorphic
to the torus by the uniqueness of quotient spaces.
InLemma3.15weshowedthatthedoughnutsurfaceishomeomorphicto
the torus by a rather laborious explicit computation. Now that lemma can
be proved much more simply, as follows. Consider the map F: R2 → R3
defined in Example 3.7. The restriction of this map to I ×I is a quotient
map by the closed map lemma. Since it makes the same identifications
as the map q in the preceding paragraph, the two quotient spaces D and
S1 ×S1 are homeomorphic. (The homeomorphism is the map that sends
q(u,v) to F(u,v).)
Another application of the closed map lemma is the following useful
result. You should notice how the closed map lemma, invoked twice in the
proof, allows us to avoid ever having to prove continuity directly by ε-δ
estimates.
Proposition 4.26. Let K be a compact convex subset of Rn with
nonempty interior. Then K is homeomorphic to the closed unit ball Bn,
by a homeomorphism that sends Sn−1 to ∂K.
Proof. Let q be an interior point of K. By replacing K with its image
under the translation x (cid:10)→ x−q (which is a homeomorphism of Rn with
itself), we can assume 0 ∈ IntK. Then there is some ε > 0 such that the
ball B (0) is contained in K; using the dilation x (cid:10)→ x/ε, we can assume
ε
Bn =B1(0)⊂K.
Thecoreoftheproofisthefollowingclaim:Eachraystartingattheorigin
intersects∂K inexactlyonepoint.SinceK iscompact,itsintersectionwith
each closed ray is compact; thus there is a point x0 in this intersection at
which the distance to the origin assumes its maximum. This point is easily
seen to lie in the boundary of K. To see that there can be only one such
point, we will show that the line segment from 0 to x0 consists entirely
of interior points of K, except for x0 itself. Since B1(0) ⊂ K, every line
segment from x0 to a point y ∈B1(0) is contained in K. As y ranges over
B1(0),theselinesegmentssweepoutasetC shapedlikeanicecreamcone
(Figure 4.8). Around each point λx0 for 0≤λ<1, it is easy to check that
there is a ball of radius 1−λ contained in C and hence in K. Thus x0 is
the only boundary point of K on the ray.
Now we define a map f: ∂K →Sn−1 by
x
f(x)= .
|x|
In words, f(x) is the point where the line segment from the origin to x
intersects the sphere. Since f is the restriction of a continuous map, it is
continuous, and the discussion in the preceding paragraph shows that it is
bijective. Since ∂K is compact, f is a homeomorphism by the closed map
lemma.

---

Locally Compact Hausdorff Spaces 81
K
x0
C
λx0
0
FIGURE 4.8. Proof that there is only one boundary point on a ray.
Finally, define F: Bn →K by
(cid:10) (cid:11)
x
F(x)=|x|f−1 .
|x|
Then F is continuous because f−1 is. Geometrically, F takes each radial
line segment from 0 to a point ω ∈ Sn linearly onto the radial segment
from 0 to the point f−1(ω) ∈ ∂K. By convexity, F takes its values in
K. The map F is injective, since points on distinct rays are mapped to
distinctrays,andeachradialsegmentismappedlinearlytoitsimage.Itis
surjective because each point y ∈ K is on some ray from 0. By the closed
map lemma, F is a homeomorphism.
Locally Compact Hausdorff Spaces
Compact Hausdorff spaces have many of the familiar properties of sub-
setsofEuclideanspaces.However,whileallmanifoldsareHausdorff,many
interestingmanifoldsarenotcompact.Nonetheless,manyoftheniceprop-
erties of compact Hausdorff spaces carry over to a more general class of
spaces, which we now define.
AtopologicalspaceX issaidtobelocallycompactifforeveryq ∈X there
isacompactsubsetofX containinganeighborhoodofq.Inthisgenerality,
thedefinitionisnotparticularlyuseful,anddoesnotseemparalleltoother

---

82 4. Connectedness and Compactness
definitions of what it means for a topological space to possess a property
“locally,” which usually entails the existence of a basis of open sets with a
particularproperty.ButwhencombinedwiththeHausdorffproperty,local
compactness is much more useful. A subset A of a topological space X is
said to be precompact or relatively compact if A is compact.
Proposition 4.27. Let X be a Hausdorff space. The following are equiv-
alent.
(a) X is locally compact.
(b) Each point of X has a precompact neighborhood.
(c) X has a basis of precompact open sets.
Proof. Clearly, (c) =⇒ (b) =⇒ (a), so all we have to prove is (a) =⇒
(c). It suffices to show that if X is locally compact Hausdorff, then each
pointx∈X hasaneighborhoodbasisofprecompactopensets.LetK ⊂X
beacompactsetcontaininganeighborhoodU ofx.ThecollectionVofall
neighborhoods of x contained in U is clearly a neighborhood basis at x.
BecauseX isHausdorff,K isclosedinX.IfV ∈V,thenV ⊂K (because
V ⊂U ⊂K andK isclosed),andthereforeV iscompact(becauseaclosed
subset of a compact set is compact). Thus V is the required neighborhood
basis.
Lemma 4.28 (Shrinking Lemma). Let X be a locally compact Haus-
dorff space. If x ∈ X and U is any neighborhood of x, there exists a pre-
compact neighborhood V of x such that V ⊂U.
Proof. Suppose x∈X and U is a neighborhood of x. If W is any precom-
pactneighborhoodofx,thenW(cid:3)U isclosedinW andthereforecompact.
Because open sets separate compact sets in a Hausdorff space, there are
disjoint open sets Y containing x and Y(cid:5) containing W (cid:3)U (Figure 4.9).
Let V = Y ∩W. Because V ⊂ W, V is compact. Because V ⊂ Y, which
is disjoint from Y(cid:5), we have V ⊂W (cid:3)Y(cid:5). Now the fact that W (cid:3)U ⊂Y(cid:5)
means that W (cid:3)Y(cid:5) ⊂U, so V ⊂U.
Lemma 4.29. Any open or closed subset of a locally compact Hausdorff
space is locally compact Hausdorff.
Proof. LetX bealocallycompactHausdorffspace.Notethatanysubspace
ofX isHausdorff,soonlylocalcompactnessneedstobechecked.IfY ⊂X
is open, the shrinking lemma says that any point in Y has a neighborhood
whose closure is compact and contained in Y, so Y is locally compact.
Suppose Z ⊂ X is closed. Any x ∈ Z has a precompact neighborhood U
in X. Since U ∩Z = U ∩Z is a closed subset of the compact set U, it
is compact, so U ∩Z is a precompact neighborhood of x in Z. Thus Z is
locally compact.

---

Locally Compact Hausdorff Spaces 83
Y(cid:5)
x
Y
W
U
FIGURE 4.9. Proof of the shrinking lemma.
Exercise 4.6. Show that any finite product of locally compact Hausdorff
spaces is locally compact Hausdorff.
Example 4.30 (Locally Compact Hausdorff Spaces).
(a) Euclidean space Rn is locally compact Hausdorff, because any closed
ball B (x) is a precompact neighborhood of x. Thus every open or
ε
closed subset of Rn is locally compact Hausdorff.
(b) Let M be a manifold, and let U be a cover of M by Euclidean balls.
Each U ∈ U has a basis of open sets that are precompact in U and
thusalsoinM,andtheunionofallsuchbasesisabasisforM.Thus
any manifold is locally compact Hausdorff.
The last example shows that every manifold has a basis of precompact
open sets. For later use, we will need the following refinement of that fact.
LetM beann-manifold.AEuclideanballB ⊂M iscalledregularifithas
the following properties:
(i) There is a Euclidean ball B(cid:5) ⊂M containing B.
(ii) For some r >0, there is a chart ϕ: B(cid:5) →B2r (0)⊂Rn that sends B
onto B (0).
r
Lemma 4.31. Every manifold has a countable basis of regular Euclidean
balls.
Proof. Let M be an n-manifold. Every point of M is contained in a Eu-
clidean neighborhood, and since M is second countable, a countable col-
lection U={U :i∈N} of such neighborhoods covers M by Lemma 2.15.
i
For each of these open sets U , choose a homeomorphism ϕ from U to an
i i i
open set U (cid:7) ⊂Rn.
i
Now let B be the collection of all open subsets of M of the form
ϕ −1 (B (x)), where x ∈ U (cid:7) is a point with rational coordinates and r is
i r i

---

84 4. Connectedness and Compactness
(cid:7)
U
i
M
ϕ
i
3r
ϕ (q)
U i 2r
i
x r
q V
FIGURE 4.10. Showing that the collection B is a basis.
any positive rational number such that B2r (x) ⊂ U (cid:7)
i
. Since there are only
countably many such balls for each U , the collection B is countable. For
i
any such set B =ϕ −
i
1 (B
r
(x))∈B, let B(cid:5) =ϕ −
i
1 (B2r (x)). To show that B
isaregularball,weneedtoshowthatB ⊂B(cid:5) andϕ (B)=B (x).Wewill
i r
−1 −1
show,equivalently,thatϕ (B (x))=B.Now,ϕ (B (x))iscompactand
i r i r
thereforeclosedinM (becauseM isHausdorff),soB ⊂ϕ −1 (B (x))⊂B(cid:5).
i r
This means that the closure of B in M is equal to its closure in B(cid:5), which
−1
is ϕ (B (x)), since ϕ is a homeomorphism.
i r i
To show that the collection B is a basis, it suffices to show that each
opensubsetofM satisfiesthebasiscriterionwithrespecttoit.LetV ⊂M
beanyopensubsetandq ∈V.Thenq ∈U forsomei,andϕ (V ∩U )isan
i i i
(cid:7)
opensubsetofU containingϕ (q)(Figure4.10).Choosearationalnumber
i i
r >0 small enough that B3r (ϕ
i
(q))⊂ϕ
i
(V ∩U
i
), and then choose a point
x ∈ ϕ (V ∩U ) with rational coordinates such that |x−ϕ (q)| < r. Then
i i i
ϕ
i
(q) ∈ B
r
(x), and it follows from the triangle inequality that B2r (x) ⊂
ϕ (V ∩U ).Therefore,B =ϕ −1 (B (x))isinB,containsq,andiscontained
i i i r
in V, thus completing the proof.
The closed map lemma is powerful, but it applies only when the domain
is compact. The following proposition provides a useful generalization of
the closed map lemma to noncompact spaces. A continuous map is said to
be proper if the inverse image of each compact subset of Y is compact.
Proposition 4.32. Suppose f: X → Y is a continuous map between lo-
cally compact Hausdorff spaces. If f is proper, it is a closed map.

---

Locally Compact Hausdorff Spaces 85
Proof. Let K ⊂X be a closed set. We will show that f(K) contains all of
its boundary points, which means that it is closed in Y.
If y ∈ Y is a boundary point of f(K), let U be a precompact neigh-
borhood of y. An easy verification shows that y is also a boundary point
of f(K)∩U. Because f is proper, f−1(U) is compact, which implies that
K∩f−1(U)iscompact.Bycontinuity, f(K∩f−1(U))=f(K)∩U iscom-
pact and therefore closed in Y. In particular, y ∈ f(K)∩U ⊂ f(K), so
f(K) is closed.
Theorem 4.33 (Baire Category Theorem). In a locally compact
Hausdorff space or a complete metric space, any countable collection of
dense open subsets has dense intersection.
Proof. Suppose {V n } n∈N is a countable collection of dense open subsets of
suchaspaceX.Weneedto(cid:9)showthatifU ⊂X isanonemptyopensubset,
the intersection of U with V is nonempty.
n n
FirstconsiderthecaseinwhichX islocallycompactHausdorff.SinceV1
isdense,U∩V1isnonempty,sobytheshrinkinglemmathereisanonempty
precompact open set W1 such that W1 ⊂ U ∩ V1. Similarly, there is a
nonemptyprecompactopensetW2 suchthatW2 ⊂W1 ∩V2 ⊂U∩V1 ∩V2.
Continuingbyinduction,weobtainasequenceofnestednonemptycompact
sets W1 ⊃ W2 ⊃ ··· ⊃ W
n
⊃ ··· (cid:9)such that W
n
⊂ U ∩V1 ∩···∩ (cid:9)V
n
. By
Exercise 4.4, there is a point x∈ W , which is clearly in U ∩ V as
n n n n
well.
In the case that X is a complete metric space, we modify the above
proof as follows. At the inductive step, since W n−1 ∩ V n is open and
nonempty,thereissomeballB (x )containedintheintersection.Choos-
εn n
ing r < min(ε ,1/n), we obtain a sequence of nested closed balls such
n n
that B
rn
(x
n
)⊂U ∩V1 ∩···∩V
n
. Because r
n
→0, the c(cid:9)enters {x
n
} form
a Cauchy sequence, which converges to a point x∈U ∩ V .
n n
The Baire category theorem has a useful complementary reformulation.
A subset F of a topological space X is said to be nowhere dense if its
closure contains no nonempty open set.
Corollary 4.34. In a locally compact Hausdorff space or a complete met-
ricspace,anycountablecollectionofnowheredensesetshasemptyinterior.
Proof. Let X be such a space, and let {F } be a countable collection of
n
nowhere dense subsets of X. Replacing each F by its closure, we may
n
assume that the sets are closed. Then their(cid:9)complements U
n
are open and
d(cid:2)ense, so by t(cid:9)he Baire category theorem
n
U
n
is dense. It follows that
F =X(cid:3) U cannot contain any nonempty open set.
n n n n
For example, it is easy to show that the solution set to any polynomial
equation in two variables is nowhere dense in R2. Since there are only

---

86 4. Connectedness and Compactness
countably many polynomials with rational coefficients, this corollary im-
plies that there are points in the plane (a dense set of them, in fact) that
satisfy no rational polynomial equation.
The name of the theorem derives from the (astonishingly unedifying)
terminology used by Baire: He defined a set of the first category to be a
countable union of nowhere dense sets, and a set of the second category to
be any set that is not of the first category. The theorem proved by Baire
wasthatforspacessatisfyingthehypothesis,everyopensetisofthesecond
category. Although the category terminology is mostly ignored nowadays,
the name of the theorem has stuck.
As we mentioned in Chapter 3, quotient maps do not generally behave
well with respect to products. In particular, it is not always true that the
product of two quotient maps is again a quotient map. However, it turns
out that the product of a quotient map with the identity map of a locally
compact Hausdorff space is indeed a quotient map, as the next lemma
shows.ThiswillbeusedinChapter7;theproofisrathertechnicalandcan
safely be skipped on first reading.
Lemma 4.35. Suppose π: X → Y is a quotient map and K is a locally
compact Hausdorff space. The map π×Id: X×K →Y ×K is a quotient
map.
Proof. We need to show that π × Id takes saturated open sets in X ×
K to open sets in Y × K. Let U ⊂ X × K be a saturated open set.
Given (x0,k0) ∈ U, we will show that (x0,k0) has a saturated product
neighborhoodW×J containedinU.Itthenfollowsthatπ(W)×J contains
(π(x0),k0),iscontainedinπ×Id(U),andisopen(sinceπ(W)istheimage
ofasaturatedopensetunderthequotientmapπ).Thusπ×Id(U)isopen
in Y ×K.
Now we proceed to prove the existence of the desired saturated prod-
uct neighborhood. For any subset W ⊂ X, we define its saturation to be
Sat(W)=π−1(π(W)); it is the smallest saturated subset containing W.
By definition of the product topology, (x0,k0) has a product neighbor-
hoodW0 ×J0 ⊂U.Bytheshrinkinglemma,thereisaprecompactneighbor-
hood J of k0 such that J ⊂J0, and thus (x0,k0)∈W0 ×J ⊂W0 ×J0 ⊂U
(Figure 4.11). Because U is saturated, it follows that Sat(W0)×J ⊂ U.
Now,Sat(W0)×J isasaturatedsubsetofX×K,butnotnecessarilyopen
(since π may not be an open map).
We will show that there exists an open set W1 ⊂X containing Sat(W0)
such that W1 × J ⊂ U. To prove this, fix some x ∈ Sat(W0). For any
k ∈ J, (x,k) has a product neighborhood in U. Finitely many of these
cover the compact set {x}×J; call them V1 ×J1,…,V
m
×J
m
. If we set
V
x
=V1 ∩···∩V
m
,thenV
x
isaneighborhoodof{x}suchthatV
x
×J ⊂U.
Taking W1 to be the union of all such sets V
x
for x ∈ Sat(W0) proves the
claim.

---

Locally Compact Hausdorff Spaces 87
K
U
J (x0,k0)
W0 x
X
Sat(W0)
W1
FIGURE 4.11. Finding a saturated product neighborhood.
Repeating this construction, we obtain a sequence of open sets W ⊂X
i
such that
W0 ⊂Sat(W0)⊂W1 ⊂Sat(W1)⊂···
and W ×J ⊂ U. Let W be the union of all the W ’s. Then W is open
i i
because it is a union of open sets, and W ×J ⊂ U. Moreover, W ×J is
saturated: If (x,k) ∈ W ×J, then x is in some W ; and if (x(cid:5),k) is any
i
point in the same fiber, then x(cid:5) ∈ W i+1, so (x(cid:5),k) ∈ W ×J as well. Thus
W ×J is the required saturated product neighborhood of (x0,k0).

---

88 4. Connectedness and Compactness
Problems
4-1. (a) If U is any open subset of R and x ∈ U, show that U (cid:3){x} is
disconnected.
(b) Show that a topological space cannot be both a 1-manifold and
an n-manifold for any n>1.
4-2. Show that the union of the x-axis and the y-axis in R2 is not a
manifold in the subspace topology.
4-3. Showthatany n-manifoldisadisjointunionofcountablymanycon-
nected n-manifolds.
4-4. Suppose f: X → Y is a surjective local homeomorphism. If X is
locally connected, locally path connected, or locally compact, show
that Y has the same property.
4-5. Let X be the topologist’s sine curve (Example 4.10).
(a) Show that X is connected but not path connected or locally
connected.
(b) Determine the components and the path components of X.
4-6. Like Problem 3-7, this problem constructs a space that is locally Eu-
clideanandHausdorffbutnotsecondcountable.Unlikethatexample,
however, this one is connected.
(a) Recallthatatotallyorderedsetissaidtobewell-orderedifevery
nonempty subset has a smallest element (see the Appendix).
Showthatthewell-orderingtheorem(TheoremA.2)impliesthat
there exists an uncountable well-ordered set Y such that for
every p∈Y, there are only countably many q <p. [Hint: Let X
be any uncountable well-ordered set. If X does not satisfy the
desired condition, let Y be an appropriate subset of X.]
(b) Now let
(cid:12) (cid:13)
L= Y ×[0,1) (cid:3){(a0,0)},
where a0 is the smallest element of Y. We give L the dictionary
order: This means that (p,q) < (r,s) if either p < r, or p = r
and q < s. With the order topology, L is called the long line.
Show that L is locally Euclidean and Hausdorff but not second
countable.
(c) Show that L is path connected.
4-7. Define a topology on Z by declaring a set A to be open if and only
if n ∈ A implies −n ∈ A. Show that Z with this topology is second
countable and limit point compact but not compact.

---

Problems 89
4-8. Let V be a finite-dimensional real vector space. A norm on V is a
real-valued function on V, written v (cid:10)→|v|, satisfying
- Positivity: |v|≥0, and |v|=0 if and only if v =0.
- Homogeneity: |cv|=|c||v| for any c∈R and v ∈V.
- Triangle inequality: |v+w|≤|v|+|w|.
Anormdeterminesametricbyd(v,w)=|v−w|.Showthatallnorms
determine the same topology on V. [Hint: Consider the restriction of
the norm to the unit sphere.]
4-9. SupposeK andLarecompactconvexsetsinRn,bothwithnonempty
interior. Show that any continuous map f: ∂K →∂L has a continu-
ous extension to a map F: K → L. If f is a homeomorphism, show
that F can be chosen to be a homeomorphism also.
4-10. Let X be a noncompact, locally compact Hausdorff space. The one-
point compactification of X is the topological space X∗ defined as
follows.Let∞besomeobjectnotinX,andletX∗ =X(cid:20){∞}with
the following topology:
T ={open subsets of X}
∪{U ⊂X∗ :X∗(cid:3)U is a compact subset of X}.
(a) Show that T is a topology.
(b) Show that X∗ is a compact Hausdorff space.
(c) Show that X is open and dense in X∗ and has the subspace
topology.
4-11. If X and Y are noncompact, locally compact Hausdorff spaces, show
that a continuous map f: X → Y extends to a continuous map
f∗: X∗ →Y∗ if and only if it is proper.
4-12. Let σ : Sn (cid:3){N} → Rn be stereographic projection, as defined in
Example 3.6. Show that σ extends to a homeomorphism of Sn with
the one-point compactification of Rn.
4-13. If M is a noncompact n-manifold, show that its one-point compact-
ification is an n-manifold if and only if there exists a precompact
open subset U ⊂M such that M (cid:3)U is homeomorphic to Rn(cid:3)Bn.
[Hint: You may find the inversion map I:Rn(cid:3)Bn →Bn defined by
I(x)=x/|x|2 useful.]
4-14. Suppose M is a 1-dimensional manifold with boundary. Show that
the interior and boundary of M are disjoint. Use this to conclude
that M is a manifold if and only if ∂M =∅.

---

5
Simplicial Complexes
In this chapter we give a brief introduction to simplicial complexes. These
are spaces constructed from building blocks called simplices, which are
points, line segments, filled-in triangles, solid tetrahedra, and their higher-
dimensional analogues. They provide a highly useful way of constructing
topological spaces, and play a fundamental role in geometry and algebraic
topology.
As we did with manifolds, we will define simplicial complexes in two
stages, starting with a very concrete version and proceeding to the most
general definition. Concretely, we think of a simplicial complex as a col-
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
manifolds.Theseresultswillbeusedinthenextchapterassteppingstones
toward classifying curves and surfaces up to homeomorphism.
Attheendofthechapterweexploretwocombinatorialpropertiesofsim-
plicial complexes that are important in the study of manifolds. The first
is the concept of an orientation of a complex, which generalizes and sys-
tematizes the intuitive notions of “direction” in 1-dimensional complexes,

---

92 5. Simplicial Complexes
FIGURE 5.1. Simplices.
“clockwise” and “counterclockwise” in 2-dimensional ones, and “handed-
ness” in 3-dimensional ones. The second is the Euler characteristic, which
is the alternating sum of the numbers of simplices in different dimensions,
and generalizes Euler’s classical formula for compact convex polyhedra in
R3.
Euclidean Simplicial Complexes
We begin with a little linear algebra. An affine map between vector spaces
is a map f: V → W of the form f(x) = a(x)+b, where a is a linear map
andb∈W.Anaffinesubspaceofavectorspaceisthezerosetofsomeaffine
map:{x:a(x)+b=0}.Itsdimensionisthedimensionofthekernelofthe
linear part of the affine map. The special case of an affine subspace of V
whosedimensionisonelessthanthatofV iscalledanaffine hyperplanein
V.Elementarylinearalgebrashowsthatifn≥k,anyk+1pointsv0,…,v
k
in Rn are contained in some k-dimensional affine subspace (just choose a
linearmapa: Rn →Rn−k whosekernelcontains{v1 −v0,…,v
k
−v0 }and
letb=−a(v0)).Wesaythatk+1pointsareingeneral positioniftheyare
not contained in any (k−1)-dimensional affine subspace, or equivalently if
{v1 −v0,…,v
k
−v0 } are linearly independent.
Given points v0,…,v
k
in general position in Rn, the simplex (plural:
simplices) spanned by them is the set of all points in Rn of the form
(cid:14)k (cid:14)k
t v , where 0≤t ≤1 and t =1, (5.1)
i i i i
i=0 i=0
with the subspace topology. Each of the points v is called a vertex of the
i
simplex. We will sometimes use the notation (cid:22)v0,…,v
k
(cid:23) to denote the
simplex spanned by v0,…,v
k
. The integer k (one less than the number of
vertices)iscalleditsdimension,andak-dimensionalsimplexisoftencalled
a k-simplex. A 0-simplex is a single point, a 1-simplex is a line segment,
a 2-simplex is a (filled-in) triangle, and a 3-simplex is a solid tetrahedron
(Figure 5.1).
For any subset A ⊂ Rn, the convex hull of A is defined to be the inter-
sectionofallconvexsetscontainingA.Itisimmediatethattheconvexhull
is itself a convex set, in fact, the smallest convex set containing A.

---

Euclidean Simplicial Complexes 93
Lemma 5.1. A simplex is the convex hull of its vertices.
Exercise 5.1. Prove Lemma 5.1.
Let σ be a simplex. Each simplex spanned by a nonempty subset of the
vertices is called a face of σ. The faces that are not equal to σ itself are
called its proper faces. The 0-dimensional faces of σ are just its vertices,
and the 1-dimensional faces are called its edges. The (k−1)-dimensional
faces of a k-simplex are sometimes called its boundary faces.
A map f: σ →τ between simplices is called a simplicial map if it is the
restriction of an affine map that takes vertices of σ to vertices of τ. As the
next exercise shows, simplicial maps between a given pair of simplices are
in one-to-one correspondence with maps between their vertices.
Exercise 5.2.
(a) Show that given any map f0 from the set of vertices of σ to the set
of vertices of τ, there is a unique simplicial map f: σ → τ whose
restriction to the vertices of σ is f0.
(b) Showthatanytwok-simplicesarehomeomorphicbyasimplicialhome-
omorphism.
(c) Show that every k-simplex is homeomorphic to Bk. [Hint: Work with
a particular simplex in Rk and use Proposition 4.26.]
It follows from part (c) of the preceding exercise that a k-simplex is a
k-dimensional manifold with boundary. Thus we define the boundary of a
simplex to be the union of its boundary faces (which is the same as the
union of all of its proper faces), and its interior to be the simplex minus
its boundary. The interior of a k-simplex(cid:15)is sometimes called an open k-
simplex;itisthesetofpointsoftheform t
i
v
i
where{v0,…,v
k
}arethe
vertices of σ and none of the coefficients t are zero. For example, if σ is a
i
0-simplex, Intσ = σ, and if σ is a 1-simplex, Intσ is σ minus its vertices.
Note that an open simplex is generally not an open subset of Rn, and the
interiorandboundaryofσ asasimplexmaynotbeequaltoitstopological
interior and boundary as a subset of Rn.
A Euclidean simplicial complex is a collection K of simplices in some
Euclidean space Rn satisfying the following conditions:
(i) If σ ∈K, then every face of σ is in K.
(ii) The intersection of any two simplices in K is either empty or a face
of each.
(iii) Local Finiteness: Every point in a simplex of K has a neighbor-
hood that intersects at most finitely many simplices of K.

---

94 5. Simplicial Complexes
FIGURE 5.2. A complex in R2. FIGURE 5.3. Not a complex.
ThedimensionofK isdefinedtobethemaximumdimensionofanysimplex
in K (which is well-defined, since simplices in Rn have dimension at most
n). Figure 5.2 shows an example of a 2-dimensional simplicial complex in
R2. The set of simplices shown in Figure 5.3 is not a simplicial complex,
because the intersection condition is violated.
Given a Euclidean complex K, the union of all the simplices in K, with
thesubspacetopologyinheritedfromRn,isatopologicalspacedenotedby
|K| and called the (Euclidean) polyhedron of K.
Many of the spaces we have seen so far are homeomorphic to Euclidean
polyhedra. Here are some simple examples.
Example 5.2 (Euclidean Polyhedra).
(a) Any n-simplex together with its faces is a simplicial complex whose
polyhedron is homeomorphic to Bn.
(b) The proper faces of an n-simplex constitute an (n−1)-dimensional
complex whose polyhedron is homeomorphic to Sn−1.
(c) The set of all unit-length intervals [n,n+1]⊂R for n∈Z, together
with their endpoints, is a simplicial complex whose polyhedron is R.
(d) For any integer m ≥ 3, let P be a regular m-sided polygon in the
m
plane. The set of edges and vertices of P is a simplicial complex
m
whose polyhedron is homeomorphic to S1.
Example 5.3. Thesetofclosedlinesegmentsintheplanefromtheorigin
to the points (1,1/n) for n ∈ N, together with their vertices (Figure 5.3),
is not a simplicial complex, because the local finiteness condition fails at
the origin.
Exercise 5.3. Prove the claims made in the two preceding examples.
You might wonder why we should focus on building spaces out of sim-
plices, and not out of cubes or some other sort of geometric object. The
simple answer is that simplicial complexes are the most general: It is not
hardtoshowthatalocallyfinite“polyhedralcomplex”(underanyreason-
able definition) can be subdivided to form a simplicial complex.

---

Euclidean Simplicial Complexes 95
FIGURE 5.4. Failure of local finiteness.
Let K be a Euclidean simplicial complex. Any subset K(cid:5) ⊂ K that is
itself a simplicial complex is called a subcomplex of K. It is clear that the
only condition that needs to be checked is that the faces of each simplex
in K(cid:5) are in K(cid:5). In particular, for any nonnegative integer k, the subset
K(k) ⊂K consisting of all simplices of dimension less than or equal to k is
a subcomplex, called the k-skeleton of K.
Let K and L be two Euclidean simplicial complexes. A continuous map
f: |K| → |L| whose restriction to each simplex of K is a simplicial map
to a simplex of L is called a simplicial map, and is denoted by f: K →L.
The restriction of f to K(0) is called the vertex map of f.
Exercise 5.4. Let K and L be Euclidean simplicial complexes.
(a) Let f0: K(0) → L(0) be any map with the property that whenever
{v0,…,vk }aretheverticesofasimplexofK,{f0(v0),…,f0(vk)}are
the vertices of a simplex of L (possibly with repetitions). Show that
there is a unique simplicial map f: K →L whose vertex map is f0.
(b) Now let f0 be as in (a), and assume in addition that f0 is bijective
and {v0,…,vk } are the vertices of a simplex of K if and only if
{f0(v0),…,f0(vk)} are the vertices of a simplex of L. Show that |K|
and |L| are homeomorphic by a simplicial map.
All the considerations of this section carry over without change if we
replace Rn by an arbitrary finite-dimensional vector space V. We give V
the metric topology induced by any norm; Problem 4-8 shows that the
resulting topology is independent of the norm. The only properties of Rn
that we use are its vector space structure and its topology, and since any
choice of basis gives a linear homeomorphism of V with Rn, all the results
of this section are true with Rn replaced by V. We will use this slightly
more general setting in the next section.

---

96 5. Simplicial Complexes
Abstract Simplicial Complexes
Just as it is too restrictive to define manifolds to be subsets of Euclidean
spaces,Euclideansimplicialcomplexesarenotsufficientlygeneralformany
important applications. In this section we will define a more general kind
of simplicial complex. The key idea is already implicit in Exercise 5.4(b),
whichsaysthatasimplicialcomplexiscompletelydetermined,uptosimpli-
cialhomeomorphism,byknowledgeofwhichsetsofverticesspansimplices.
Motivated by this observation, we define an abstract simplicial complex
to be a collection K of nonempty finite sets called (abstract) simplices,
subject only to one condition: If σ ∈ K, then every nonempty subset of σ
is in K. Any element of a simplex σ ∈ K is called a vertex of σ, and any
nonemptysubsetofσiscalledafaceofσ.(Wemakenodistinctionbetween
avertexv andthecorrespondingface{v}.)Todistinguishthesimpliceswe
defined earlier (as convex subsets of some Euclidean space) from abstract
simplices in this sense, we will sometimes refer to the former as Euclidean
simplices.
Thedimensionofanabstractsimplexconsistingofk+1verticesisdefined
to be k. The dimension of K is the maximum dimension of any simplex in
K, if it exists; if there are simplices of arbitrarily high dimensions, K is
said to be infinite-dimensional. We say that K is a finite complex if K is
a finite set, and locally finite if every vertex belongs to only finitely many
simplices.
AsubsetofKthatisitselfasimplicialcomplex(i.e.,thatcontainsallthe
faces of each of its simplices) is called a subcomplex of K. The set K(k) of
all simplices of dimension at most k is a k-dimensional subcomplex called
the k-skeleton of K.
Given two abstract complexes K,L, a map f: K→L is called a simpli-
cial map if it is of the form f({v0,…,v
k
})={f0(v0),…,f0(v
k
)} for some
map f0: K(0) → L(0), called the vertex map of f (which must have the
property that {f(v0),…,f(v
k
)} ∈ L whenever {v0,…,v
k
} ∈ K). A sim-
plicial map f is called an isomorphism if f0 is a bijection and {v0,…,v
k
}
is a simplex of K if and only if {f0(v0),…,f0(v
k
)} is a simplex of L.
One way of constructing an abstract simplicial complex, as you have
probably already guessed, is the following. Given a Euclidean simplicial
complex K, let K denote the set of all those finite subsets {v0,…,v
k
} ⊂
K(0) that consist of the vertices of some simplex of K. It is immediate
that K is an abstract simplicial complex, called the vertex scheme of K. It
is an immediate consequence of Exercise 5.4(b) that two Euclidean com-
plexes are simplicially homeomorphic if and only if their vertex schemes
are isomorphic.
Exercise 5.5. Show that every finite abstract complex is the vertex
scheme of a Euclidean simplicial complex. [Hint: Use basis vectors ei =
(0,…,1,…,0) as vertices.]

---

Abstract Simplicial Complexes 97
Not all abstract simplicial complexes are vertex schemes of Euclidean
complexes, however. Such an abstract complex must obviously be finite-
dimensionalandlocallyfinite.Moreover,sincethelocalfinitenesscondition
forces the vertex set of a Euclidean complex to be a discrete subset of Rn,
its vertex scheme can have only countably many simplices. Problem 5-5
shows that these conditions are also sufficient.
Thetheoryofquotientspacesgivesausefulwayofconstructingtopolog-
ical spaces out of abstract complexes without these restrictions. The first
step is to construct a canonical Euclidean k-simplex for each abstract k-
simplex. Using equation (5.1) as(cid:15)a guide, we wish to think of our simplex
as “a set of points of the form t v .” The trouble is that the vertices
i i
v of an abstract simplex are just abstract objects and not points in some
i
Euclideanspace,sothisexpressionnolongermakesliteralsenseasavector
sum. Instead, we consider such a sum as a “formal linear combination” of
theverticesv .(Theword“formal”isusedheretoindicatethattheexpres-
i
sion has the form of a linear combination, but may not actually represent
addition of vectors in a vector space.) To make this precise, we introduce
a bit of algebraic terminology.
Given a set S, we wish to define a vector space whose elements we can
think of as “formal linear combinations” of the elements of S. The main
property of such a linear combination is that it is completely determined
bythecoefficienttattachedtoeachv ∈S.Thusweareledtothefollowing
definition:AformallinearcombinationofelementsofSisafunctiont: S →
R such that t(v)=0 for all but finitely many v ∈S. Under the operations
of pointwise addition and multiplication by constants, the set of all such
functionsisavectorspace,denotedbyR(cid:22)S(cid:23)andcalledthefreevectorspace
on S.
Any element t∈R(cid:22)S(cid:23) can be represented symbolically as
(cid:14)k
t= t v , (5.2)
i i
i=0
where v are the (finitely many) elements of S for which t(v) (cid:14)= 0, and
i
t = t(v ). To be a bit more precise, each v ∈ S determines in a natural
i i
way a function from S to R, also denoted by v for simplicity, given by
(cid:16)
1, w =v,
v(w)=
0, w (cid:14)=v.
Itiseasytocheckthateacht∈R(cid:22)S(cid:23)hasauniqueexpressionasafinitelin-
earcombinationofthesefunctions;thisistheappropriatewaytointerpret
(5.2).
Now consider any abstract simplex {v0,…,v
k
}. We define its geometric
realization to be the k-simplex (cid:22)v0,…,v
k
(cid:23) in the finite-dimensional vector
space R(cid:22)v0,…,v
k
(cid:23). With the topology on R(cid:22)v0,…,v
k
(cid:23) induced by any
norm,thisgeometricrealizationishomeomorphictoaEuclideank-simplex.

---

98 5. Simplicial Complexes
π
FIGURE 5.5. The quotient map defining the topology of |K|.
Since each abstract simplex determines its geometric realization and
vice versa, we will sometimes use the term “simplex” and the notation
(cid:22)v0,…,v
k
(cid:23) interchangeably to refer either to an abstract simplex or to
its geometric realization. When we need to distinguish between the two,
we will use the notation |σ| for the geometric realization of σ. As in the
Euclidean case, the open simplex Int|σ| is the subset of |σ| consisting of
points all of whose coefficients t are nonzero.
i
ForanyabstractsimplicialcomplexK,let|K|denotethesetofallformal
(cid:15)
linear combinations of the form k
i=0
t
i
v
i
with (cid:22)v (cid:15)0,…,v
k
(cid:23) a simplex of K
and with coefficients satisfying 0 ≤ t ≤ 1 and k t = 1. This can be
i i=0 i
thought of abstractly as a subset of the free vector space R(cid:22)K(0)(cid:23) on the
vertex set of K. More concretely, |K| is just the union of all the geometric
realizations of the simplices of K, with points in two simplices identified
whenevertheyhavethesameexpressionasli(cid:6)nearcombinationsofvertices.
Wetopologize|K|inthefollowingway.Let |σ|bethedisjointunion
σ∈K
ofthegeometricrealizationsofallthesimplicesofK,withthedisjo(cid:6)intunion
topology as in Problem 2-9 (this just means that a set is open in |σ|
σ∈K
if and only if its intersection with each |σ| is open in |σ|), and let
(cid:17)
π: |σ|→|K|
σ∈K
be the natural map that sends each simplex |σ| to itself (Figure 5.5). We
give|K|thequotienttopologywithrespecttoπ.Unwindingthedefinitions,

---

Abstract Simplicial Complexes 99
thisisthesameassayingthatasubsetof|K|isopen(orclosed)ifandonly
ifitsintersectionwitheachsimplexisopen(orclosed).Withthistopology,
|K| is called the geometric realization of K.
Thiswayofcharacterizingatopologyturnsouttobeofgreatimportance,
soithasaname.Givenanycollection{S α } α∈A ofsubspacesofatopological
space X whose union is X, the topology of X is said to be coherent with
the subspaces S if a set is open in X if and only if its intersection with
α
each S is open in S . It is easy to check that this is equivalent to saying
α α
thatasetisclosedinX ifandonlyifitsintersectionwitheachS isclosed
α
in S .
α
Lemma 5.4. LetKbeanabstractsimplicialcomplexand|K|itsgeometric
realization.
(a) Each simplex |σ| is a closed, compact subset of |K|.
(b) If dimK = n, then each open n-simplex Int|σ| is an open subset of
|K|.
(c) The topology of |K| is the unique topology coherent with the collection
of subspaces {|σ|:σ ∈K}.
(d) A map F: |K|→|L| is continuous if and only if its restriction to |σ|
is continuous for each σ ∈K.
Exercise 5.6. Prove Lemma 5.4.
Any simplicial map f: K → L between abstract complexes induces in
an obvious way a map |f|: |K|→|L|. (On each simplex |σ|, |f| is just the
Euclidean simplicial map determined by the vertex map of f.) Since the
restriction of |f| to each simplex is continuous, |f| is a continuous map.
Lemma 5.5. Let K, L, and M be simplicial complexes.
(a) If Id: K→KdenotestheidentitymapofK,then|Id|istheidentity
map of |K|.
(b) Iff: K→Landg: L→Maresimplicialmaps,then|g◦f|=|g|◦|f|.
(c) Isomorphic complexes have homeomorphic geometric realizations.
Exercise 5.7. Prove Lemma 5.5.
Lemma 5.6. If K is the vertex scheme of a Euclidean simplicial complex
K, then the geometric realization of K is homeomorphic to |K|.
Proof. Recall that an abstract simplex σ ∈ K is just the set of vertices of
some Euclidean simplex σ(cid:7) ∈K. Let π(cid:5) denote the natural map
(cid:17)
π(cid:5): |σ|→|K|,
σ∈K

---

100 5. Simplicial Complexes
which, restricted to each simplex |σ|, is the obvious simplicial homeomor-
phism |σ|→σ(cid:7). This map makes the same identifications as the map π we
used above to define the topology of |K|. If we can show that π(cid:5) is a quo-
tient map, the lemma will follow from the uniqueness of quotient spaces.
To show that it is a quotient map is the same as showing that |K| has the
topology coherent with its simplices.
To verify this, let G ⊂ |K| be an arbitrary subset. If G is closed, then
clearly its intersection with any simplex is closed, because it is an inter-
section of closed sets. Conversely, suppose the intersection of G with each
simplex is closed. If x ∈ |K| is any limit point of G, by local finiteness x
has a neighborhood U that intersects only finitely many simplices. Thus
G∩U is the union of finitely many closed subsets of U and hence closed in
U.Thisimpliesx∈G,soGisclosedin|K|.(Thisisthereasonweinsisted
on local finiteness in the definition of Euclidean simplicial complexes.)
Any topological space that is homeomorphic to the geometric realiza-
tion of some simplicial complex is called a polyhedron. A particular such
homeomorphismiscalledatriangulationofX.Anyspacethatadmitsatri-
angulation (i.e., any polyhedron) is said to be triangulable. Sometimes one
canobtainabetterunderstandingofthetopologyofanunknownspaceby
firstshowingthatitistriangulable;thiswillbeourapproach,forexample,
to the classification of 1-dimensional and 2-dimensional manifolds.
Example 5.7. The following abstract complexes are isomorphic to the
vertex schemes of the Euclidean complexes of Example 5.2, and therefore
yield triangulations of the indicated spaces.
(a) Thesetofallnonemptysubsetsof{0,1,2,…,n}isanabstractcom-
plex whose geometric realization is homeomorphic to Bn.
(b) Thesetofallpropernonemptysubsetsof{0,1,2,…,n}isanabstract
complex whose geometric realization is homeomorphic to Sn−1.
(c) Let K ∞ be the abstract complex consisting of 0-simplices {{n}:n∈
Z} and 1-simplices {{n,n+1} : n ∈ Z}. Its geometric realization is
homeomorphic to R.
(d) For any integer m ≥ 3, let K be the abstract complex whose
m
0-simplices are {{1},{2},…,{m}}, and whose 1-simplices are
{{1,2},{2,3},…,{m − 1,m},{m,1}}. Its geometric realization is
homeomorphic to S1.
Example 5.8 (Graphs). We define a graph to be a 1-dimensional poly-
hedron with a given triangulation. (For some applications, it is useful to
have a more general definition, allowing two edges to share more than one
vertex,oroneedgetobeginandendatthesamevertex;butthiswillsuffice
for our purposes. The kind of graph we have defined is sometimes called a

---

Abstract Simplicial Complexes 101
simplegraphtodistinguishitfromothermoregeneraltypes.Notethatthis
use of the word graph has no relation to the graph of a function as defined
in Chapter 3.) A subgraph of a graph is the polyhedron of a 1-dimensional
subcomplex.Agraphissaidtobefiniteifitsassociatedsimplicialcomplex
is finite.
We will illustrate the utility of simplicial complexes by showing how
a topological property of polyhedra—connectedness—can be detected by
purely combinatorial means. Let K be a simplicial complex. An edge path
inKisafiniteorinfinitesequenceofverticessuchthatanytwoconsecutive
vertices span an edge. An edge path is said to bereduced if in addition any
three consecutive vertices are all distinct. (The idea is that a reduced edge
pathcontainsno“dead-endexcursions”likev,w,v.)WesaythatKisedge
path connected if any two vertices can be joined by a finite edge path.
Proposition 5.9. Let K be a simplicial complex. Then |K| is connected if
and only if K is edge path connected, in which case any two vertices can be
joined by a reduced edge path.
Proof. SupposeKisedgepathconnected.Becausesimplicesareconnected,
any two vertices that span an edge lie in the same component of |K|. It
follows easily by induction that any two vertices joined by a finite edge
path lie in the same component. Thus if K is edge path connected, all the
verticeslieinthesamecomponentV0 of|K|.Anypointx∈|K|liesinsome
simplex |σ|, and since |σ| contains at least one vertex in common with V0,
it must be contained in V0. This shows that V0 =|K|, so |K| is connected.
Conversely, suppose |K| is connected. Choose a vertex v ∈ K, and let C
denote the subcomplex of K consisting of all vertices that are traversed in
edge paths starting from v, together with all the simplices of K they span.
If σ is a simplex of K that has a vertex w ∈ C, then every vertex w(cid:5) of σ
must lie in C, because we can form an edge path from v to w(cid:5) by starting
with an edge path to w and then appending w(cid:5) (since (cid:22)w,w(cid:5)(cid:23) is an edge
of σ). Thus σ ∈ C as well. It follows that |C| is both open and closed in
|K|,becauseitsintersectionwitheachsimplexiseitheremptyortheentire
simplex. Thus C=K, which shows that K is edge path connected.
Now suppose K is edge path connected. Given any two vertices v,v(cid:5) ∈
K, there is an edge path (v,…,v(cid:5)) connecting them. If this edge path is
not reduced, it must have three consecutive vertices of the form w,w(cid:5),w
for some pair of vertices w,w(cid:5) that span an edge. It is easy to see that
the sequence obtained by replacing these three vertices with the single
vertexw isstillanedgepathconnectingthesametwovertices.Repeatedly
shorteningtheedgepathinthiswayuntilitisimpossibletoshortenitany
more, we obtain a reduced edge path joining the same two vertices.

---

102 5. Simplicial Complexes
Triangulation Theorems
In the next chapter we will begin to study the problem of classifying man-
ifolds up to homeomorphism. Our approach to classifying 1-manifolds and
2-manifolds will be to start with a triangulated manifold and study the
combinatorialpropertiesofthetriangulation.Forthiswewillneedtoknow
that all manifolds of dimensions 1 and 2 are triangulable.
Theorem 5.10 (Triangulation Theorem for 1-Manifolds). Every1-
manifold can be triangulated by a 1-dimensional simplicial complex.
Proof. We begin by showing that there exists a sequence of compact sub-
spaces G ⊂ M, n = 1,2,…, whose union is M, satisfying the following
n
conditions:
(i) Each G is a finite graph.
n
(ii) For each n, G
n
is a subgraph of G n+1.
(iii) For each n there exists m>n such that G ⊂IntG .
n m
By Lemma 4.31, M admits a countable cover {B } by regular Euclidean
i
balls. From the definition of regular balls, it is evident that the closure of
eachregularballishomeomorphictoa1-simplexwhosetopologicalinterior
in M is equal to its interior as a simplex.
Begin by letting G1 be the graph consisting of the single 1-simplex B1
and its vertices. Now let n > 1, and assume by induction that we have
found finite graphs G1 ⊂ G2 ⊂ ··· ⊂ G
n
satisfying (i) and (ii) with G
n
=
B1 ∪···∪ B
n
. Consider the next 1-simplex B n+1. Some of the vertices
of G n may lie in B n+1 (the interior of B n+1); the ones that do define a
subdivisionofB n+1 intoafinitegraphS,withthepropertythatnovertex
of G lies in the interior of any edge of S.
n
For each of the edges e ⊂ S, we will prove the following claim: Either e
intersectseachoftheedgesofG onlyatvertices,oreisentirelycontained
n
in one of the edges of G . To prove this, suppose e has an interior point
n
that lies in some edge e(cid:5) ⊂G (Figure 5.6). By the remark above, it must
n
be an interior point of e(cid:5) as well.
NotethatInte∩Inte(cid:5) isopeninInte.Ontheotherhand,e(cid:5) isacompact
subset of the Hausdorff space M, so it is closed in M, and therefore Inte∩
Inte(cid:5) =Inte∩e(cid:5) isclosedinInte.Byconnectedness,therefore,Inte∩Inte(cid:5)
isallofInte.Inotherwords,Inte⊂Inte(cid:5),whichimpliese⊂e(cid:5) andproves
the claim.
Now simply throw away those edges of S that are contained in G , and
n
redefine S to be the graph consisting of the remaining edges and their
vertices. Let G n+1 =G n ∪S. We wish to show that G n+1 is a finite graph
containing G as a subgraph. The edges of S intersect each of the edges
n
of G only at vertices; but it may happen that both vertices of some edge
n

---

Triangulation Theorems 103
G
n
e(cid:5)
e
S
FIGURE 5.6. Proof that e⊂e(cid:3).
e in S intersect a single edge e(cid:5) in G . If so, simply subdivide e into two
n
edges by adding a new vertex in its interior. With this modification, each
of the edges of S intersects each edge of G at most in a single vertex.
n
Since G n+1 has only finitely many simplices, its topology is coherent
with the simplices by Problem 5-1. Thus the foregoing argument proves
that G n+1 is a finite graph whose polyhedron is B1 ∪···∪B n+1 and that
containsG asasubgraph.Continuingbyinduction,weobtainanincreas-
n
ing sequence {G : n = 1,2,…} of graphs such that every point of M is
n
contained in G for some n. Since the interiors of the Euclidean balls B
n i
cover M, for each n there is some m>n such that the compact set G is
n
covered by B1 ∪···∪B
m
, and therefore G
n
⊂IntG
m
. This completes the
induction.
Let K be the abstract simplicial complex whose 0-skeleton is the union
of the 0-skeletons of G for all n, and whose 1-simplices are the pairs
n
{v,v(cid:5)} that span an edge in some G . There is an obvious bijective map
n
|K| → M, defined by choosing a homeomorphism from each 1-simplex of
|K| onto the corresponding edge in M. To see that this map is a homeo-
morphism, we need only show that M has the topology coherent with the
simplices. Clearly, any set that is closed in M has closed intersection with
eachsimplex,becausethesimpliceshavethesubspacetopology.Conversely,
suppose K ⊂M is a subset whose intersection with each simplex is closed.
If x ∈ M is a limit point of K, choose n large enough that x ∈ IntG .
n
SincetheintersectionofK witheachofthe(finitelymany)simplicesofG
n
isclosedinG ,itfollowsthatK∩IntG isclosedinIntG .Inparticular,
n n n
x∈K, which proves that K is closed in M and thus the topology of M is
coherent with the simplices.
For use in the next chapter, we will need the following property of tri-
angulated 1-manifolds.
Proposition 5.11. If K is a simplicial complex whose geometric realiza-
tion is a 1-manifold, each vertex of K lies on exactly two edges.

---

104 5. Simplicial Complexes
Proof. Let v be any vertex, and let V be the union of {v} together with
the interiors of all the edges that have v as a vertex. Since the intersection
of V with each simplex is open in the simplex, V is open in |K|.
Because|K|isa1-manifold,v hasaneighborhoodU ⊂V homeomorphic
to an open interval. It follows that U (cid:3){v} has exactly two components.
Foreachedgeecontainingv,Inte∩(U(cid:3){v})isanopensubsetofU(cid:3){v}.
These sets are disjoint (because all the edges have disjoint interiors), and
nonempty(because∩U isnonemptyandopenineandthusmustcontain
some interior points of e). Therefore, if v lies on more than two edges, we
have a separation of U (cid:3){v} into more than two nonempty disjoint open
subsets,contradictingthefactthatithasonlytwocomponents.Thisshows
that each vertex lies on at most two edges.
On the other hand, if some vertex v lies on only one edge e, the con-
struction above shows that v has a Euclidean neighborhood U contained
entirely in e. This means that v has a neighborhood Y ⊂ U such that
Y (cid:3){v} is connected—just take Y to be the image of [0,ε) under some
homeomorphism ϕ: [0,1] → e taking 0 to v. But any Euclidean neighbor-
hood minus a point is disconnected by Problem 4-1(a), so there can be no
such vertex.
We turn our attention next to 2-manifolds. The following theorem was
proved by Tibor Rad´o [Rad25] in 1925.
Theorem 5.12 (Triangulation Theorem for Surfaces). Every 2-
manifold admits a triangulation by a 2-dimensional simplicial complex, in
which each edge lies on exactly two 2-simplices.
Sketch of proof. The basic approach is analogous to the proof of triangu-
lability of 1-manifolds: Cover the manifold with countably many regular
disks, and inductively show that each successive disk can be triangulated
in a way that is compatible with the triangulations that have already been
defined,sothatthemanifoldisultimatelywrittenasanincreasingunionof
polyhedra. In the case of surfaces, however, finding a triangulation of each
successivediskthatiscompatiblewiththepreviousonesismuchmoredif-
ficult, primarily because the boundary of the new disk might intersect the
boundaries of the already-defined simplices infinitely many times. Even if
thereareonlyfinitelymanyintersections,showingthattheregionsdefined
by the intersecting curves are homeomorphic to closed disks, and therefore
triangulable, requires a delicate topological result known as the Scho¨nflies
theorem,whichassertsthatanytopologicalembeddingofthecircleintoR2
extends to an embedding of the closed disk. The details of the proof are
long and intricate and would take us too far from our main goals, so we
leave it to the reader to look it up. A readable presentation can be found
in [Moi77].

---

Orientations 105
v1 v2 v3 v4
v4 v5 v6 v1
FIGURE 5.7. The Mo¨bius band.
Finally,althoughwewillnotuseit,wementionthefollowingmorerecent
result, proved by Edwin Moise in 1977 [Moi77].
Theorem 5.13 (Triangulation Theorem for 3-Manifolds). Every
3-manifold is triangulable.
Beyonddimension3,mattersarenotnearlysonice.Ithasrecentlybeen
shown that there are manifolds of dimension 4 that admit no triangula-
tions; and it is still not known whether all manifolds of dimension greater
than 4 can be triangulated. See [Ran96] for a history of the subject of
triangulations and a summary of the current state of the art.
Orientations
The Mo¨bius band is the famous topological space obtained by identifying
two edges of the square I ×I according to the relation (0,t) ∼ (1,1−t)
(Figure 5.7). It is a manifold with boundary (though not a manifold), and
it is triangulable (one triangulation is shown in Figure 5.7). If you have
ever made a paper model (it is best to start with a long, narrow rectangle
instead of a square), you have undoubtedly noticed that it has the curious
property that it is impossible to consistently pick out which is the “front”
side and which is the “back”—you cannot continuously color one side gray
and the other side white.
By using simplicial theory, we can make this notion precise and extend
it to complexes of other dimensions as well. Instead of choosing which side
of each triangle to call the front, we will, in effect, choose which direction
of travel around the vertices to consider “counterclockwise.”
Let σ be an abstract k-simplex. Given any two orderings (v ,…,v )
i0 ik
and (v ,…,v ) of the vertices of σ, there is a permutation s of the set
j0 jk
{0,…,k} such that s(i )=j for p=0,…,k. Define an equivalence rela-
p p
tion on the set of all orderings by saying that two orderings are equivalent
if they differ by an even permutation (see the Appendix). A choice of an
equivalence class of vertex orderings is called an orientation of σ. For ex-
ample, an orientation of a 1-simplex is just a choice of initial and terminal
vertices, which can be indicated schematically by drawing an arrow along

---

106 5. Simplicial Complexes
v3
v2
v1
v0
v0 v0 v1 v1
v2
FIGURE 5.8. Orientations of simplices.
the simplex (see Figure 5.8). An orientation of a 2-simplex is a choice of a
preferred direction of rotation, which can be indicated by a circular arrow;
andanorientationofa3-simplexisachoiceof“handedness”:Thepreferred
hand is the one whose fingers curl around the first three vertices in order
while the thumb points toward the fourth. Since there is only one way to
order a single vertex, by convention an orientation for a 0-simplex is just a
choice of a plus or minus sign.
An oriented simplex is a simplex together with a choice of orientation.
We will write [v0,…,v
k
] for the k-simplex (cid:22)v0,…,v
k
(cid:23) oriented by the
vertex ordering (v0,…,v
k
), and we will let −[v0,…,v
k
] denote the same
simplex with the opposite orientation. Thus, for example, for 1-simplices
and 2-simplices we have
[v,w]=−[w,v],
[v,w,x]=[w,x,v]=[x,v,w]=−[v,x,w]=−[x,w,v]=−[w,v,x].
Any n-simplex in Rn automatically gets an orientation, which we call
the natural orientation, by declaring [v0,…,v
n
] to be oriented if and only
ifdet(v1 −v0,v2 −v0,…,v
n
−v0)>0.Toseethatthisiswell-defined,first
note that the n vectors {v1 −v0,…,v
n
−v0 } are independent precisely
when the vertices {v0,…,v
n
} are in general position. Interchanging two
vertices other than v0 has the same effect as interchanging two rows of
the determinant, which changes its sign. If v0 is interchanged with another
vertex v
i
, the determinant becomes det(v1 −v
i
,…,v0 −v
i
,…,v
n
−v
i
);
multiplyingtheithrowby−1(whichchangesthesignofthedeterminant)
and then adding the ith row to each other row (which leaves the deter-
minant unchanged) transforms the new determinant back to the original
one. Thus a transposition of two vertices always changes the sign of the
determinant, so an arbitrary permutation of the vertices changes the sign
ofthedeterminantifandonlyifitiseven,whichshowsthatthisrulegives
a well-defined orientation. Geometrically, for a 1-simplex in R the natural
orientationisfromthesmallertothelargervertex;fora2-simplexin R2 it

---

Orientations 107
−
+
FIGURE 5.9. Induced orientations of boundary faces.
is the counterclockwise direction of rotation; and for a 3-simplex in R3 it
is the right-handed orientation. (These statements can be taken as mathe-
matical definitions of the terms “counterclockwise” and “right-handed.”)
If σ = [v0,…,v
k
] is an oriented k-simplex, the orientation of σ deter-
mines an orientation on each of its boundary faces (i.e., faces of dimension
k−1), called the induced orientation, by the following rule: The induced
orientation on the face τ
i
= (cid:22)v0,…,v(cid:18)
i
,…,v
k
(cid:23) (where the hat indicates
that v
i
is omitted) is defined to be (−1)i[v0,…,v(cid:18)
i
,…,v
k
]. To check that
thisiswell-defined,weneedtoshowthattheinducedorientationofτ isun-
i
changed if the vertices of σ are subjected to an even permutation. Because
everypermutationcanbewrittenasacompositionoftranspositionsofad-
jacentvertices(seeExerciseA.19intheAppendix),itsufficestoshowthat
the induced orientation is reversed if two adjacent vertices of σ are trans-
posed. This is clear if neither of the vertices is v . If v is transposed with
i i
v i±1, the induced orientation becomes (−1)i±1[v0,…,v i−1,v i+1,…,v
k
],
which is the opposite of what it was originally.
For an oriented 1-simplex [v0,v1], the induced orientation gives a minus
signtotheinitialvertexv0 andaplussigntotheterminalvertexv1 (Figure
5.9). For an oriented 2-simplex [v0,v1,v2], the induced orientations on the
edges are [v1,v2], −[v0,v2] = [v2,v0], and [v0,v1]. Thus the arrow on each
edge points in the preferred direction of rotation.
Now suppose K is an n-dimensional simplicial complex in which every
(n−1)-simplexisafaceofnomorethantwon-simplices.(Itcanbeshown,
though we will not do so, that any triangulated manifold has this form.)
If σ and σ(cid:5) are two n-simplices that share a boundary face τ, we say that
orientations of σ and σ(cid:5) are consistent if they induce opposite orientations
on τ. An orientation of K is a choice of orientation of each n-simplex
in such a way that any two simplices that intersect in an (n−1)-face are
consistentlyoriented.Figure5.10givesschematicindicationsoforientations
of 1-dimensional and 2-dimensional complexes. If a complex K admits an
orientation, it is said to be orientable.
Example 5.14. ThetriangulationoftheMo¨biusbandshowninFigure5.7
isnotorientable.Toseewhy,supposethereexistsanorientation.Reversing
the orientations of all the 2-simplices if necessary, we may assume that
the leftmost triangle is oriented as [v1,v4,v5] (i.e., in the counterclockwise

---

108 5. Simplicial Complexes
FIGURE 5.10. Orientations of simplicial complexes.
direction). Then the consistency condition implies that the next simplex
is oriented as [v1,v5,v2]. Similarly, each of the succeeding simplices must
be oriented in the counterclockwise direction. But then both the leftmost
and the rightmost 2-simplices induce the same orientation [v1,v4] on their
commonedge,whichcontradictstheconsistencycondition.Therefore,there
exists no orientation.
Example 5.15. Letσ =(cid:22)v0,…,v n+1 (cid:23)bean(n+1)-simplexinRn+1,and
let K be the set of proper faces of σ, which is a triangulation of Sn. Give
σ the natural orientation inherited from Rn+1, and give the n-simplices
of K the induced orientation. Each (n−1)-simplex of K is of the form
τ = (cid:22)v0,…,v(cid:18) i ,…,v(cid:18) j ,…,v n+1 (cid:23), and belongs to two n-simplices: the one
oppositev andtheoneoppositev .Itiseasytocheckthattheorientations
i j
induced on τ by these two faces are opposite, because in one case v is
i
removed first and then v , while in the other case the order is reversed.
j
Thus we have produced an orientation of K.
Proposition 5.16. LetK beanyn-dimensionalEuclideancomplexinRn.
The natural orientation of each n-simplex determines an orientation of K.
Proof. First we show that no more than two n-simplices in K can have an
(n−1)-face in common. Let τ be an (n−1)-simplex in K. The vertices
of τ determine a unique affine hyperplane (i.e., (n−1)-dimensional affine
subspace) in Rn, whose complement has exactly two components, which
we call the sides of τ. Because the vertices of σ are in general position, the
additionalvertexofσ thatisnotinτ mustlieononesideofτ ortheother,
and therefore all of σ(cid:3)τ must lie on the same side (since it is connected).
For any x ∈ Intτ and any sufficiently small ε > 0, B (x) (cid:3) τ has two
ε
components, one lying on each side of τ. Any n-simplex that contains τ
must contain exactly one of these components for ε small enough. Thus if
more than two n-simplices contain τ, two of them must contain the same

---

Combinatorial Invariants 109
component of B (x) (cid:3) τ and therefore have interior points in common,
ε
which contradicts the definition of a Euclidean complex.
Now we must show that the natural orientations of any two sim-
plices σ,σ(cid:5) ∈ K that share an (n − 1)-face τ are consistent. Write
τ =(cid:22)v0,…,v n−1 (cid:23), σ =(cid:22)v0,…,v n−1,v n (cid:23), and σ(cid:5) =(cid:22)v0,…,v n−1,v n (cid:5)(cid:23).
The function f(v) = det(v1 −v0,…,v −v0) is an affine function of v
that is zero precisely when v lies in the affine hyperplane determined by
τ, so it must be positive on one side of τ and negative on the other side.
Since the argument above implies that v and v(cid:5) lie on opposite sides
n n
of τ, it follows that det(v1 −v0,…,v
n
(cid:5) −v0) has the opposite sign from
det(v1 − v0,…,v
n
− v0). If the vertices have been ordered so that the
natural orientation of σ is [v0,…,v
n
], then the natural orientation of σ(cid:5)
is −[v0,…,v
n
(cid:5)], and it is immediate that they induce opposite orientations
on τ.
Combinatorial Invariants
Simplicial complexes were invented in the hope that they would enable
topologicalquestionsaboutmanifoldstobereducedtocombinatorialques-
tions about simplicial complexes. To make sense of this, we need a notion
ofequivalenceofcomplexesthatisweakerthansimplicialisomorphismbut
strong enough to imply that they have homeomorphic geometric realiza-
tions, and that can be detected purely from the combinatorial structure of
the abstract complexes.
The most natural way to modify a simplicial complex to obtain another
one with a homeomorphic geometric realization is to “subdivide” the sim-
plices of the original complex into smaller ones. We can then consider two
complexestobeequivalentiftheybothhaveacommonsubdivision.Inthis
section we make this notion precise, and study one important property of
complexes that is preserved by this kind of equivalence. For our purposes,
it is sufficient and simpler to restrict our attention to finite complexes,
although many of the definitions can be extended to the general case.
Let K be a finite Euclidean simplicial complex. A subdivision of K is a
simplicial complex K(cid:5) with the following properties:
- |K(cid:5)|=|K|.
- Each simplex of K(cid:5) is contained in a simplex of K.
- Each simplex of K is a finite union of simplices of K(cid:5).
Some examples of subdivisions are shown in Figure 5.11.
Example 5.17 (Barycentric Subdivision). Aparticularlyusefulkind
of subdivision is obtained in the following way. Let σ = (cid:22)v0,…,v
k
(cid:23) be a

---

110 5. Simplicial Complexes
K K(cid:5)
M M(cid:5)
L L(cid:5) N N(cid:5)
FIGURE 5.11. Subdivisions.
Euclidean k-simplex in Rn. If v is a point not in the k-dimensional affine
subspace determined by σ, we define
v∗σ =(cid:22)v,v0,…,v
k
(cid:23).
This is a (k+1)-simplex, called the cone on σ from v.
Now let K be a finite Euclidean complex. For each k-simplex σ =
(cid:22)v0,…,v
k
(cid:23)∈K, define the barycenter of σ to be the point
(cid:14)k
1
b = v ∈Intσ.
σ k+1 i
i=0
It is the “center of gravity” of the vertices of σ. (The name comes from
Greekbarys,meaning“heavy.”)Forexample,thebarycenterofa1-simplex
is just its midpoint; the barycenter of a vertex v is v itself.
We will define a complex SK, called the barycentric subdivision of K,
whose vertices are the barycenters of all the simplices in K. It is easiest
to define by induction on the dimension of K. If dimK = 0, then we set
SK =K (you cannot subdivide a point!). Assuming that we have defined
SK for all finite complexes of dimension less than n, we define SK for
a complex of dimension n as the union of S(K(n−1)) with the set of all
simplices of the form b ∗τ where σ is an n-simplex of K and τ is any
σ
simplex of S(K(n−1)) contained in a face of σ. It is straightforward to
check that SK is indeed a subdivision of K (see Problem 5-7). Examples
of barycentric subdivisions are pictured in Figure 5.12.
The key fact about barycentric subdivision is that it reduces the sizes of
all the simplices by a uniform ratio, as the following lemma shows.
Lemma 5.18. If σ is a Euclidean k-simplex in Rm, the diameter of each
simplex in the barycentric subdivision of σ is at most k/(k+1) times that
of σ.

---

Combinatorial Invariants 111
K SK S(SK)
FIGURE 5.12. Barycentric subdivisions.
Proof. Note first that for any point x ∈ σ, the maximum of the function
|x − y| for y ∈ σ is achieved when y is a vertex. To see why, let R be
the maximum distance from x to any vertex of σ; since σ is the convex
hull of its vertices and the closed ball B (x) is a convex set containing the
R
vertices, σ ⊂ B (x), which proves the claim. It follows immediately that
R
the diameter of σ is the maximum of the distances between its vertices.
The following computation shows that the distance from the barycenter
b
τ
ofaq-simplexτ =(cid:22)v0,…,v
q
(cid:23)toanyofitsverticesv
j
isatmostq/(q+1)
times the diameter of τ:
(cid:19) (cid:19)
(cid:19)(cid:14)q (cid:19)
(cid:19) 1 (cid:19)
|b −v |=(cid:19) v −v (cid:19)
τ j (cid:19) q+1 i j(cid:19)
(cid:19)i=0 (cid:19)
(cid:19)(cid:14)q (cid:14)q (cid:19)
(cid:19) 1 1 (cid:19)
=(cid:19) v − v (cid:19)
(cid:19) q+1 i q+1 j(cid:19)
i=0 i=0
(cid:14)q
1
≤ |v −v |
q+1 i j
i=0
q
≤ diamτ.
q+1
Now if σ(cid:5) is any face of the barycentric subdivision of σ and w1, w2 are
any two vertices of σ(cid:5), by Problem 5-7 each w is the barycenter of a k -
j j
dimensional face τ
j
of σ, and we may assume that τ1 is a face of τ2. By
the computation above, the distance from w2 to any point of τ2 is at most
k2/(k2+1) times the diameter of τ2. Since w1, in particular, is a point in
τ2, we have
|w1 −w2 |≤
k2
diamτ2 ≤
k
diamσ.
k2+1 k+1

---

112 5. Simplicial Complexes
It follows from the remark at the beginning of the proof that diamσ(cid:5) sat-
isfies the same inequality.
To express subdivisions in terms of the combinatorics of abstract com-
plexes, we will show how to decompose an arbitrary subdivision into a
sequence of subdivisions that are combinatorially simpler. Suppose K(cid:5) is
a subdivision of K. We say that it is an elementary subdivision if K(cid:5) con-
tains precisely one more vertex than K. (For example, the 3-dimensional
complex M(cid:5) in Figure 5.11 is an elementary subdivision ofM, obtained by
adding one vertex in the bottom face of M.)
Suppose we start with a finite Euclidean complex K and choose a k-
simplex σ = (cid:22)v0,…,v
k
(cid:23) ∈ K, choose a point v ∈ Intσ, and replace
each simplex (cid:22)v0,…,v
k
,w1,…,w
m
(cid:23) that has σ as a face (including σ
itself) by the set of all simplices of the form (cid:22)v,v
i1
,…,v
ij
,w1,…,w
m
(cid:23) as
{
ch
v
e
i1
c
,
k
..
th
.,
a
v
t
ij
K
}
(cid:5)
r
i
a
s
n
a
g
n
es
el
o
e
v
m
e
e
r
n
p
t
r
a
o
r
p
y
e
s
r
ub
su
d
b
iv
se
is
t
i
s
on
of
o
{
f
v
K
0,
,
.
a
.
n
.
d
,v
t
k
h
}
a
.
t
T
e
h
v
e
e
n
ry
it
el
i
e
s
m
e
e
a
n
s
t
y
ar
t
y
o
subdivision is of this form. Moreover, if K(cid:5)(cid:5) is any subdivision of K, there
is a finite sequence K = K0,K1,…,K
m
= K(cid:5)(cid:5) of complexes such that
K i+1 is an elementary subdivision of K i . One advantage of working with
elementary subdivisions is that the effect of an elementary subdivision on
the vertex scheme of K is clearly determined solely by the choice of σ, and
soelementarysubdivisionscanbedefinedbytherecipeaboveforarbitrary
abstract complexes as well.
Twofinitesimplicialcomplexesaresaidtobe combinatorially equivalent
if they become isomorphic after finitely many elementary subdivisions. It
was conjectured by Ernst Steinitz and Heinrich Tietze in 1908 that if two
finite simplicial complexes have homeomorphic polyhedra, they are com-
binatorially equivalent; this conjecture became known as the Hauptvermu-
tung (main conjecture) of combinatorial topology. It is now known to be
true for all finite complexes of dimension 2 and for triangulated compact
manifolds of dimension 3, but false in all higher dimensions. (See [Ran96]
for a nice discussion of the history of this problem.) Thus the hope of re-
ducing topological questions about manifolds to combinatorial ones about
simplicial complexes has not been realized. Nonetheless, simplicial theory
hasprovideduswithanumberofextremelyusefulcombinatorialinvariants
thatturnouttohaveimportanttopologicalramifications.Weconcludethis
chapterwithanintroductiontooneofthem,calledtheEulercharacteristic.
The Euler Characteristic
One of the oldest results in global surface theory is Euler’s formula: If
P ⊂ R3 is a compact polyhedral surface that is the boundary of a convex
openset,andP hasF faces,E edges,andV vertices,thenV −E+F =2.
This quantity has a natural generalization to arbitrary finite simplicial
complexes: If K is a finite simplicial complex of dimension n, we define the

---

Combinatorial Invariants 113
Euler characteristic of K, denoted by χ(K), by
(cid:14)n
χ(K)= (−1)kn ,
k
k=0
where n is the number of k-dimensional simplices in K. Although we are
k
not yet in a position to prove Euler’s formula in full generality, we can
at least show that the Euler characteristic of a simplicial complex is a
combinatorial invariant.
Theorem 5.19. If K and L are combinatorially equivalent finite simpli-
cial complexes, then χ(K)=χ(L).
Proof. ItclearlysufficestoprovethattheEulercharacteristicisunchanged
by an elementary subdivision. Let K(cid:5) be an elementary subdivision of K
obtained by adding a vertex v in the k-simplex σ = (cid:22)v0,…,v
k
(cid:23), and let
Δχ=χ(K(cid:5))−χ(K). We must show that Δχ=0.
For each simplex τ = (cid:22)v0,…,v
k
,w1,…,w
m
(cid:23) of K that has σ as a
face, K(cid:5) has one less (k + m)-simplex. In its place, for each j-element
proper subset {v
i1
,…,v
ij
} ⊂ {v0,…,
(cid:12)
v
k
},
(cid:13)
K(cid:5) has a new (j+m)-simplex
(cid:22)v,v
i1
,…,v
ij
,w1,…,w
m
(cid:23). There are k+
j
1 =
j!(
(
k
k
+
+
1
1
−
)!
j)!
such subsets, so
each such τ makes a contribution to Δχ of
(cid:20) (cid:21) (cid:20) (cid:21)
(cid:14)k k(cid:14)+1
k+1 k+1
−(−1)k+m+ (−1)j+m = (−1)j+m.
j j
j=0 j=0
By the binomial theorem, this last sum is the expansion of the polynomial
(−1)m(x+1)k+1 evaluated at x=−1, and therefore is equal to zero.
Note that we are not claiming yet that the Euler characteristic is a
topologicalinvariant,becausetwotriangulationsofthesamecompactspace
are not necessarily combinatorially equivalent. In fact, it is a topological
invariant. For compact surfaces, this will follow from the classification of
surfaces,whichwewillcompleteinChapter10.Formoregeneralsimplicial
complexes, the proof will require techniques of homology theory, which we
will develop in Chapter 13.

---

114 5. Simplicial Complexes
Problems
5-1. Suppose X is a topological space, and G1,…,G
k
are finitely many
closed subspaces of X whose union is X. Show that the topology of
X iscoherentwiththesesubspaces.Explainwhatthishastodowith
the gluing lemma (Lemma 3.8).
5-2. Let v be a vertex of the simplicial complex K, and let Stv (the open
starofv)betheunionoftheopensimplicesIntσ asσ rangesoverall
simplices that have v as a vertex. Show that Stv is a neighborhood
of v in |K|, and the collection of open stars of all the vertices is an
open cover of |K|.
5-3. ShowthateverypolyhedronisHausdorffandlocallypathconnected.
5-4. LetKbeanabstractsimplicialcomplex.Showthat|K|iscompactif
and only if K is finite, and locally compact if and only if K is locally
finite.
5-5. Show that an abstract simplicial complex is the vertex scheme of
a Euclidean complex if and only if it is finite-dimensional, locally
finite, and countable. [Hint: If the complex has dimension n, let the
vertices be the points v = (k,k2,k3,…,k2n+1) ∈ R2n+1. Use the
k
fundamentaltheoremofalgebratoshowthatno2n+2verticesliein
aproperaffinesubspace,soany2n+2orfewerverticesareingeneral
position. If two simplices σ, τ with vertices in this set intersect, let
σ0, τ0 be the smallest face of each containing an intersection point,
and consider the set consisting of all the vertices of σ0 and τ0. (This
proof is from [Sti93].)]
5-6. DefineanabstractsimplicialcomplexKtobethefollowingcollection
of abstract 2-simplices together with all of their faces:
{{a,b,e},{b,e,f},{b,c,f},{c,f,g},{a,c,g},{a,e,g},
{e,f,h},{f,h,j},{f,g,j},{g,j,k},{e,g,k},{e,h,k},
{a,h,j},{a,b,j},{b,j,k},{b,c,k},{c,h,k},{a,c,h}}.
Show that the geometric realization of K is homeomorphic to the
torus. [Hint: Look at Figure 5.13.]
5-7. IfK isafiniteEuclideansimplicialcomplex,showthatitsbarycentric
subdivisionSK isinfactasubdivisionofK,andthatthesimplicesof
SK are those of the form (cid:22)b ,…,b (cid:23) in which each σ is a simplex
σ0 σk j
in K and σ j is a face of σ j+1 for j =0,…,k−1.
5-8. LetKbeafinitecomplex.Giveanexplicitalgorithmforobtainingthe
barycentricsubdivisionofKasasequenceofelementarysubdivisions.

---

Problems 115
a b c a
e f g e
h j k h
a b c a
FIGURE 5.13. Triangulation of the torus.
5-9. Let K be the 1-dimensional abstract complex whose vertices are the
nonnegative integers and whose 1-simplices are {(cid:22)0,n(cid:23):n∈N}, and
let S be the subspace of R2 obtained by taking the union of all the
line segments in Example 5.3. Define a map F: |K| → S by sending
0 to the origin, sending each n>0 to the point (1,1/n), and sending
each 1-simplex (cid:22)0,n(cid:23) linearly onto the corresponding line segment.
Show that F is continuous and bijective but not a homeomorphism.
5-10. SupposeKisanysimplicialcomplexwhosegeometricrealizationisa
1-manifold. Show that K is 1-dimensional.
5-11. Show that every triangulated 1-manifold is orientable.
5-12. Showthatorientabilityisacombinatorialinvariantoffinitesimplicial
complexes. [Hint: It suffices to prove that if K is a finite Euclidean
complex and K(cid:5) is a subdivision of K, then an orientation of either
K or K(cid:5) determines an orientation of the other. Show that if σ is an
oriented Euclidean n-simplex and σ(cid:5) is an n-simplex in some subdi-
vision of σ, there is a unique orientation of σ(cid:5) such that any affine
embedding σ → Rn that determines the given orientation of σ also
determines the given orientation of σ(cid:5).]

---

6
Curves and Surfaces
In this chapter we undertake a detailed study of curves (1-manifolds) and
surfaces(2-manifolds).Thesearethemanifoldsthataremostfamiliarfrom
our everyday experience, and about which the most is known mathemat-
ically. They are thus excellent prototypes for the study of manifolds in
higher dimensions.
We begin by proving the classification theorem for 1-manifolds, which
says that every connected 1-manifold is homeomorphic to S1 or R. Using
the triangulation theorem for 1-manifolds proved in Chapter 5, this is a
simple exercise in the combinatorics of graphs.
We then proceed to a general discussion of 2-manifolds and a detailed
examination of the basic examples of compact surfaces: the sphere, the
torus, and the projective plane. Next we show how to form other compact
surfaces by the technique of connected sums, a way of patching together
simpler surfaces to form more complicated ones. To unify these results, we
introducethenotionofpolygonalpresentationsofsurfaces,whichgeneralize
simplicial complexes by representing surfaces as a collection of polygons
(not necessarily triangles) with edges identified in pairs.
Thecentralpartofthechapterpresentsthemainpartoftheclassification
theorem for compact surfaces, which says that every compact, connected
surface is homeomorphic to a sphere, a connected sum of tori, or a con-
nected sum of projective planes. Again, the triangulation theorem reduces
the problem to one of showing that every polygonal presentation can be
reduced to a standard presentation of one of the model surfaces.

---

118 6. Curves and Surfaces
In the last section we revisit orientations and the Euler characteristic,
introduced in the last chapter for simplicial complexes, and reinterpret
them in the context of polygonal surface presentations.
Classification of Curves
Our first goal in this chapter is to prove that up to homeomorphism, the
onlyconnected1-manifoldsarethelineandthecircle.(Ofcourse,thisclas-
sifies the disconnected ones too, because it implies that each component of
adisconnected1-manifoldisalineoracircle,soevery1-manifoldishome-
omorphic to a countable disjoint union of lines and/or circles.) You can
think of this classification theorem as a warm-up for the more complicated
classification of surfaces to follow; but it is also quite important in its own
right.
Theorem 6.1 (Classification of 1-Manifolds). A connected 1-
manifold is homeomorphic to S1 if it is compact and to R if it is
not.
Proof. Bythetriangulationtheorem(Theorem5.10)andProposition5.11,
M is homeomorphic to a graph in which every vertex lies on exactly two
edges. Let K denote the abstract simplicial complex associated with this
graph. We will show that K is isomorphic either to one of the complexes
K of Example 5.7(d) (the vertex scheme of a regular m-gon, whose poly-
m
hedron is homeomorphic to S1) or to the complex K ∞ of Example 5.7(c)
(whose polyhedron is homeomorphic to R). Since isomorphic complexes
have homeomorphic polyhedra, this suffices to prove the theorem.
ThefirststepistoshowthateveryvertexinM iscontainedinareduced
edge path {v : n ∈ Z} that extends indefinitely in both directions. Start
n
withanyvertexv0.Byassumptionv0 liesontwoedges,sowecanlabelthe
other vertices of those edges arbitrarily as v1 and v−1. Now by induction
define v n+1 for each n ≥ 1 to be the unique vertex other than v n−1 such
that v n and v n+1 span an edge. Similarly, we define v−n by induction on
n.
Let U be the union of all the edges (cid:22)v n ,v n+1 (cid:23) ⊂ M for v n in the edge
path. The set U is closed in M (because its intersection with each sim-
plex is closed and M has the coherent topology), and open (because the
edges minus their vertices are open, and each vertex has a neighborhood
intersecting only two edges, both of which must be in U). Thus U =M.
Now we distinguish two cases.
Case I: v (cid:14)=v for any n(cid:14)=k. In this case, the correspondence sending
n k
n(cid:10)→v n is easily seen to give an isomorphism between K ∞ and K, so M is
homeomorphic to R.

---

Surfaces 119
v i+m+1
v i+1
v
v i+m
i
v i+m−1
FIGURE 6.1. Periodic edge path.
Case II: v n = v n+m for some n ∈ Z and some m > 0. We may assume
that m and n have been chosen so that m is the least positive integer with
this property. (Note that m ≥ 3 because the edge path is reduced.) We
will show by induction that the edge path is periodic, in the sense that
v i = v i+m for every i. By hypothesis this is true for i = n. If it is true for
some i≥n, we argue as follows. The two vertices v i+m−1 and v i+m+1 are
the only vertices that are connected to v i+m by edges (Figure 6.1). Since
v i =v i+m ,thevertexv i+1 alsoisconnectedbyanedgetov i+m ,soitmust
beequaltoeitherv i+m−1 orv i+m+1.Byminimalityofmitcannotbeequal
tov i+m−1,sov i+1 =v i+m+1,completingtheinductionfori≥n.Asimilar
induction takes care of i≤n.
Now let K be the complex of Example 5.7(d), and define a map
m
f: K(0) → K(0) by f(n) = v for n = 1,…,m. Again, it is straightfor-
m n
ward to check that {f(i),f(j)} are the vertices of a simplex of K if and
only if {i,j} are the vertices of a simplex of K . Thus f extends to a
m
simplicial isomorphism, so M is homeomorphic to S1.
Surfaces
The rest of this chapter is devoted to the study of compact surfaces. We
have already seen several important examples: the sphere S2, the torus T2,
and the projective plane P2 (i.e., the projective space of dimension 2). As
we will soon see, these examples are fundamental because every compact
surface can be built up from these three.
In order to systematize our knowledge of surfaces, it will be useful to
haveauniformwaytorepresentthemthatissomewhatmoregeneralthan
simplicial complexes. The prototype is the representation of the torus as a

---

120 6. Curves and Surfaces
π
FIGURE 6.2. The sphere as a quotient of the disk.
quotient of the square by identifying the edges in pairs (Example 3.24). It
turns out that every compact surface can be represented as a quotient of a
polygonal region in the plane by an equivalence relation that identifies its
edges in pairs.
Let us begin by seeing how our three basic compact examples can be
so represented. We have already shown how to represent the torus as a
quotient of a square (Example 3.24), so we focus on the sphere and the
projective plane.
Proposition 6.2. The sphere S2 is homeomorphic to the following quo-
tient spaces.
(a) The closed disk B2 ⊂R2 modulo the equivalence relation generated by
(x,y)∼(−x,y) for x∈∂B2 (Figure 6.2).
(b) The square I×I modulo the equivalence relation generated by (0,t)∼
(t,0) and (t,1)∼(1,t) for 0≤t≤1 (Figure 6.3).
Proof. To see that each of these spaces is homeomorphic to the sphere,
all we need to do is exhibit a quotient map from the given space to the
sphere that makes the same identifications, and then appeal to uniqueness
of quotient spaces (Corollary 3.32).
For (a), define a map from the disk to the sphere by wrapping each
horizontal line segment around a “latitude circle” (Figure 6.2). Formally,
π: B2 →S2 is given by
π(x,y)
⎧(cid:26) (cid:27)
⎪⎪⎪⎨
−
(cid:3)
1−y2cos(cid:3)
πx
,−
(cid:3)
1−y2sin(cid:3)
πx
,y , y (cid:14)=±1;
1−y2 1−y2
=
⎪⎪⎪⎩
(0,0,y), y =±1.

---

Surfaces 121
α β
γ π
FIGURE 6.3. The sphere as a quotient of the square.
This is a quotient map by the closed map lemma; it is straightforward to
checkthatitmakesexactlythesameidentificationsasthegivenequivalence
relation.
Toprove(b),wewillconstructaquotientmapfromI×I tothesphereas
a composition of several simpler maps (Figure 6.3). First let S denote the
square {(x,y) : |x|,|y| ≤ 1}, and define a homeomorphism α: I ×I → S
by first scaling both coordinates by a factor of 2 and then translating
the new center (1,1) back to the origin: α(x,y) = (2x−1,2y−1). Then
let β: S → B2 be the homeomorphism whose existence is guaranteed by
Proposition 4.26; it sends each radial line segment between the origin and
the boundary of S linearly onto the parallel segment between the center of
the disk and its boundary. Next let γ: B2 → B2 be the counterclockwise
rotation through π/4 radians (obviously a homeomorphism), and consider
the composite map ϕ=π◦γ◦β◦α:
I×I −α→S −β→B2 −γ→B2 −π→S2,
where π is the quotient map of the preceding paragraph. Since this is a
compositionofquotientmaps,itisaquotientmap.Threadingthroughthe
definitions (with help from the pictures!), you will see that it makes the
same identifications as the quotient map defined in (b), thus completing
the proof.
Proposition 6.3. The projective plane P2 is homeomorphic to each of the
following quotient spaces (Figure 6.4).

---

122 6. Curves and Surfaces
x
−x
(a) (b) (c)
FIGURE 6.4. Representations of P2 as a quotient space.
(a) The sphere S2 modulo the equivalence relation x ∼ −x for each x ∈
S2.
(b) The closed disk B2 modulo the relation (x,y) ∼ (−x,−y) for each
(x,y)∈∂B2.
(c) ThesquareI×I modulotherelation(t,0)∼(1−t,1),(0,1−t)∼(1,t)
for 0≤t≤1.
Proof. Let S2/∼ denote the quotient space of S2 obtained by identifying
eachpointxwithitsantipodalpoint−x,andletp: S2 →S2/∼denotethe
quotient map. Consider also the composite map
S2 (cid:9)→ι R3(cid:3){0}−π→P2,
where ι is inclusion and π is the quotient map defining P2. Note that π◦ι
is a quotient map by the closed map lemma. It makes exactly the same
identificationsasp,sobyuniquenessofquotientspacesP2ishomeomorphic
to S2/∼.
If F: B2 → S2 is(cid:3)the map sending the disk onto the upper hemisphere
by F(x,y) = (x,y, 1−x2−y2), then p◦F: B2 → S2/∼ is easily seen
to be surjective, and is thus a quotient map by the closed map lemma. It
identifies only (x,y) ∈ ∂B2 with (−x,−y) ∈ ∂B2, so P2 is homeomorphic
to the resulting quotient space.
Part (c) is left as an exercise.
Exercise 6.1. Prove Proposition 6.3(c).
When doing geometric “cutting and pasting” constructions like the ones
in the last two propositions, it is often safe to rely on pictures and a few
wordstodescribethemapsandidentificationsbeingconstructed.Sofar,we
havebeencarefultogiveexplicitdefinitions(oftenwithformulas)ofallour
maps, together with rigorous proofs that they do in fact give the results

---

Surfaces 123
v
q
FIGURE 6.5. An edge point. FIGURE 6.6. A vertex.
we claim; but as your sophistication increases and you become adept at
carrying out such explicit constructions yourself, you can leave out many
of the details. The main thing is that before you skip any such details,
youshouldbeabsolutelysurethatyoucouldquicklywritethemdownand
checkyourclaimsrigorously;thisistheonlywaytobesurethatyouarenot
hidingrealdifficultiesbehind“hand-waving.”Inthisbookwewillbeginto
leave out some such details in our proofs; for a while, you should fill them
in for yourself to be sure that you know how to turn an argument based
on pictures into a complete proof.
Now we describe a general method for building surfaces by identifying
edgesofgeometricfigures.LetussaythatasubsetP oftheplaneisapolyg-
onalregionifitisacompactsubsetwhoseboundaryisafinite1-dimensional
Euclidean simplicial complex, satisfying the following conditions:
(i) Eachpointq ofanedgeotherthanavertexhasaneighborhoodU in
R2 suchthatP∩U isequaltotheintersectionwithU ofsomeclosed
half-plane {(x,y):ax+by+c≥0} (Figure 6.5).
(ii) Each vertex v has a neighborhood V in R2 such that P ∩V is equal
totheintersectionofV withtwoclosedhalf-planeswhoseboundaries
intersect only at v (Figure 6.6).
Any finite collection of disjoint 2-simplices in the plane is easily seen to
beapolygonalregion,asisafilled-insquare,oranycompactconvexregion
boundedbyfinitelymany1-simplices.Below,wewillseesomemoreexam-
ples of manifolds obtained as quotients of polygonal regions by identifying
the edges in pairs. It is a general fact that such a quotient space is always
a surface.
Proposition 6.4. Let P be a polygonal region in the plane with an even
number of edges, and suppose we are given an equivalence relation that

---

124 6. Curves and Surfaces
α1
q1
U1 q2
U2
α2
FIGURE 6.7. Euclidean neighborhood of an edge point.
identifies each edge with exactly one other edge by means of a simplicial
homeomorphism. The resulting quotient space is a compact 2-manifold.
Proof. LetM bethequotientspace,andletπ: P →M denotethequotient
map. Clearly, M is compact, because it is the continuous image of the
compact space P.
Since the equivalence relation identifies only edges with edges and ver-
tices with vertices, the points of M fall into three disjoint sets: (a) face
points, whose inverse images in P are in the interior of P; (b) edge points,
whose inverse images are on edges but not vertices; and (c) vertex points,
whose inverse images are vertices. To prove that M is locally Euclidean,
we consider the three types separately.
Because π is injective on IntP, IntP is a saturated open subset of P, so
the restriction of π to IntP is a one-to-one quotient map and therefore a
homeomorphism. Thus π(IntP) is a Euclidean neighborhood of each face
point.
An edge point q(cid:7) has exactly two inverse images q1 and q2, each on a
different edge. Using condition (i) in the definition of polygonal region,
there exist disjoint neighborhoods U1 of q1 and U2 of q2 such that P ∩U
i
is a closed half-disk (Figure 6.7). Let V = P ∩U . It is straightforward
i i
to construct affine homeomorphisms α1 taking V1 to a half-disk in the
upper half-plane and α2 taking V2 to a half-disk in the lower half-plane,
in such a way that q1 and q2 both go to the origin and the boundary
identifications are respected. Define α: V1 ∪V2 →R2 by letting α=α1 on
V1 and α=α2 on V2. Shrinking V1 and V2 if necessary, we can ensure that
V1 ∪V2 is a saturated open set in P (this just means that for each point
in V1 ∩∂P, the corresponding boundary point is in V2, and conversely).
Then the restriction of π to V1 ∪V2 is a quotient map, so α descends to a
mapα(cid:7): V (cid:7) →R2,whereV (cid:7) =π(V1 ∪V2).Itsimagecontainsaneighborhood

---

Surfaces 125
v2
v3
v1
v4
FIGURE 6.8. Euclidean neighborhood of a vertex point.
(cid:7)
of the origin by construction, and its domain V is the image under π of
a saturated open set and therefore open. This shows that q(cid:7)has a locally
Euclidean neighborhood.
Similarly, a vertex point v(cid:7) has as its inverse image a finite set of ver-
tices {v1,…,v
k
} ⊂ P. For each i, choose a homeomorphism from a
neighborhood of v in P to an open subset in a closed “wedge” of an-
i
gle 2π/k in the plane, which is a set described in polar coordinates by
{(r,θ) : θ0 ≤ θ ≤ θ0+2π/k}. (If we place v
i
at the origin, such a homeo-
morphismisgiveninpolarcoordinatesbyafan transformationoftheform
(r,θ)(cid:10)→(r,θ0+cθ) for suitable constants θ0,c.)
Because each edge is paired with exactly one other, the k wedges can
be mapped onto a set containing a neighborhood of the origin by rotating
and piecing them together (Figure 6.8). However, this may not respect
the edge identifications. To correct this, we can subject each wedge to
a preliminary transformation that rescales its edges independently. First,
by a rotation followed by a fan transformation, take the wedge to the first
quadrantsothatoneedgeliesalongthepositivex-axisandtheotheralong
the positive y-axis. Then rescale the two axes by a linear transformation
(x,y) (cid:10)→ (ax,by). Finally, use another fan transformation to insert the
wedge into its place. (The case k = 1 deserves special comment. This
case can occur only if the two edges adjacent to the single vertex v1 are
identified with each other; then you can check that our construction maps
a neighborhood of v1 onto a neighborhood of the origin, with both edges
going to the same ray.) In each case, we end up with a map defined on
a saturated open set in P, which descends to a homeomorphism from a
neighborhood of v(cid:7)to a neighborhood of the origin.
The quotient is second countable by Lemma 3.21. To prove that it is
Hausdorff is the same as showing that the fibers of π can be separated by

---

126 6. Curves and Surfaces
FIGURE 6.9. The Klein bottle.
saturated open sets. It is straightforward to check on a case-by-case basis
that the inverse images of sufficiently small Euclidean balls will do.
Hereisanotherexampleofamanifoldformedasaquotientofapolygonal
region.
Example 6.5. The Klein bottle is the 2-manifold K obtained by iden-
tifying the edges of the square I × I according to (0,t) ∼ (1,t) and
(t,0)∼(1−t,1) for 0≤t≤1. To visualize K, think of gluing the left and
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
manifolds of any dimension, so we will define it in arbitrary dimensions.
Let M1 and M2 beconnected n-manifolds.Geometrically,theconnected
sum is obtained by cutting out a small open ball from each of M1 and M2
andgluingtheresultingspacestogetheralongtheirboundaryspheres.More
precisely,letB ⊂M beregularEuclideanballs.Chooseahomeomorphism
i i
σ: ∂B1 →∂B2 (suchahomeomorphismexistsbecausebothboundariesare
homeomorphic to Sn−1). Let M(cid:5) = M (cid:3)B , and define a quotient space
i i i
of M
1
(cid:5) (cid:20)M
2
(cid:5) by identifying each q ∈ ∂B1 with σ(q) ∈ ∂B2 (Figure 6.10).
The resulting quotient space is called a connected sum of M1 and M2 and
is denoted by M1#M2.
Proposition 6.6. IfM1 andM2 areconnectedn-manifolds,anyconnected
sum M1#M2 is a connected n-manifold.

---

Connected Sums 127
M1 M2
B1 B2
π
M1#M2
FIGURE 6.10. A connected sum.
Proof. FirstweshowthatM1#M2 islocallyEuclidean.Letπ: M
1
(cid:5)(cid:20)M
2
(cid:5) →
M1#M2 denote the quotient map, and let S = π(∂B1 ∪∂B2). Since π is
one-to-one and thus a homeomorphism away from S, M1 #M2 (cid:3)S is a
manifoldandthereforelocallyEuclidean.Thusweneedonlyconsiderpoints
in S.
For any nonempty interval J ⊂ [0,∞), let us use the notation A to
J
denotetheannulus{x∈Rn :|x|∈J}.Thus,forexample,A[1,2) isequalto
B2(0)(cid:3)B1(0). Our regular balls B
i
for i = 1,2 come with neighborhoods
U
i
containingB
i
andhomeomorphismsϕ
i
: U
i
→B2(0)takingU
i
(cid:3)B
i
onto
A[1,2) (Figure 6.11). (If ϕ
i
takes U
i
onto a ball of radius different from 2,
wecanadjustitbyadilationtomakesurethatitsimageis B2(0).)Notice
that ϕ sends ∂B to the unit sphere.
i i
Thefirstthingweneedtodoistoadjustoneofthesemapstocompensate
for the fact that ϕ
−
2
1◦ϕ1
does not make the same identification between
∂B1 and ∂B2 as σ does. To correct this, observe that the composite map
β =ϕ2 ◦σ◦ϕ −
1
1 from Sn−1 ⊂Rn to itself is a homeomorphism:
Sn−1
−ϕ−
1→
1
∂B1 −σ→∂B2 −ϕ→2 Sn−1.
(cid:7)
Defineahomeomorphismβ fromB2(0)toitselfbysendingtheraythrough
each point x0 ∈ Sn−1 linearly onto the ray through β(x0); formally, since

---

128 6. Curves and Surfaces
ϕ1 β (cid:7)
U1 (cid:3)B1 A[1,2) A[1,2)
I
ϕ(cid:7)
1
ϕ2
U2 (cid:3)B2 A(1/2,2)
FIGURE 6.11. Euclidean neighborhood of points in S.
x/|x| is the point where the ray through x intersects Sn−1,
(cid:20) (cid:21)
β (cid:7) (x)=|x|β x .
|x|
Let ϕ(cid:7) 1 =β (cid:7)◦ϕ1. It is immediate from the definitions that
ϕ(cid:7) 1 =ϕ2 ◦σ on ∂B1. (6.1)
TheinversionmapI(x)=x/|x|2 mapstheannulusA[1,2) homeomorphi-
cally onto the annulus A(1/2,1], and restricts to the identity map on Sn−1.
We define a map Φ from the open set (U1 (cid:3)B1)∪(U2 (cid:3)B2) ⊂ M
1
(cid:5) (cid:20)M
2
(cid:5)
to Rn by
(cid:16)
I◦ϕ(cid:7) 1(q), q ∈U1 (cid:3)B1,
Φ(q)=
ϕ2(q), q ∈U2 (cid:3)B2.
Let us check that Φ respects the identifications made by π. If q ∈ ∂B1
and p=σ(q)∈∂B2, then
I◦ϕ(cid:7) 1(q)=ϕ(cid:7) 1(q) (because I is the identity on Sn−1)
=ϕ2 ◦σ(q) (by (6.1))
=ϕ2(p).
ThusΦpassestothequotientanddefinesahomeomorphismfromaneigh-
borhoodofS totheopenannulusA(1/2,2),showingthatM1#M2 islocally

---

Polygonal Presentations of Surfaces 129
# =
FIGURE 6.12. Connected sum with a sphere.
Euclidean. The proofs that it is second countable and Hausdorff are anal-
ogous to those in Proposition 6.4, and are left as an exercise.
To show that M1#M2 is connected, just note M1#M2 is the union of
the two sets π(M(cid:5)) and π(M(cid:5)), which are both connected and have points
1 2
of S in common.
Exercise 6.2. Prove that M1#M2 is Hausdorff and second countable.
Our definition of M1#M2 depends on several choices—the sets B
i
and
the homeomorphism σ. When M1 and M2 are surfaces, it can be shown
that different choices yield homeomorphic connected sums. We will not
prove this in full generality, but in the case of compact surfaces it will
turn out to be a consequence of the classification theorem (see Problem
10-4). Nevertheless, we will sometimes use the imprecise terminology “the
connected sum M1#M2” to refer to any connected sum between M1 and
M2.
Example 6.7. IfM isanyn-manifold,aconnectedsumM#Sn ishomeo-
morphictoM,atleastifwechoosethesettocutoutofSncarefully(Figure
6.12). Let B2 ⊂ Sn be the open lower hemisphere, so (Sn)(cid:5) = Sn (cid:3)B2 is
theclosedupperhemisphere,whichishomeomorphictoaclosedball.Then
M#Sn isobtainedfromM bycuttingouttheopenballB1 andgluingback
a closed ball along the boundary sphere, so we have not changed anything.
Example 6.8. The n-fold connected sum T2 # T2 # ··· # T2 (Figure
6.13), is called the n-holed torus, or the sphere with n handles. The lat-
terterminologyreferstothefactthatthissurfaceisalsohomeomorphicto
S2#T2#···#T2, and each added torus looks like a “handle” attached to
the sphere (Figure 6.14).
Polygonal Presentations of Surfaces
As we mentioned earlier in this chapter, for the classification theorem we
needauniformwaytodescribesurfaces.Wewillrepresentallofoursurfaces

---

130 6. Curves and Surfaces
FIGURE 6.13. A connected sum of tori.
FIGURE 6.14. A sphere with handles.
asquotientsof2n-sidedpolygonalregions.Informally,wecandescribeany
edge equivalence relation by labeling the edges with letters a1,…,a
n
, and
giving each edge an arrow pointing toward one of its vertices, in such a
way that edges with the same label are to be identified, with the arrows
indicating which way the vertices match up. With each such labeling of a
polygon we associate a sequence of symbols, obtained by reading off the
boundarylabelscounterclockwisefromthetop,andforeachboundarylabel
−1
a , placing a in the sequence if the arrow points counterclockwise and a
i i i
if it points clockwise. For example, the equivalence relation on I ×I of
Example3.24thatyieldsthetorusmightresultinthesequenceofsymbols
aba−1b−1.
Formally,givenasetS,wedefineawordinS tobeanorderedk-tupleof
symbols, each of the form a or a−1 for some a∈S. (To be more precise, if
youlike,youcandefineawordtobeafinitesequenceoforderedpairsofthe
form(a,1)or(a,−1)fora∈S,andthendefineaanda−1 asabbreviations
for (a,1) and (a,−1), respectively.) A polygonal presentation, written
P=(cid:22)S |W1,…,W
k
(cid:23),
isafinitesetS togetherwithfinitelymanywordsW1,…,W
k
inS oflength
3 or more, such that every symbol in S appears in at least one word. As a

---

Polygonal Presentations of Surfaces 131
a a a a
S2 P2
FIGURE 6.15. Presentations of S2 and P2.
matter of notation, when the set S is described by listing its elements, we
willleaveoutthebracessurroundingtheelementsofS,andwilldenotethe
wordsW byjuxtaposition,soforexamplethepresentationwithS ={a,b}
i
and the single word W = (a,b,a−1,b−1) will be written (cid:22)a,b | aba−1b−1(cid:23).
WealsoallowasaspecialcaseanypresentationinwhichS hasoneelement
and there is a single word of length 2. There are only four such: (cid:22)a | aa(cid:23),
(cid:22)a|a−1a−1(cid:23), (cid:22)a|aa−1(cid:23), and (cid:22)a|a−1a(cid:23).
Any polygonal presentation P determines a topological space |P|, called
the geometric realization of P, by the following recipe:
1. For each word W , let P denote the convex k-sided polygonal region
i i
in the plane that has its center at the origin, sides of length 1, and
one vertex on the positive y-axis. (Here k is the length of the word
W .)
i
2. Define a one-to-one correspondence between the symbols of W and
i
the edges of P in counterclockwise order, starting at the vertex on
i
the y-axis.
(cid:6)
3. Let |P| denote the quotient space of P determined by identifying
i i
each pair of edges that have the same edge symbol according to the
simplicialhomeomorphismthatmatchesupthefirstverticesincoun-
terclockwise order if both edges have the same label a or a−1, and
matches the first vertex of one with the second vertex of the other if
the edges are labeled a and a−1.
IfPisoneofthespecialpresentationswithawordoflength2,motivated
by Propositions 6.2 and 6.3 we define |P| to be the sphere if the word is
aa−1 or a−1a, and the projective plane if it is aa or a−1a−1 (Figure 6.15).
The interiors, edges, and vertices of the polygonal regions P are called
i
thefaces,edges,andverticesofthepresentation.Thenumberoffacesisthe
sameasthenumberofwords,whilethenumberofedgesisthetotalnumber
of symbols that occur in all the words. For an edge labeled a, the initial
vertex is the first one in counterclockwise order, and the terminal vertex

---

132 6. Curves and Surfaces
F
p1
p2
P1 P2
FIGURE 6.16. Simplicial homeomorphism between polygons.
is the other one; for an edge labeled a−1, these definitions are reversed.
In terms of our informal description above, if we label each edge with an
arrow pointing counterclockwise when the symbol is a and clockwise when
it is a−1, the arrow points from the initial vertex to the terminal vertex.
The geometric realization of a presentation with only one face is con-
nected, because it is a quotient of a single connected polygon; with more
thanoneface,itmightormightnotbeconnected.Althoughfordefiniteness
we have defined the geometric realization as a quotient of a disjoint union
of a specific collection of polygonal regions, the following lemma shows
that we could have used arbitrary disjoint convex polygonal regions in the
planewiththesamenumbersofedges,becausebetweenanytwopolygonal
regions with the same sequence of edge labels there is a homeomorphism
that respects the edge labels. Because of this, in the arguments that fol-
low we will illustrate our presentations with any convex polygons that are
convenient.
Lemma 6.9. LetP1,P2 beconvexpolygonswiththesamenumberofedges,
and let f: ∂P1 → ∂P2 be a simplicial homeomorphism. Then f extends to
a homeomorphism F: P1 →P2.
Proof. Choose any points p ∈ IntP , i = 1,2. By convexity, the line seg-
i i
mentfromp toeachvertexofP liesentirelyinP .Theedgesandvertices
i i i
of P together with p , these new line segments, and the triangles they
i i
bound form a Euclidean simplicial complex whose polyhedron is P (Fig-
i
ure 6.16). The required map F: P1 → P2 is the simplicial map whose
restriction to ∂P1 is f and that takes p1 to p2.
A polygonal presentation is called a surface presentation if each symbol
a ∈ S occurs exactly twice in W1,…,W
k
(counting either a or a−1 as
one occurrence). By Proposition 6.4, the geometric realization of a surface
presentation is a compact surface.

---

Polygonal Presentations of Surfaces 133
a a a a
b a b b b b b b
b a a a
S2 T2 P2 K
FIGURE 6.17. Standard presentations.
Example 6.10. Thefollowingsurfacesaredeterminedbythegivenpolyg-
onalpresentations,whichwecalltheirstandardpresentations(Figures6.15
and 6.17).
(a) The sphere: (cid:22)a|aa−1(cid:23) or (cid:22)a,b|abb−1a−1(cid:23) (Proposition 6.2).
(b) The torus: (cid:22)a,b|aba−1b−1(cid:23) (Example 3.24).
(c) The projective plane: (cid:22)a|aa(cid:23) or (cid:22)a,b|abab(cid:23) (Proposition 6.3).
(d) The Klein bottle: (cid:22)a,b|abab−1(cid:23) (Example 6.5).
IfKisa2-dimensionalsimplicialcomplexinwhicheverysimplexiscon-
tainedinsome2-simplex,thenKdeterminesinanobviouswayapolygonal
presentation in which each 2-simplex corresponds to a word of length 3.
For later use in proving the classification theorem, we will develop some
generalrulesfortransformingpolygonalpresentations.Iftwopresentations
P 1 andP 2 havehomeomorphicgeometricrealizations,wewillsaythatthey
are topologically equivalent and write P 1 ≈P 2.
The following operations are called elementary transformations of a
polygonal presentation. As a matter of notation, in what follows S will
denote any sequence of symbols; a,b,c,a1,a2,… will denote any symbols
fromS ortheirinverses;ewilldenoteanysymbolnotinS;andW1,W2,…
will denote any words made from the symbols in S. Given two words
W1,W2, the notation W1W2 denotes the word formed by concatenating
W1 and W2 together. We adopt the convention that (a−1)−1 =a.
- Relabeling:Changingalloccurrencesofasymbolatoanewsymbol
not already in the presentation, interchanging all occurrences of two
symbols a and b, or interchanging all occurrences of a and a−1 for
some a∈S.
- Subdividing: Replacing every occurrence of a by ae and every oc-
currence of a−1 by e−1a−1, where e is a new symbol not already in
the presentation.

---

134 6. Curves and Surfaces
a1
a5 a5
a1 a1
a5
a2
a1
a2 a2 a2
a3
a3 a4 a4 a3 a3 a4 a4 a5
FIGURE 6.18. Reflecting. FIGURE 6.19. Rotating.
a e
a c
e
e
W1 W2 W1
e
W2 b e
c
b
FIGURE 6.20. Cutting/pasting. FIGURE 6.21. Folding/unfolding.
- Consolidating:Ifaandbalwaysoccuradjacenttoeachothereither
as ab or b−1a−1, replacing every occurrence of ab by a and every
occurrence of b−1a−1 by a−1, provided that the result is one or more
words of length at least 3 or a single word of length 2.
- Reflecting (Figure 6.18):
(cid:22)S |a1…a
m
, W2,…,W
k
(cid:23)(cid:10)→(cid:22)S |a−
m
1…a
1
−1 , W2,…,W
k
(cid:23).
- Rotating (Figure 6.19):
(cid:22)S |a1a2…a
m
, W2,…,W
k
(cid:23)(cid:10)→(cid:22)S |a2…a
m
a1, W2,…,W
k
(cid:23).
- Cutting (Figure 6.20): If W1 and W2 both have length at least 2,
(cid:22)S |W1W2, W3,…,W
k
(cid:23)(cid:10)→(cid:22)S,e|W1e, e−1W2, W3,…,W
k
(cid:23).
- Pasting (Figure 6.20):
(cid:22)S,e|W1e, e−1W2, W3,…,W
k
(cid:23)(cid:10)→(cid:22)S |W1W2, W3,…,W
k
(cid:23).
- Folding (Figure 6.21): If W1 has length at least 3,
(cid:22)S,e|W1ee−1, W2,…,W
k
(cid:23)(cid:10)→(cid:22)S |W1, W2,…,W
k
(cid:23).
We also allow W1 to have length 2, provided that the presentation
has only one word.

---

Polygonal Presentations of Surfaces 135
- Unfolding (Figure 6.21):
(cid:22)S |W1, W2,…,W
k
(cid:23)(cid:10)→(cid:22)S,e|W1ee−1, W2,…,W
k
(cid:23).
Proposition 6.11. Each elementary transformation of a polygonal pre-
sentation produces a topologically equivalent presentation.
Proof. Clearly, subdividing and consolidating are inverses of each other,
as are cutting/pasting and folding/unfolding, so by symmetry only one of
each pair needs to be proved. We demonstrate the techniques by proving
the proposition for cutting and folding, and leave the rest as exercises.
To prove that cutting produces a homeomorphic geometric realization,
let P1 and P2 be convex polygons labeled W1e and e−1W2, respectively,
and let P(cid:5) be a convex polygon labeled W1W2. For the moment, let us
assume that these are the only words in their respective presentations. Let
π: P1 (cid:20)P2 → S and π(cid:5): P(cid:5) → S(cid:5) denote the respective quotient maps.
The line segment going from the terminal vertex of W1 in P(cid:5) to its initial
vertex lies in P(cid:5) by convexity; label this segment e. By Lemma 6.9 there is
a continuous map f: P1 (cid:20)P2 →P(cid:5) that takes each edge of P1 or P2 to the
edge in P(cid:5) with the corresponding label, and whose restriction to each P
i
isahomeomorphism.Bytheclosedmaplemma,f isaquotientmap.Since
f identifies the two edges labeled e and e−1 but nothing else, the quotient
mapsπ(cid:5)◦f andπ makepreciselythesameidentifications,sotheirquotient
spaces are homeomorphic. If there are other words W3,…,W
k
, we just
extendf bydeclaringittobetheidentityontheirrespectivepolygonsand
proceed as above.
For folding, as before we can ignore the additional words W2,…,W
k
. If
W1 has length 2, we can subdivide to lengthen it, then perform the folding
operation, and then consolidate, so we assume that W1 has length at least
3.AssumefirstthatW1 =abchaslengthexactly3.LetP andP(cid:5) beconvex
polygonswithedgelabelsabcee−1 andabc,respectively,andletπ: P →S,
π(cid:5): P(cid:5) → S(cid:5) be the quotient maps. Adding edges as shown in Figure 6.21
turnsP andP(cid:5) intopolyhedraofEuclideansimplicialcomplexes,andthere
isauniquesimplicialmapf: P →P(cid:5) thattakeseachedgeofP totheedge
of P(cid:5) with the same label. As before, π(cid:5)◦f and π are quotient maps that
make the same identifications, so their quotient spaces are homeomorphic.
IfW1 haslength4ormore,wecanwriteW1 =XbcforsomeX oflength
at least 2. Then we cut along a to obtain
(cid:22)S,b,c,e|Xbcee−1(cid:23)≈(cid:22)S,a,b,c,e|Xa−1,abcee−1(cid:23),
and proceed as before.
Exercise 6.3. ProvetherestofProposition6.11.Notethatyouwillhave
to consider a word of length 2 as a special case when treating subdividing
or consolidating.

---

136 6. Curves and Surfaces
v
a
W1
v
W1
f
b a
a c b v
c
c
v b
P 1 (cid:5) Q P1
π(cid:5) π
(cid:7)
f
M1 B1 M1
FIGURE 6.22. The presentation (cid:8)S1,a,b,c|W1c−1b−1a−1,abc(cid:9).
Next we need to find standard polygonal presentations for connected
sums. The key is the following proposition.
Proposition 6.12. Let M1 and M2 be surfaces determined by presenta-
tions (cid:22)S1 |W1 (cid:23) and (cid:22)S2 |W2 (cid:23), respectively, in which S1 and S2 are disjoint
sets and each presentation has a single face. Then (cid:22)S1,S2 | W1W2 (cid:23) is a
presentation of a connected sum M1#M2. (Here W1W2 denotes the word
formed by concatenating W1 and W2 together.)
Proof. Consider the presentation (cid:22)S1,a,b,c|W1c−1b−1a−1,abc(cid:23) (pictured
in the left half of Figure 6.22). Pasting along a and folding twice, we see
that this presentation is equivalent to (cid:22)S1 | W1 (cid:23) and therefore is a pre-
sentation of M1. Let B1 denote the image in M1 of the interior of the
polygonal region bounded by triangle abc. We will show below that B1
is a regular Euclidean disk in M1. Assuming this, it follows immediately
that the geometric realization of (cid:22)S1,a,b,c | W1c−1b−1a−1(cid:23) is homeomor-
phic to M1 (cid:3)B1 (which we denote by M
1
(cid:5)), and ∂B1 is the image of the
edges c−1b−1a−1. A similar argument shows that (cid:22)S2,a,b,c | abcW2 (cid:23) is a
presentationofM2 withaEuclideandiskremoved(denotedbyM
2
(cid:5)).There-
fore, (cid:22)S1,S2 |W1c−1b−1a−1,abcW2 (cid:23) is a presentation of M
1
(cid:5)(cid:20)M
2
(cid:5) with the
boundaries of the respective disks identified, which is M1 #M2. Pasting
along a and folding twice, we arrive at the presentation (cid:22)S1,S2 |W1W2 (cid:23).
ItremainsonlytoshowthatB1isaregulardiskinM1,i.e.,thatithasan
open disk neighborhood in which B1 corresponds to a smaller closed disk.
LetP1,P
1
(cid:5),andQbeconvexpolygonswithedgeslabeledbythewordsW1,
W1c−1b−1a−1, and abc, respectively. Triangulating the polygons as shown
in Figure 6.22, we obtain a simplicial map f: P
1
(cid:5)(cid:20)Q→P1 such that π◦f

---

Classification of Surface Presentations 137
v
FIGURE 6.23. Showing that B1 is a regular disk.
makesthesameidentificationsasπ(cid:5),andsodescendstoahomeomorphism
f (cid:7) : M1 →M1. The inverse image of f (cid:7) (B1) under π is a small triangle in P1
sharing one vertex v in common with P1.
Now look back at the proof in Proposition 6.4 that the quotient space
of a surface presentation is a manifold. In constructing a Euclidean neigh-
borhood of a vertex point, we assembled “wedges” at the various vertices
intoaEuclideandisk.Applyingthatconstructiontothevertexv,thesmall
triangleistakentoasetthatishomeomorphictoacloseddiskintheplane
(Figure 6.23), and it is an easy matter to extend that homeomorphism to
a slightly larger open disk.
Example 6.13. Usingtheprecedingproposition,wecanaugmentourlist
of presentations of known surfaces as follows:
- Connected sum of n tori:
(cid:22)a1,b1,…,a
n
,b
n
|a1b1a −
1
1 b −
1
1 …a
n
b
n
a−
n
1b−
n
1(cid:23).
- Connected sum of n projective planes:
(cid:22)a1,…,a
n
|a1a1…a
n
a
n
(cid:23).
We call these the standard presentations of these surfaces.
Classification of Surface Presentations
We are now ready to state the main result in the classification of surfaces.
This theorem was first proved in 1907 by Max Dehn and Poul Heegaard
[DH07] under the assumption that the surface had some polygonal presen-
tation. Using the triangulation theorem of Chapter 5, we now know that
every compact surface has a triangulation, which determines a polygonal
presentation.

---

138 6. Curves and Surfaces
a a b
c b a a b a
b b b c b b c
a a c c c
FIGURE 6.24. Transforming the Klein bottle to P2#P2.
Theorem 6.14 (Classification of Surface Presentations). Any sur-
face presentation is equivalent by a sequence of elementary transformations
to a presentation of one of the following:
(a) the sphere S2;
(b) a connected sum T2#···#T2; or
(c) a connected sum P2#···#P2.
Therefore, every compact surface is homeomorphic to one of the surfaces
in this list.
Before we prove the theorem, we need to make one important observa-
tion. You might have noticed that some surfaces appear to be absent from
the list—the Klein bottle, for example, and T2 #P2, and, for that mat-
ter, every connected sum involving both tori and projective planes. These
apparent deficiencies are explained by the following two lemmas.
Lemma 6.15. The Klein bottle is homeomorphic to P2#P2.
Proof. Byasequenceofelementarytransformations,wefindthattheKlein
bottle has the following presentations (see Figure 6.24):
(cid:22)a,b|abab−1(cid:23)
≈(cid:22)a,b,c|abc, c−1ab−1(cid:23) (cut along c)
≈(cid:22)a,b,c|bca,a−1cb(cid:23) (rotate and reflect)
≈(cid:22)b,c|bbcc(cid:23). (paste along a and rotate)
This last is a presentation of the connected sum of two projective planes.
Lemma 6.16. TheconnectedsumT2#P2 ishomeomorphictoP2#P2#P2.
Proof. Start with (cid:22)a,b,c|abab−1cc(cid:23) (Figure 6.25), which is a presentation
ofK#P2,andthereforebytheprecedinglemmaofP2#P2#P2.Following
Figure 6.25, we cut along d, paste along c, cut along e, and paste along b,
rotating and reflecting as necessary, to obtain (cid:22)a,d,e|a−1d−1adee(cid:23), which
is a presentation of T2#P2.

---

Classification of Surface Presentations 139
a
a d a d
b c
d
b c c a b a
a c e
b d b d b
a a
d d d d
b
b
e a e a
e e
FIGURE 6.25. Transforming P2#P2#P2 to T2#P2.
Proof of the classification theorem. By the triangulation theorem we can
assumethatM comeswithagivenpresentation.Wewillprovethetheorem
by transforming this presentation to one of our standard presentations in
several steps. Let us say that a pair of edges that are to be identified
are complementary if they appear in the presentation as both a and a−1,
and twisted if they appear as a,…,a or as a−1,…,a−1. (The terminology
reflects the fact that if a polygonal region is cut from a piece of paper, you
have to twist the paper to paste together a twisted edge pair, but not for
a complementary pair.)
Step 1: M admits a presentation with only one face. Since M is con-
nected, if there are two or more faces, some edge in one face must be
identified with an edge in a different face; otherwise, M would be the dis-
jointunionofthequotientsofitsfaces,andsinceeachsuchquotientisopen
andclosed,theywouldprovideaseparationofM.Thusbyperformingsuc-
cessive pasting transformations (together with rotations and reflections as
necessary), we can reduce the number of faces in the presentation to one.
Step2:EitherM ishomeomorphictothesphere,orM admitsapresen-
tation in which there are no adjacent complementary pairs. Each adjacent
complementary pair can be eliminated by folding, unless it is the only pair
of edges in the presentation; in this case the presentation is equivalent to
(cid:22)a|aa−1(cid:23) and M is homeomorphic to the sphere.
From now on, we assume that the presentation is not the standard pre-
sentation of the sphere.
Step 3:M admits a presentation in which all twisted pairs are adjacent.
If a twisted pair is not adjacent, the presentation is described by a word of
the form VaWa, where neither V nor W is empty. Figure 6.26 shows how
to transform the word VaWa into VW−1bb by cutting along b, reflecting,
and pasting along a. (Here W−1 denotes the word obtained from W by
reflecting).Inthislastpresentation,thetwistedpaira,ahasbeenreplaced

---

140 6. Curves and Surfaces
V V VW−1
a
a b
b
W−1
a
b
a
W
b b
FIGURE 6.26. Making a twisted pair adjacent.
byanothertwistedpairb,b,whichisnowadjacent.Moreover,nootherad-
jacent pairs have been separated. We may have created some new twisted
pairs when we reflected W, but we decreased the total number of nonadja-
cent pairs by at least one. Thus, after finitely many such operations, there
willbenomorenonadjacenttwistedpairs.Wemayalsohavecreatedsome
new adjacent complementary pairs. These can be eliminated by repeating
Step 2, which does not increase the number of nonadjacent pairs.
Step 4: M admits a presentation in which all vertices are identified to
a single point. Choose some equivalence class of vertices, and call it v.
If there are vertices that are not identified with v, there must be some
edge that goes from a v vertex to a vertex in some other equivalence class;
label the edge a and the other vertex class w (Figure 6.27). The other
edge that touches a at its v vertex cannot be identified with a: If it were
complementarytoa,wewouldhaveeliminatedbothedgesinStep3,while
ifitformedatwistedpairwitha,thenthequotientmapwouldidentifythe
initial and terminal vertices of a with each other, which we are assuming
is not the case. So label this other edge b, and label its other vertex x (this
one may be identified with v, w, or neither one).
Somewhereinthepolygonisanotheredgelabeledborb−1.Letusassume
for definiteness that it is b−1; the argument for b is similar except for an
extrareflection.Thuswecanwritetheworddescribingthepresentationin
the form baXb−1Y, where X and Y are unknown words, not both empty.
NowcutalongcandpastealongbasinFigure6.27.Inthenewpresentation,
the number of vertices labeled v has decreased, and the number labeled w
has increased. We may have introduced a new adjacent complementary
pair, so perform Step 2 again to remove it. This may again decrease the
number of vertices labeled v (for example, if a v vertex lies between edges
labeled aa−1 that are eliminated by folding), but it cannot increase their
number. So repeating this sequence a finite number of times—decrease
the v vertices by one, then eliminate adjacent complementary edges—we
eventually eliminate the vertex class v from the presentation altogether.
Iterate this procedure for each vertex class until there is only one left.
Step 5: If the presentation has any complementary pair a,a−1,
then it has another b,b−1 that occurs intertwined with the first, as in
a,…,b,…,a−1,…,b−1. If this is not the case, then the presentation is of
theformaXa−1Y,whereX containsonlymatchedcomplementarypairsor

---

Classification of Surface Presentations 141
v w c x
a b
w x X Y
c
b
X Y v x
a c
v b x w
FIGURE 6.27. Reducing the number of vertices equivalent to v.
c c
W b
a b b b c Z d X
c Y Z d c Y
X Z b W
a b
a b
b a Y c
Y X W X d Z
c W
FIGURE 6.28. Bringing intertwined complementary pairs together.
adjacenttwistedpairs.ThuseachedgeinX isidentifiedonlywithanother
edge in X, and the same is true of Y. But this means that the terminal
verticesoftheaanda−1 edges,bothofwhichtouchonlyX,canbeidenti-
fiedonlywithverticesinX,whiletheinitialverticescanbeidentifiedonly
with vertices in Y. This is a contradiction, since all vertices are identified
together by Step 4.
Step6:M admitsapresentationinwhichallintertwinedcomplementary
pairs occur together with no other edges intervening: aba−1b−1. If the pre-
sentation is given by the word WaXbYa−1Zb−1, perform the elementary
transformations indicated in Figure 6.28 (cut along c, paste along a, cut
alongd,andpastealongb)toobtainthenewwordcdc−1d−1WZYX.This
replaces the old intertwined set of pairs with a new adjacent set cdc−1d−1,
withoutseparatinganyedgesthatwerepreviouslyadjacent.Repeatthisfor
each set of intertwined pairs. (Note that this step requires no reflections.)
Step 7: M is homeomorphic to either a connected sum of tori or a con-
nected sum of projective planes.Fromwhatwehavedonesofar,alltwisted
pairs occur adjacent to each other, and all complementary pairs occur in
intertwinedgroupslikeaba−1b−1.Thisisapresentationofaconnectedsum

---

142 6. Curves and Surfaces
of tori (presented by aba−1b−1) and projective planes (presented by cc). If
there are only tori or only projective planes, we are done.
The only remaining case is that in which the presentation contains both
twistedandcomplementarypairs.Inthatcase,sometwistedpairmustoc-
cur next to a complementary one; thus the presentation is described either
byawordoftheformaba−1b−1ccX orbyoneoftheformccaba−1b−1X.In
eithercase,thisisaconnectedsumofatorus,aprojectiveplane,andwhat-
ever surface is described by the word X. But Lemma 6.16 shows that the
standardpresentationofT2#P2 canbetransformedtothatofP2#P2#P2.
Making this transformation, we eliminate one of the occurrences of T2 in
the connected sum. Iterating this procedure, we eliminate them all, thus
completing the proof.
Combinatorial Invariants
Two of the properties of simplicial complexes introduced in Chapter 5—
orientations and the Euler characteristic—generalize easily to polygonal
surface presentations, and give us interesting information about surfaces.
Letusextendthenotionofcombinatorialinvariancebysayingthataprop-
erty of a polygonal presentation is a combinatorial invariant if it is un-
changed by elementary transformations. Of course, any topological invari-
ant of the geometric realization (such as connectedness) is automatically a
combinatorial invariant, because elementary transformations yield homeo-
morphic surfaces. It would not be difficult to show that every polygonal
presentationcanbetriangulatedandthatthetwonotionsofcombinatorial
invariants coincide; however, in this case it is easier just to work directly
with the polygonal presentations.
The Euler Characteristic
The Euler characteristic can be generalized to polygonal presentations in
the following form. If P is a polygonal presentation, define the Euler char-
acteristic of P to be V −E+F, where V is the number of vertices (after
identifications), E is the number of edge symbols (which is equal to the
number of edges after identifications), and F is the number of faces. If P
is the presentation determined by a 2-dimensional simplicial complex, it is
easytocheckthatthisdefinitionagreeswiththedefinitiongiveninChapter
5.
Theorem 6.17. The Euler characteristic of a polygonal presentation is
unchanged by elementary transformations.
Proof. It is obvious that relabeling, rotating, and reflecting do not change
the Euler characteristic of a presentation, because they leave the numbers

---

Combinatorial Invariants 143
of vertices, edges, and faces individually unchanged. For the other trans-
formations, we need only check that the changes to these three numbers
cancelout.Subdividingincreasesboththenumberofedgesandthenumber
ofverticesbyone,leavingthenumberoffacesunchanged.Cuttingincreases
both the number of edges and the number of faces by one, and leaves the
numberofverticesunchanged.Unfoldingincreasesthenumberofedgesand
the number of vertices by one, and leaves the number of faces unchanged.
Finally, consolidating, pasting, and folding leave the Euler characteristic
unchanged, since they are the inverses of subdividing, cutting, and unfold-
ing, respectively.
Proposition 6.18 (Euler Characteristics of Compact Surfaces).
The Euler characteristic of a standard surface presentation is equal to
(a) 2 for the sphere;
(b) 2−2n for the connected sum of n tori;
(c) 2−n for the connected sum of n projective planes.
Proof. Just compute.
These results allows us to conclude a great deal about a surface from a
given presentation, without actually carrying out the reduction to a stan-
dardpresentation.Forexample,anypresentationwithEulercharacteristic
2 gives the sphere, and a presentation with Euler characteristic 0 gives
either the torus or the Klein bottle ≈P2#P2.
At the moment, we do not know that the Euler characteristic is a topo-
logical invariant, for the simple reason that we still do not know that the
standard surfaces on our list are not homeomorphic to each other. (If you
donotbelievethis,justtrytoprove,forexample,thattheprojectiveplane
is not homeomorphic to the torus using the techniques we have developed
so far!) The problem is that we cannot yet rule out the possibility that P2,
say, could have a presentation that is so exotic that it is not related to the
standardonebyaseriesofelementarytransformations,butsomehowman-
ages to reduce to a presentation of the torus after following the algorithm
oftheclassificationtheorem.WewillremedythisdeficiencyinChapter10,
when we show that all of our standard compact surfaces are topologically
distinct;onlythenwillwebeabletocompletetheclassificationofcompact
surfaces.
TheEulercharacteristiccanbeusedbyitselftodistinguishpresentations
that reduce to connected sums of different numbers of tori or connected
sums of different numbers of projective planes. However, to distinguish a
presentationoftheconnectedsumof ntorifromoneoftheconnectedsum
of 2n projective planes (for example, the torus from the Klein bottle), we
will need one more property: orientability.

---

144 6. Curves and Surfaces
Orientability
In Chapter 5 we introduced the notion of orientation of a simplicial com-
plex. In this section we show how to extend it to polygonal presentations.
Note that a permutation of a set with three elements is even if and only
if it is a cyclic permutation (i.e., of the form i (cid:10)→ j (cid:10)→ k (cid:10)→ i). Thus an
orientation of a 2-simplex is just an equivalence class of vertex orderings
modulo cyclic permutations. Suppose P is a surface presentation arising
from a simplicial complex, so that every word has length 3. Each word
determines an orientation of the associated 2-simplex, by ordering the ver-
tices in counterclockwise order. It is easy to check that when two simplices
are glued together via an edge pairing, their orientations are consistent if
and only if the edge pair is complementary. Motivated by this, we make
the following definition. A surface presentation P is said to be oriented if
it has no twisted edge pairs. Intuitively, this means that you can decide
whichisthe“front”side(or“outside”)of|P|bycoloringthetopsurfaceof
each polygon white and the bottom side gray; the condition on edge pairs
ensures that the colors will match up when edges are pasted together.
A compact surface is said to be orientable if it admits an oriented pre-
sentation. By looking a little more closely at the proof of the classification
theorem, we can identify exactly which compact surfaces are orientable.
Proposition 6.19. A compact surface is orientable if and only if it is
homeomorphic to the sphere or a connected sum of one or more tori.
Proof. The standard presentations of the sphere and the connected sums
oftoriareoriented,sothesesurfacesarecertainlyorientable.Toshowthat
an orientable surface is homeomorphic to one of these, let M be any sur-
face that admits at least one orientable presentation. Starting with that
presentation, follow the algorithm described in the proof of the classifi-
cation theorem to transform it to one of the standard presentations. The
only elementary transformation that can introduce a twisted pair into an
oriented presentation is reflection. The only steps in which reflections are
used are Steps 3, 4, and 7, and you can check that none of those steps
require any reflections if there were no twisted pairs to begin with. Thus
the classification theorem tells us that the presentation can be reduced to
one of the standard ones with no twisted pairs, which means that M is
homeomorphic to a sphere or a connected sum of tori.
Because of this result, the connected sum of n tori is also known as the
orientablesurfaceofgenus n,andtheconnectedsumofnprojectiveplanes
iscalledthenonorientable surface of genus n.Byconvention,thesphereis
the (unique, orientable) surface of genus 0. Technically, this terminology is
premature,becausewestilldonotknowthataconnectedsumofprojective
planes is not homeomorphic to an oriented surface. But for now we will
go ahead and use this standard terminology with the caveat that all we

---

Combinatorial Invariants 145
know about the “nonorientable surface of genus n” is that its standard
presentation is not oriented.
Before moving away from classification theorems, it is worth remarking
onthesituationwithhigher-dimensionalmanifolds.Becauseofthetriangu-
lation theorem for 3-manifolds stated in Chapter 5, one might hope that a
similarapproachtoclassifying3-manifoldsmightbearfruit.Unfortunately,
the combinatorial problem of reducing any given 3-manifold triangulation
to some standard form is, so far, unsolved. And this approach cannot get
us very far in dimensions higher than 3, because we do not have trian-
gulation theorems. Thus, in order to make any progress in understanding
higher-dimensional manifolds, as well as to resolve the question of whether
the standard surfaces are distinct, we will need to develop more powerful
tools. This we will do in the remainder of the book.

---

146 6. Curves and Surfaces
Problems
6-1. For each of the following surface presentations, compute the Euler
characteristic, and then apply the algorithm of the classification the-
orem to determine which of our standard surfaces it is.
(a) (cid:22)a,b,c|abacb−1c−1(cid:23).
(b) (cid:22)a,b,c|abca−1b−1c−1(cid:23).
(c) (cid:22)a,b,c,d,e,f |abc, bde, c−1df, e−1fa(cid:23).
(d) (cid:22)a,b,c,d,e,f,g,h,i,j,k,l,m,n,o|
abc, bde, dfg, fhi, haj, c−1kl, e−1mn,
g−1ok−1, i−1l−1m−1, j−1n−1o−1(cid:23).
6-2. Showthataconnectedsumofoneormoreprojectiveplanescontains
a subspace that is homeomorphic to the M¨obius band.
6-3. Show that the projective plane is homeomorphic to the quotient ob-
tainedbygluingaM¨obiusbandandadisktogetheralongtheircom-
mon boundary.
6-4. ShowthattheKleinbottleishomeomorphictothequotientobtained
by gluing two M¨obius bands together along their common boundary.

---

7
Homotopy and the Fundamental
Group
The results of the preceding chapter left a serious gap in our attempt to
classify compact 2-manifolds up to homeomorphism: Although we have
exhibitedalistofsurfacesandshownthateverycompact,connectedsurface
is homeomorphic to one on the list, we still have no way of knowing when
two surfaces are not homeomorphic. For all we know, all the surfaces on
our list might be homeomorphic to the sphere! (Think, for example, of the
unexpected homeomorphism between P2#P2#P2 and T2#P2.)
To distinguish nonhomeomorphic surfaces, we need topological invari-
ants. For some surfaces, the properties we already know suffice. For exam-
ple,the2-sphereisnothomeomorphictotheplanebecauseoneiscompact,
while the other is not. The plane, the disjoint union of two planes, and the
disjoint union of three planes are all topologically distinct, because they
have different numbers of components. It follows from Problem 4-1 that
thelineisnothomeomorphictotheplane;theproofinvolvedarathersub-
tle use of connectedness. But to decide whether, for example, the sphere is
homeomorphictothetorus,ortheplaneishomeomorphictothepunctured
plane R2(cid:3){0}, we need to introduce some new invariants.
Inthischapterwebeginourstudyofthefundamentalgroup,analgebraic
groupthatmeasuresthenumberof“holes”inaspace,inacertainsense.To
set the stage, let us think about the difference between the plane and the
punctured plane. Both are connected, noncompact 2-manifolds, so they
cannot be distinguished by any of the basic topological properties that
we have discussed so far. Yet intuition suggests that they should not be
homeomorphic to each other because the punctured plane has a “hole,”
while the full plane does not.

---

148 7. Homotopy and the Fundamental Group
Toseehowthisdistinctionmightbedetectedtopologically,observethat
every closed curve in R2 can be continuously shrunk to a point (you will
prove this rigorously in Exercise 7.3 below); by contrast, it is intuitively
clear that a circle drawn around the hole in the space R2(cid:3){0} can never
becontinuouslyshrunktoapointwhileremaininginthespace,andinfact
cannotbedeformedintoanyclosedpaththatdoesnotgoaroundthehole.
Wewilldefineanequivalencerelationonclosedpathswithafixedstart-
ing and ending point: Two paths are equivalent if one can be continuously
deformed into the other while keeping the starting and ending point fixed.
Thesetofequivalenceclassesiscalledthefundamentalgroupofthespace;
the product of two elements of the group is obtained by first following one
path and then the other. After making the basic definitions, we will prove
that homeomorphic spaces have isomorphic fundamental groups. Then we
willprovethatthefundamentalgroupsatisfiesanevenstrongerinvariance
property, that of homotopy invariance. As a consequence, we will be able
toreducethecomputationsoffundamentalgroupsofmanyspacestothose
of simpler ones.
Provingthatthefundamentalgroupofaspaceisnottrivialturnsoutto
be somewhat harder, and we will not do so until the next chapter.
Homotopy
Let X and Y be topological spaces, and let f,g: X → Y be continuous
maps. A homotopy from f to g is a continuous map H: X×I →Y (where
I =[0,1] is the unit interval) such that for all x∈X,
H(x,0)=f(x); H(x,1)=g(x). (7.1)
If there exists a homotopy from f to g, we say that f and g are homo-
topic, and write f (cid:25) g (or H: f (cid:25) g if we want to emphasize the specific
homotopy).
Ahomotopydefinesaone-parameterfamilyofmapsH (x)=H(x,t)for
t
0≤t≤1 (Figure 7.1), and condition (7.1) says that H0 =f and H1 =g.
We usually think of the parameter t as time, and think of H as giving
a “deformation” of f into g as t goes from 0 to 1. The continuity of H
guarantees that this deformation proceeds continuously without breaks or
jumps.
Lemma 7.1. For any topological spaces X and Y, homotopy is an equiv-
alence relation on the set of all continuous maps from X to Y.
Proof. Anymapf ishomotopictoitselfviathetrivialhomotopyH(x,t)=
f(x), so homotopy is reflexive. Similarly, if H: f (cid:25) g, then a homotopy
from g to f is given by H (cid:7) (x,t) = H(x,1−t), so homotopy is symmetric.
Finally, if F: f (cid:25)g and G: g (cid:25)h, define H: X×I →Y by following F at

---

Homotopy 149
f1
Y
X×I H
f0
FIGURE 7.1. A homotopy between f0 and f1.
double speed for 0 ≤ t ≤ 1, and then following G at double speed for the
2
remainder of the unit interval. Formally,
(cid:16)
F(x,2t), 0≤t≤ 1;
H(x,t)= 2
G(x,2t−1), 1 ≤t≤1.
2
Since F(x,1) = g(x) = G(x,0), the two definitions of H agree at t =
1, where they overlap. Thus H is continuous by the gluing lemma, and
2
is therefore a homotopy between f and h. This shows that homotopy is
transitive.
Lemma 7.2. The homotopy relation is preserved by composition: If
f0,f1: X →Y and g0,g1: Y →Z
are continuous maps with f0 (cid:25)f1 and g0 (cid:25)g1, then g0 ◦f0 (cid:25)g1 ◦f1.
Proof. SupposeF: f0 (cid:25)f1 andG: g0 (cid:25)g1 arehomotopies.DefineH: X×
I → Z by H(x,t) = G(F(x,t),t). At t = 0, H(x,0) = G(f0(x),0) =
g0(f0(x)), and at t = 1, H(x,1) = G(f1(x),1) = g1(f1(x)). Thus H is a
homotopy from g0 ◦f0 to g1 ◦f1.
Example 7.3. Define maps f: R→R2 by
f(x)=(x,x2); g(x)=(x,x).
Then the map H(x,t)=(x,x2−tx2+tx) is a homotopy from f to g.
Example 7.4. Let B ⊂ Rn and let X be any topological space. Suppose
f,g: X → B are any two continuous maps with the property that for all

---

150 7. Homotopy and the Fundamental Group
Rn
X×I
B
FIGURE 7.2. A straight-line homotopy.
x∈X, the line segment from f(x) to g(x) lies in B. This will be the case,
forexample,ifB isconvex.DefineahomotopyH: f (cid:25)g bylettingH(x,t)
trace out the line segment from f(x) to g(x) at constant speed as t goes
from 0 to 1 (Figure 7.2):
H(x,t)=(1−t)f(x)+tg(x).
This is called the straight-line homotopy between f and g. It shows, in
particular,thatallmapsfromagivenspaceintoaconvexsetarehomotopic.
The Fundamental Group
Recall that a path in a topological space X is a continuous map f: I →X.
The points p=f(0) and q =f(1) are called the initial point and terminal
point of f, respectively, and we say that f is a path “from p to q.” We will
use paths to detect “holes” in a space.
Example 7.5. Consider the path α: I → R2 (cid:3){0} defined (in complex
notation) by
α(s)=e2πis
and the map H: I×I →R2(cid:3){0} by
H(s,t)=e2πist.
Ateachtimet,H isapaththatfollowsthecircleonlyasfarasangle2πt,
t
so H0 is the constant path c1(s) ≡ 1 and H1 = α. Thus H is a homotopy
from the constant path to α.

---

The Fundamental Group 151
This last example shows that the circular path around the origin is ho-
motopic in R2 (cid:3){0} to a constant path, so that simply asking whether
a closed path is homotopic to a constant is not sufficient to detect holes.
To remedy this, we will need to consider homotopies of paths throughout
whichtheendpointsstayfixed.Moregenerally,itwillbeusefultoconsider
homotopies that fix an arbitrary subset of the domain.
Let X and Y be topological spaces, and A ⊂ X an arbitrary subspace.
A homotopy H between maps f,g: X → Y is called a homotopy relative
to A if
H(x,t)=f(x) for all x∈A, t∈I.
In other words, for each t, the map H agrees with f on A. If there exists
t
such a homotopy, we say that f and g are homotopic relative to A and
write f (cid:25)
A
g. Notice that this implies g|
A
=H1 |
A
=f|
A
, so for two maps
to be homotopic relative to A they must first of all agree on A.
Nowsupposef andg aretwopathsinX.Apathhomotopyfromf tog is
a homotopy relative to {0,1}, that is, a homotopy that fixes the endpoints
for all time. If there exists a path homotopy between f and g, we say they
are path homotopic, and write f ∼g. By the remark above, this is possible
only if f and g both have the same initial point and the same terminal
point.
Lemma 7.6. For any points p,q ∈ X, path homotopy is an equivalence
relation on the set of all paths from p to q.
Exercise 7.1. Prove Lemma 7.6.
For any path f in X, we denote the path homotopy equivalence class of
f by [f], and call it the path class of f. For our purposes, we will be most
interested in paths that start and end at the same point. Such a path is
calledaloop.Iff isaloopwhoseinitialandterminalpointisq ∈X,wesay
that f is based at q, and we call q the base point of f. The set of all loops
in X based at q is denoted by Ω(X,q). The constant loop c ∈ Ω(X,q) is
q
the map c (s) ≡ q. If a loop is path homotopic to the constant loop, we
q
say that it is null homotopic.
One (not very interesting, but sometimes useful) way to get homotopic
pathsisbythefollowingconstruction.Areparametrizationofapathf: I →
X is a path of the form f ◦ϕ for some homeomorphism ϕ: I →I fixing 0
and 1.
Lemma 7.7. Any reparametrization of a path f is path homotopic to f.
Proof. Suppose f ◦ϕ is a reparametrization of f, and let H: I ×I → I
denote the straight-line homotopy from the identity map to ϕ. Then f◦H
is a homotopy from f to f ◦ϕ.

---

152 7. Homotopy and the Fundamental Group
t
f1 g1 f1 g1
H
F G f0
g0
s
f0 g0
FIGURE 7.3. Homotopy invariance of path multiplication.
Lemma 7.6 says that path homotopy is an equivalence relation on
Ω(X,q). We define the fundamental group of X based at q, denoted by
π1(X,q), to be the set of path classes of loops based at q.
Tomakeπ1(X,q)intoagroup,wemustdefineamultiplicationoperation.
This is done first on the level of paths: The product of two paths f and
g is the path obtained by first following f and then following g, both at
double speed. For future use, we will define products of paths in a more
general setting—instead of requiring that both paths start and end at the
samepoint,wewillrequiresimplythatthesecondonestartwherethefirst
ends.
Thus let f,g: I →X be paths with f(1)=g(0). We define their product
·
f g: I →X by
(cid:16)
f · g(s)= f(2s); 0≤s≤ 1 2 ;
g(2s−1); 1 ≤s≤1.
2
(Here and throughout the book we will consistently use s as the “space
variable” parametrizing individual paths, and reserve t for the “time vari-
·
able” in homotopies.) The condition f(1) = g(0) guarantees that f g is
continuous by the gluing lemma.
Lemma 7.8 (Homotopy Invariance of Path Multiplication). Path
multiplicationiswell-definedonpathclasses.Moreprecisely,iff0 ∼f1 and
· ·
g0 ∼ g1, and if f0 g0 is defined (that is, if f0(1) = g0(0)), then f1 g1 is
· ·
also defined and f0 g0 ∼f1 g1.
Proof. Let F: f0 ∼ f1 and G: g0 ∼ g1 be homotopies (Figure 7.3). The
· ·
required homotopy H: f0 g0 ∼f1 g1 is given by
(cid:16)
F(2s,t); 0≤s≤ 1, 0≤t≤1;
H(s,t)= 2
G(2s−1,t); 1 ≤s≤1, 0≤t≤1.
2

---

The Fundamental Group 153
t
t
c p f −1
f f
p
s s
c
f p
FIGURE 7.4. f ∼cp · f. FIGURE 7.5. cp ∼f · f−1.
Again, this is continuous by the gluing lemma.
Withthisresult,itmakessensetodefinemultiplicationofpathclassesby
· · ·
setting [f] [g]=[f g] whenever f g is defined. In particular, it is always
defined for [f],[g] ∈ π1(X,q). We wish to show that π1(X,q) is a group
under this multiplication, which amounts to proving associativity of path
class multiplication and the existence of an identity and inverses. Again, it
will be useful to prove these properties in a slightly more general setting,
forpathsthatdonotnecessarilyhavethesameinitialandterminalpoints.
For any path f, we define the reverse path f−1 by f−1(s)=f(1−s); this
just retraces f from its terminal point to its initial point. Recall that c
q
denotes the constant loop at q.
Theorem 7.9 (Properties of Path Multiplication). Let f be any
path from p to q in a space X, and let g and h be any paths in X. Path
multiplication satisfies the following properties:
· ·
(a) [c ] [f]=[f] [c ]=[f].
p q
(b) [f] · [f−1]=[c ]; [f−1] · [f]=[c ].
p q
· · · ·
(c) [f] ([g] [h])=([f] [g]) [h] whenever either side is defined.
·
Proof. For(a),letusshowthatc f ∼f;theproducttheotherwayworks
p
similarly. Define H: I×I →X (Figure 7.4) by
⎧
⎨p,(cid:20)
(cid:21)
t≥2s;
H(s,t)= 2s−t
⎩f , t≤2s.
2−t
Geometrically, this maps the portion of the square on the left of the line
t = 2s to the point p, while it maps the portion on the right along the
path f at increasing speeds as t goes from 0 to 1. (The slanted lines in the
picture are the level sets of H, i.e., the lines along which H takes the same

---

154 7. Homotopy and the Fundamental Group
value.) This map is continuous by the gluing lemma, and you can check
· ·
that H(s,0)=f(s) and H(s,1)=c f(s). Thus H: f ∼c f.
p p
For(b),wewilljustshowthatf · f−1 ∼c .Since(f−1)−1 =f,theother
p
relationfollowsbyinterchangingtherolesoff andf−1.Defineahomotopy
H: c ∼ f · f−1 by the following recipe (Figure 7.5): At any time t, the
p
path H follows f as far as f(t) at double speed while the parameter s is
t
in the interval [0,t/2]; then for s ∈ [t/2,1−t/2] it stays at f(t); then it
retraces f at double speed back to q. Formally,
⎧
⎪⎨f(2s), 0≤s≤t/2;
H(s,t)= f(t), t/2≤s≤1−t/2;
⎪⎩
f(2−2s) 1−t/2≤s≤1.
It is easy to check that H is a homotopy from c to f · f−1.
p
· · · ·
Finally,toproveassociativity,weneedtoshowthat(f g) h∼f (g h).
The first path follows f and then g at quadruple speed for s ∈ [0,1], and
2
then follows h at double speed for s ∈ [1,1], while the second follows f
2
at double speed and then g and h at quadruple speed. The two paths are
therefore reparametrizations of each other and thus homotopic.
Corollary 7.10. For any space X and any point q ∈ X, π1(X,q) is a
group.
Note that path multiplication is not associative on the level of paths,
onlyonthelevelofpathhomotopyclasses.Fordefiniteness,letusagreeto
interpret products of more than two paths as being grouped from left to
· · · ·
right if no parentheses are present, so that f g h means (f g) h.
The next question we need to address is how the fundamental group
depends on the choice of base point. The first thing to notice is that if
X is not path connected, we cannot expect the fundamental groups based
at points in different path components to have any relationship to each
other; π1(X,q) can give us information only about the path component
containing q. Therefore, the fundamental group is usually used only to
study path connected spaces. When X is path connected, it turns out that
the fundamental groups at different points are all isomorphic; the next
theorem gives an explicit isomorphism between them.
Theorem 7.11 (Change of Base Point). Suppose X is path con-
nected, p,q ∈ X, and g is any path from p to q. The map Φ
g
: π1(X,p) →
π1(X,q) defined by
Φ [f]=[g−1] · [f] · [g]
g
is an isomorphism.
Proof. Beforewebegin,weshouldverifythatΦ makessense(Figure7.6):
g

---

The Fundamental Group 155
f
g
q
p
FIGURE 7.6. Change of base point.
Since g goes from p to q and f goes from p to p, paths in the class [g−1] ·
[f] · [g] go from q to p (by g−1), then from p to p (by f), and then from p
back to q (by g), so Φ
g
(f) does indeed define an element of π1(X,q).
To check that Φ is a group homomorphism, use Theorem 7.9:
g
·
Φ
g
[f1] Φ
g
[f2]
=[g−1] · [f1] · [g] · [g−1] · [f2] · [g]
=[g−1] · [f1] · [c
p
] · [f2] · [g]
=[g−1] · [f1] · [f2] · [g]
·
=Φ
g
([f1] [f2]).
(This is one reason why we needed to prove the properties of Theorem 7.9
for paths that start and end at different points.)
Finally, the fact that Φ is an isomorphism follows easily from the fact
g
that it has an inverse, given by Φ
g−1
: π1(X,q)→π1(X,p).
Because of this theorem, when X is path connected we sometimes use
the imprecise notation π1(X) to refer to the fundamental group of X with
respect to an unspecified base point, if the base point is irrelevant. For ex-
ample, we might say “π1(X) is trivial” if π1(X,q)={[c
q
]} for any q ∈X;
or we might say “π1(X) ∼ =Z” if there exists an isomorphism π1(X,q)→Z
for some (hence any) q. However, we cannot dispense with the base point
altogether: Since different paths from p to q may give rise to different iso-
morphisms,whenweneedtorefertoaspecificelementofthefundamental
group, or to a specific homomorphism between fundamental groups, we
must be careful to specify all base points.

---

156 7. Homotopy and the Fundamental Group
X
k
g
I×I
F h
f
FIGURE 7.7. The map of Lemma 7.12.
If X is path connected and π1(X) is trivial, we say that X is simply
connected. This means that every loop in X can be continuously shrunk to
a constant loop while its endpoints are kept fixed.
Exercise 7.2. Let X be a topological space.
(a) Letf,g: I →X betwopathsfromptoq.Showthatf ∼gifandonly
·
if f g−1 ∼cp.
(b) Show that X is simply connected if and only if any two paths in X
with the same initial and terminal points are path homotopic.
Exercise 7.3. Show that any convex subset of Rn is simply connected.
In particular, Exercise 7.3 shows that the plane is simply connected. We
will see later that the punctured plane is not, thus proving that the two
spacesarenothomeomorphic.In fact,wewillshowthatbothR2(cid:3){0}and
S1 have infinite cyclic fundamental groups, generated by the path class of
a loop that winds once around the origin. The proof will occupy most of
our efforts for the remainder of this chapter and the next.
Lemma 7.12. Let F: I ×I → X be a continuous map, and let f, g, h,
and k be the paths in X defined by
f(s)=F(s,0);
g(s)=F(1,s);
h(s)=F(0,s);
k(s)=F(s,1).
· ·
(See Figure 7.7.) Then f g ∼h k.
Exercise 7.4. Prove Lemma 7.12.
Considernowtheloopα: I →S1 givenbyα(s)=e2πis.Thismapwraps
the interval once around the circle counterclockwise, and maps 0 and 1 to

---

The Fundamental Group 157
f
0 1
X
α
q
1
(cid:7)
f
FIGURE 7.8. The circle representative of a loop.
the base point 1 ∈ S1. By the closed map lemma, it is a quotient map. If
f: I → X is any loop in a space X, it passes to the quotient to give a
unique map f (cid:7) : S1 → X such that f (cid:7)◦α = f (Figure 7.8), which we call
(cid:7)
the circle representative of f. Conversely, any continuous map f from the
circle to X is the circle representative of the map f =f
(cid:7)◦α.
The next proposition gives a convenient criterion for detecting null ho-
motopic loops in terms of their circle representatives.
Proposition 7.13. A loop in a space X is null homotopic if and only if
its circle representative extends to a map from the closed disk into X.
Proof. Let f: I → X be a loop based at q ∈ X, and f (cid:7) : S1 → X its circle
representative. Suppose first that f (cid:7) extends to a map F: B2 → X. Since
B2 isconvex,theloopαisnullhomotopicwhenthoughtofasaloopinB2.
Let A: I ×I → B2 be a path homotopy from α to the constant loop c1.
BecauseA(s,t)∈S1 whent=0or1,thecompositemapF◦A: I×I →X
satisfies
F ◦A(s,0)=f (cid:7)◦A(s,0)=f (cid:7)◦α(s)=f(s),
F ◦A(s,1)=f (cid:7)◦A(s,1)=f (cid:7)◦c1(s)=f(1)=q,
and is therefore a homotopy from f to c .
q
Conversely, suppose f is null homotopic, and let H: I ×I → X be a
homotopy from c to f. Observe that H sends the sides and bottom of the
q
square to the point q. We will show below that there is a quotient map
π: I × I → B2 that sends these three sides to 1 ∈ S1, makes no other
identifications, and restricts to α on the top side I ×{1}. Granting this
for the moment, the homotopy H passes to the quotient to give a map

---

158 7. Homotopy and the Fundamental Group
b
a b c
A B C
h
h
d e
a d e c
FIGURE7.9.Aquotientmapsendingthreesidesofthesquaretoapoint.
H (cid:7) : B2 → X satisfying H (cid:7) ◦π = H. The restriction of H (cid:7) to the circle is
(cid:7)
clearly the circle representative of f, so H is the desired extension.
We will construct the claimed quotient map π: I ×I → B2 in several
steps.LetT beanequilateraltriangleofaltitude2intheplane.Triangulate
I×I and T as shown in Figure 7.9, and let A: I×I →T be the simplicial
homeomorphismdeterminedbytheindicatedvertexmap.ThenletB: T →
B2 be the (nonsimplicial) map that sends each horizontal line segment in
T linearly onto the horizontal segment at the same height in the disk. The
resultingcompositemapB◦Aisaquotientmapbytheclosedmaplemma,
and it identifies the sides and bottom of the square to a point but makes
no other identifications. It is not quite the map we are seeking, because it
takes the sides and bottom to −i instead of 1, and maps the top interval
around the circle in the wrong direction. A suitable rotation and reflection
of the disk, which we denote by C, corrects these problems. Let β: I →S1
denotetherestrictionofC◦B◦AtothetopsegmentI×{1}ofthesquare
(identified with I). Although β is still not equal to α, the two maps differ
only by a homeomorphism of S1 (since both α and β are quotient maps
that make the same identifications). This homeomorphism extends to a
homeomorphism of the closed disk by Problem 4-9, and composing with
the inverse of this homeomorphism yields the desired map.
Homomorphisms Induced by Continuous Maps
Inthissectionweexploretheeffectofacontinuousmaponthefundamental
groups of its domain and range. The first thing we need to know is that
continuous maps preserve the path homotopy relation.
Lemma 7.14. The path homotopy relation is preserved by composition
with continuous maps. That is, if f0,f1: I → X are path homotopic and
ϕ: X →Y is continuous, then ϕ◦f0 and ϕ◦f1 are path homotopic.
Exercise 7.5. Prove Lemma 7.14

---

Homomorphisms Induced by Continuous Maps 159
An immediate consequence of this lemma is that any continuous map
ϕ: X → Y induces a well-defined map ϕ∗: π1(X,q) → π1(Y,ϕ(q)) simply
by setting ϕ∗[f]=[ϕ◦f].
Lemma 7.15. For any continuous map ϕ, ϕ∗ is a group homomorphism.
Proof. Just note that
· · ·
ϕ∗([f] [g])=ϕ∗[f g]=[ϕ◦(f g)].
· ·
Thusitsufficestoshowthatϕ◦(f g)=(ϕ◦f) (ϕ◦g).Thisisimmediate,
because expanding both sides using the definition of path multiplication
results in identical formulas.
The homomorphism ϕ∗: π1(X,q) → π1(Y,ϕ(q)) is called the homomor-
phism induced by ϕ. It has the following properties:
Proposition 7.16 (Properties of the Induced Homomorphism).
(a) Let ϕ: X →Y and ψ: Y →Z be continuous maps. Then (ψ◦ϕ)∗ =
ψ∗ ◦ϕ∗.
(b) If Id : X →X denotes the identity map of X, then for any q ∈X,
X
(Id
X
)∗ is the identity map of π1(X,q).
Proof. Compute:
ψ∗(ϕ∗[f])=ψ∗[ϕ◦f]=[ψ◦ϕ◦f]=(ψ◦ϕ)∗[f];
(Id
X
)∗[f]=[Id
X
◦f]=[f].
Corollary 7.17 (Topological Invariance of π 1). Homeomorphic
spaces have isomorphic fundamental groups. Specifically, if ϕ: X → Y is
a homeomorphism, then ϕ∗: π1(X,q)→π1(Y,ϕ(q)) is an isomorphism.
Proof. Ifϕisahomeomorphism,then(ϕ−1)∗ ◦ϕ∗ =(ϕ−1◦ϕ)∗ =(Id
X
)∗ =
Id π1(X,q), and similarly ϕ∗ ◦(ϕ−1)∗ is the identity on π1(Y,ϕ(q)).
Be warned that injectivity or surjectivity of a continuous map does not
necessarily imply that the induced homomorphism has the same property.
Forexample,acceptingforthemomentthefactthatπ1(S1)isinfinitecyclic
(we will prove it in the next chapter), the inclusion map S1 (cid:9)→R2 is injec-
tive, but its induced homomorphism is not, while the map ϕ: [0,1) → S1
of Exercise 2.7 that wraps the interval once around the circle is surjective
(infactbijective),butitsinducedhomeomorphismisthetrivialhomomor-
phism because [0,1) is convex and therefore simply connected.

---

160 7. Homotopy and the Fundamental Group
B
E
A
FIGURE 7.10. S1 is a retract of T2. FIGURE 7.11. Figure eight space.
There is, however, one case in which the homomorphism induced by
inclusion can be easily shown to be injective. Let X be a space and A ⊂
X a subspace. A continuous map r: X → A is called a retraction if the
restrictionofrtoAistheidentitymapofA,orequivalentlyifr◦ι =Id ,
A A
where ι : A(cid:9)→X is the inclusion map. If there exists a retraction from X
A
to A, we say that A is a retract of X.
Proposition 7.18. Suppose A is a retract of X. If r: X → A is any
retraction, then for any q ∈A, (ι
A
)∗: π1(A,q)→π1(X,q) is injective and
r∗: π1(X,q)→π1(A,q) is surjective.
Proof. Sincer◦ι
A
=Id
A
, r∗ ◦(ι
A
)∗ istheidentityon π1(A,q),fromwhich
it follows that (ι
A
)∗ is injective and r∗ is surjective.
Here are some examples of retractions. For these examples we will use
without proof the fact that the fundamental group of the circle is infinite
cyclic.
Example 7.19. It is easy to check that the map r: Rn+1 (cid:3) {0} → Sn
given by r(x) = x/|x| is a retraction. Thus the homomorphism π1(Sn) →
π1(Rn+1(cid:3){0}) induced by inclusion is injective. In particular, in the case
n=1, this means that π1(R2(cid:3){0}) has an infinite cyclic subgroup.
Example 7.20. The torus T2 = S1 ×S1 has a subspace A = S1 ×{1}
homeomorphic to S1 (Figure 7.10), and the map r: T2 → A given by
r(p,q) = (p,1) is easily seen to be a retraction. Thus the image of the
map (ι
A
)∗: π1(S1)→π1(T2) is an infinite cyclic subgroup of π1(T2).
Example 7.21. Consider the figure eight space E ⊂ R2 (Figure 7.11),
which is the union of the circles of radius 1 around (0,1) and (0,−1).
Let B denote the upper circle. There are at least two different retractions
of E onto B—one that maps the entire lower circle to the origin and is the
identityonB,andanotherthat“folds”thelowercircleontotheupperone
(formally, (x,y)(cid:10)→(x,|y|)). Thus π1(E) has an infinite cyclic subgroup.

---

Homotopy Equivalence 161
Homotopy Equivalence
Although retractions are sometimes useful tools for showing that a certain
fundamental group is not trivial, it is much more useful to have a criterion
under which a continuous map induces an isomorphism of fundamental
groups. In this section we explore a very general such criterion.
Let ϕ: X → Y be a continuous map. We say that another continuous
mapψ: Y →X isahomotopy inverseforϕifψ◦ϕ(cid:25)Id andϕ◦ψ (cid:25)Id .
X Y
Ifthereexistsahomotopyinverseforϕ,ϕiscalledahomotopyequivalence.
Inthiscase,wesaythatX ishomotopy equivalenttoY,orX hasthesame
homotopy type as Y, and we write X (cid:25)Y.
Lemma 7.22. Homotopy equivalence is an equivalence relation.
Exercise 7.6. Prove Lemma 7.22.
One kind of homotopy equivalence is relatively easy to visualize. A sub-
space A ⊂ X is said to be a deformation retract of X if there exists a
retraction r: X → A such that the identity of X is homotopic to ι ◦r.
A
The homotopy H: Id (cid:25) ι ◦r is called a deformation retraction. Intu-
X A
itively, this means that X can be continuously deformed into A in such a
way that points in A end up where they started. We say that A is a strong
deformation retract of X if in addition Id (cid:25) (ι ◦r), which means that
X A A
points in A remain fixed throughout the deformation. In this case, the
homotopy H can be called a strong deformation retraction.
Example 7.23. InExample7.19weshowedthatSn isaretractofRn+1(cid:3)
{0}. In fact, it is a strong deformation retract: The deformation retraction
is given by H: (Rn+1(cid:3){0})×I →Rn+1(cid:3){0}, where
x
H(x,t)=(1−t)x+t .
|x|
Thisisjustthestraight-linehomotopyfromtheidentitymaptotheretrac-
tion onto the sphere (Figure 7.12).
If A is a deformation retract of X, since ι ◦r (cid:25)Id and r◦ι =Id ,
A X A A
the inclusion A(cid:9)→X is a homotopy equivalence.
Our main goal in this section is the following theorem, which is a much
strongerinvariancepropertythanhomeomorphisminvariance,andwillen-
able us to compute the fundamental groups of many more spaces.
Theorem 7.24 (Homotopy Invariance of π 1). If ϕ: X →Y is a ho-
motopy equivalence, then for any point q ∈X, ϕ∗: π1(X,q)→π1(Y,ϕ(q))
is an isomorphism.
Before proving the theorem, let us look at several important examples.
Example 7.25. Let X be any space. If the identity map of X is homo-
topic to a constant map, we say that X is contractible. Other equivalent

---

162 7. Homotopy and the Fundamental Group
FIGURE 7.12. Strong deformation retraction of R2(cid:3){0} onto S1.
definitions are that any point of X is a deformation retract of X, or X is
homotopy equivalent to a one-point space (Exercise 7.7). Concretely, con-
tractibility means that there exists a continuous map H: X×I →X such
that
H(x,0)=x for all x∈X; H(x,1)=q for all x∈X.
In other words, the whole space X can be continuously shrunk to a point.
Some obvious examples of contractible spaces are convex subsets of Rn,
and, more generally, any subset B ⊂ Rn that is star-shaped, which means
thatthereissomepointq0 ∈B suchthatforeveryq ∈B,thelinesegment
fromq0 toq iscontainedinB.Sinceaone-pointspaceissimplyconnected,
it follows that every contractible space is simply connected.
Exercise 7.7. Show that the following are equivalent:
(a) X is contractible.
(b) X is homotopy equivalent to a one-point space.
(c) Any point of X is a deformation retract of X.
Example 7.26. Example 7.23 showed that the circle is a strong deforma-
tion retract of R2 (cid:3){0}. Therefore, inclusion S1 (cid:9)→ R2 (cid:3){0} induces an
isomorphism of fundamental groups. Once we show that π1(S1) is infinite
cyclic, this will characterize π1(R2(cid:3){0}) as well.
Example 7.27. The figure eight space E of Example 7.21 and the theta
space, defined by
Θ={(x,y)∈R2 :x2+y2 =4, or y =0 and −2≤x≤2},

---

Homotopy Equivalence 163
FIGURE 7.13. Deformation retractions onto E and Θ.
FIGURE 7.14. A tree. FIGURE 7.15. Not a tree.
are both strong deformation retracts of R2 with the two points (0,1) and
(0,−1) removed. The deformation retractions, indicated schematically in
Figure 7.13, are defined by carving the space up into regions in which
straight-line homotopies are easily defined; the resulting maps are con-
tinuous by the gluing lemma. Therefore, since homotopy equivalence is
transitive, E and Θ are homotopy equivalent to each other.
Example 7.28 (Finite Trees). LetΓbeagraph.AcycleinΓisaclosed
finiteedgepath,thatis,anedgepath(v0,…,v
n
)suchthatv0 =v
n
.Atree
is a connected graph that contains no reduced cycles (see Figures 7.14 and
7.15). We will show that any finite tree T is contractible and thus simply
connected.
TheproofisbyinductiononthenumberofedgesinT.Ifthereisonlyone
edge,thenT ishomeomorphictoaclosedintervalinR,whichisconvexand
therefore contractible. So suppose every tree with n edges is contractible,
and let T be a tree with n+1 edges.

---

164 7. Homotopy and the Fundamental Group
v1 v0
T0
FIGURE 7.16. Proof that a tree is contractible.
IfeveryvertexinT liesonatleasttwoedges,thenarguingasintheproof
of the classification theorem for 1-manifolds (Theorem 6.1), there must be
an infinite reduced edge path {v : i ∈ Z} in T. Because T is finite, there
i
mustbesomeintegersnandn+k >nsuchthatv n =v n+k .Ifnandk are
chosen so that k is the minimum positive integer with this property, this
meansthat(v n ,…,v n+k )isareducedcycle,contradictingtheassumption
thatT isatree.Thustheremustbeatleastonevertexv0 thatliesononly
one edge. Since T is connected, v0 lies on exactly one edge, say (cid:22)v0,v1 (cid:23).
LetT0 denotethesubgraphofT withthevertexv0 andtheedge(cid:22)v0,v1 (cid:23)
deleted (Figure 7.16). The straight-line homotopy defines a strong defor-
mation retraction of (cid:22)v0,v1 (cid:23) onto v1; extending this to be the identity on
T0 yieldsastrongdeformationretractionofT ontoT0,whichiscontinuous
becauseitsrestrictiontoeachsimplexiscontinuous.Therefore,T ishomo-
topy equivalent to T0, which is contractible by the induction hypothesis.
Now we turn to the proof of Theorem 7.24. Roughly speaking, we would
like to prove the theorem by showing that if ψ is a homotopy inverse for
ϕ, then ψ◦ϕ(cid:25)Id
X
implies that ψ∗ ◦ϕ∗ is the identity map, and similarly
forϕ∗ ◦ψ∗.Thiswouldrequireustoshowthathomotopicmapsinducethe
samefundamentalgrouphomomorphisms.However,thereisanimmediate
problemwiththisapproach:IftwomapsF0 andF1 arehomotopic,wehave
no guarantee that both maps take the base point q ∈X to the same point
in Y, so their induced homomorphisms do not even map into the same
group!
The following rather complicated-looking lemma is a substitute for the
claimthathomotopicmapsinducethesamefundamentalgrouphomomor-
phism. It says, in effect, that homotopic maps induce the same homomor-
phism up to a canonical change of base point.
Lemma 7.29. Suppose ϕ,ψ: X → Y are continuous, and H: ϕ (cid:25) ψ is a
homotopy. For any q ∈X, let h be the path in Y from ϕ(q) to ψ(q) defined
by h(t) = H(q,t). Let Φ
h
: π1(Y,ϕ(q)) → π1(Y,ψ(q)) be the isomorphism

---

Homotopy Equivalence 165
ψ◦f
ψ
ψ(q) Y
h
H ◦f
H h(t) t
I
ϕ(q)
q f ϕ◦f
X ϕ
FIGURE 7.17. Induced homomorphisms of homotopic maps.
defined in Theorem 7.11. Then the following diagram commutes:
π1(Y,ϕ(q))
(cid:3)(cid:4)
ϕ∗ (cid:3)
(cid:3)
π1(X,q) Φ
h
(cid:6)
ψ∗ (cid:6)
(cid:6)(cid:7) (cid:5)
π1(Y,ψ(q)).
Proof. Let f be any loop in X based at q. What we need to show is
ψ∗[f]=Φ
h
(ϕ∗[f])
⇐⇒ ϕ∗[f]=Φ
h−1
(ψ∗[f])
⇐⇒ [ϕ◦f]=[h] · [ψ◦f] · [h−1]
⇐⇒ ϕ◦f ∼h · (ψ◦f) · h−1.
Atanytimet,themapH ◦f isaloopbasedath(t)(Figure7.17).Thus
t
we can define a homotopy G from ϕ◦f to h · (ψ◦f) · h−1 by letting G
t
be the “lasso-shaped” loop that first follows h as far as h(t), then follows
H ◦f at triple speed, then follows h back to ϕ(q). Formally,
t
⎧
⎪⎨h(3ts), 0≤s≤ 1,
3
G(s,t)= H(f(3s−1),t), 1 ≤s≤ 2,
⎪⎩ 3 3
h(3t(1−s)), 2 ≤s≤1.
3

---

166 7. Homotopy and the Fundamental Group
It is straightforward to check that G is continuous by the gluing lemma.
· ·
T ho h m e o p t a o t p h ic G t 0 o i ϕ s ◦ a f re ; p a a n r d am G e 1 tr is iz a at r io ep n a o r f am c ϕ e ( t q r ) iza ( t ϕ io ◦ n f o ) f h c ·ϕ( ( q ψ ), ◦ w f h ) ic · h h− is 1. path
Proof of Theorem 7.24. Suppose ϕ: X → Y is a homotopy equivalence,
and let ψ: Y →X be a homotopy inverse for it. Consider the sequence of
maps
π1(X,q)−ϕ→∗ π1(Y,ϕ(q))−ψ→∗ π1(X,ψ(ϕ(q)))−ϕ→∗
π1(Y,ϕ(ψ(ϕ(q)))). (7.2)
We need to prove that the first ϕ∗ above is bijective. As we mentioned
earlier, ψ∗ is not an inverse for it, because it does not map into the right
space.
Since ψ◦ϕ(cid:25)Id , Lemma 7.29 shows that there is a path h in X such
X
that the following diagram commutes:
π1(X,q)
(cid:3)(cid:4)
Id (cid:3)
(cid:3)
π1(X,q) Φ
h
(cid:6)
ψ∗ ◦ϕ∗ (cid:6)
(cid:6)(cid:7) (cid:5)
π1(X,ψ(ϕ(q))). (7.3)
Thusψ∗ ◦ϕ∗ =Φ
h
,whichisanisomorphism.Inparticular,thismeansthat
the first ϕ∗ in (7.2) is injective and ψ∗ is surjective.
Similarly, the homotopy ϕ◦ψ (cid:25)Id leads to the diagram
Y
π1(Y,ϕ(q))
(cid:3)(cid:4)
Id (cid:3)
(cid:3)
π1(Y,ϕ(q)) Φ
k
(cid:6)
ϕ∗ ◦ψ∗ (cid:6)
(cid:6)(cid:7) (cid:5)
π1(Y,ϕ(ψ(ϕ(q)))),
from which it follows that ϕ∗ ◦ψ∗: π1(Y,ϕ(q)) → π1(Y,ϕ(ψ(ϕ(q)))) is an
isomorphism.Thismeansinparticularthatψ∗ isinjective;sincewealready
showed that it is surjective, it is an isomorphism. Therefore, going back to
(7.3), we conclude that ϕ∗ = (ψ∗)−1 ◦Φ
h
: π1(X,q) → π1(Y,ϕ(q)) is also
an isomorphism.
Homotopy Equivalence and Deformation Retraction
In Example 7.27 we showed that the figure eight and theta spaces are
homotopy equivalent by showing that they are both deformation retracts

---

Homotopy Equivalence 167
(cid:7)
X
X×I
π
f
(cid:7)
Y
Y
Z
f
FIGURE 7.18. The mapping cylinder.
ofasinglelargerspace.Thisexampleisnotasspecialasitmightseem.As
thenextpropositionshows,twospacesarehomotopyequivalentifandonly
if both are homeomorphic to deformation retracts of a single larger space.
This gives a rather concrete way to think about homotopy equivalence.
Let X and Y be topological spaces, and let f: X → Y be a continuous
map. Define the mapping cylinder Z of f to be the quotient space of
f
(X ×I)(cid:20)Y by the equivalence relation generated by (x,0)∼f(x) for all
x∈X. Let π denote the quotient map. The space Z can be visualized as
f
a “top hat” (Figure 7.18) formed by gluing the “cylinder” X×I to Y (the
“brim”) by attaching each point (x,0) on the bottom of the cylinder to its
image f(x) in Y.
ThesubspaceX×{1}⊂(X×I)(cid:20)Y isasaturatedclosedsubsethomeo-
morphic to X. The restriction of π to this subset is thus a one-to-one quo-
(cid:7) (cid:7)
tientmap,soitsimageX isalsohomeomorphictoX.Similarly,Y =π(Y)
is homeomorphic to Y.
Proposition 7.30. With notation as above, if f is a homotopy equiva-
(cid:7) (cid:7)
lence, then Y and X are deformation retracts of Z . Thus two spaces are
f
homotopy equivalent if and only if they are both homeomorphic to defor-
mation retracts of a single space.
Proof. For any (x,s) ∈ X ×I, let [x,s] = π(x,s) denote its equivalence
class in Z ; similarly, [y]=π(y) is the equivalence class of y ∈Y.
f
(cid:7)
FirstweshowthatY isastrongdeformationretractofZ ,assumingonly
f
that f is continuous. We define a retraction A: Z → Z , which collapses
f f

---

168 7. Homotopy and the Fundamental Group
f G
F
g
H1 H2 H3
FIGURE 7.19. Homotopies of the mapping cylinder.
(cid:7)
Z down onto Y, by
f
A[x,s]=[x,0];
A[y]=[y].
To be a bit more precise, we should define a map A (cid:7) : (X×I)(cid:20)Y →Z by
f
(cid:7) (cid:7)
A(x,s)=[x,0]andA(y)=[y].Thismapisevidentlycontinuousbecauseits
restrictions to X×I and Y are compositions of continuous maps. Because
(cid:7) (cid:7) (cid:7)
A(x,0)=[f(x)]=A(f(x)), A respects the identifications made by π, so it
passes to the quotient to yield the continuous map A defined above. This
kind of standard argument will be used repeatedly to show that a map
from Z is continuous; we will generally abbreviate it by saying something
f
like “A is well-defined and continuous because A[x,0]=[f(x)]=A[f(x)].”
Define a homotopy H1: Z
f
×I →Z
f
(Figure 7.19) by
H1([x,s],t)=[x,s(1−t)];
H1([y],t)=[y].
Because H1([x,0],t) = [x,0] = [f(x)] = H1([f(x)],t), H1 is well-defined.
To check that it is continuous, we need only observe that it respects the
identificationsmadebythemapπ×Id: ((X×I)(cid:20)Y)×I →Z ×I,which
f
is a quotient map by Lemma 4.35. Since H1(ζ,0)=ζ and H1(ζ,1)=A(ζ)
for any ζ ∈ Z
f
, H1 is a homotopy between the identity map of Z
f
and
A. Since, moreover, H1([y],t) = [y] for all y ∈ Y, it is in fact a strong
deformation retraction.
Now suppose f is a homotopy equivalence, and let g: Y → X be a
homotopy inverse for it. Thus there exist homotopies F: Y ×I → Y and
G: X ×I → X such that F: f ◦g (cid:25) Id and G: g◦f (cid:25) Id . Define two
Y X

---

Higher Homotopy Groups 169
more homotopies H2 and H3 by
H2([x,s],t)=[F(f(x),1−t)];
H2([y],t)=[F(y,1−t)];
H3([x,s],t)=[G(x,st),t];
H3([y],t)=[g(y),t].
The straightforward verification that H2 and H3 are well-defined and con-
tinuous is left to the reader. Geometrically, H2 deforms all of Z
f
into the
(cid:7) (cid:7)
image of f in Y along the homotopy F, and then H3 collapses Z
f
onto X
by deforming each point along the homotopy G (Figure 7.19).
Inserting t=0 and t=1 into the definitions of H2 and H3, we find that
H2: A(cid:25)B and H3: B (cid:25)C, where
B[x,s]=[g(f(x)),0];
B[y]=[g(y),0];
C[x,s]=[G(x,s),1];
C[y]=[g(y),1].
Because homotopy is transitive, the three homotopies H1,H2,H3 yield
Id (cid:25) A (cid:25) B (cid:25) C. Since G(x,1) = x, we find that C[x,1] = [x,1], so
Zf
(cid:7) (cid:7)
C is a retraction onto X, which shows that X is a deformation retract of
Z .
f
Higher Homotopy Groups
You might have wondered what the subscript 1 stands for in π1(X). As
the notation suggests, the fundamental group is just one in a series of
groups associated with a topological space, all of which measure “holes”
of various dimensions. In this section we introduce the basic definitions
withoutmuchdetail,justsothatyouwillrecognizethisconstructionwhen
you see it again. We will not use this material anywhere else in the book.
The definition of the higher homotopy groups is motivated by the fact
that by identifying loops with their circle representatives as described ear-
lier in this chapter, we can regard the fundamental group π1(X,q) as the
setofequivalenceclassesofmapsfromS1 intoX taking1toq,moduloho-
motopy relative to the base point 1. Generalizing this, for any nonnegative
integer n, we define π (X,q) to be the set of equivalence classes of maps
n

---

170 7. Homotopy and the Fundamental Group
from Sn into X taking (1,0,…,0) to q, modulo homotopy relative to the
base point. Just as in the case of the fundamental group, it can be shown
that π (X,q) is a topological invariant.
n
Thesimplestcaseisn=0.SinceS0 ={±1},amapfromS0 toX sending
the base point 1 to q is determined by where it sends −1. Two such maps
are homotopic if and only if the two images of −1 lie in the same path
component of X. Therefore, π0(X,q) can be identified with the set of path
components of X. There is no canonical group structure on π0(X,q); it is
merelyasetwithadistinguishedelement(thecomponentcontainingq).It
is conventional to define π0(X) to be the set of path components without
any distinguished element.
For n > 1, π (X,q) has a multiplication operator (which we will not
n
describe here) under which it turns out to be an abelian group, called the
nthhomotopygroupofX basedatq.Thesegroupsmeasuretheinequivalent
waysofmappingSn intoX,andtellus,inasense,aboutthen-dimensional
“holes”inX.Forexample,wewillseelaterthatπ1(R3(cid:3){0})istrivial;but
it can be shown that the inclusion S2 (cid:9)→ R3(cid:3){0} represents a nontrivial
element of π2(R3(cid:3){0}).
The higher homotopy groups are notoriously hard to compute. In fact,
only a limited amount is known about π (Sn) for k much larger than n.
k
Thestructureandcomputationofthesegroupsformtheembarkationpoint
for a vast branch of topology known as homotopy theory. See [Whi78] for
an excellent introduction to the subject.
Categories and Functors
In this section we digress a bit to give a brief introduction to category
theory, a powerful idea that unifies many of the concepts we have seen so
far, and indeed much of mathematics. We will only touch on these ideas
fromtimetotimeinthisbook,butyouwillusethemextensivelyifyoudo
more advanced work in algebraic topology, so it is important to familiarize
yourself with the basic concepts.
A category C consists of the following:
- a class (not necessarily a set) of objects;
- for each pair of objects X,Y a set HomC(X,Y) of morphisms; and
- for each triple X,Y,Z of objects a function called composition:
HomC(X,Y)×HomC(Y,Z)→HomC(X,Z), written (f,g)(cid:10)→g◦f;
such that the following axioms are satisfied:
(i) Composition is associative: (f ◦g)◦h=f ◦(g◦h).

---

Categories and Functors 171
(ii) For each object X there exists an identity morphism Id ∈
X
HomC(X,X) such that for any morphism f ∈ HomC(X,Y) we have
Id ◦f =f =f ◦Id .
Y X
Therearemanyalternativenotationsinuse.ThesetHomC(X,Y)isalso
sometimes denoted by C(X,Y) or even just Hom(X,Y) if the category
in question is understood. An element f ∈ HomC(X,Y) is often written
f: X →Y.Forthemostpartyoucanthinkoftheobjectsinacategoryas
sets with some special structure and the morphisms as maps that preserve
the structure, although the definitions do not require this, and we will see
below that there are natural examples that are not of this type.
Here are some familiar examples of categories, which we describe by
specifying their objects and morphisms; the composition laws and identity
morphisms are the obvious ones.
- SET: Sets and functions.
- GROUP: Groups and group homomorphisms.
- AB: Abelian groups and group homomorphisms.
- RING: Rings and ring homomorphisms.
- CRING: Commutative rings and ring homomorphisms.
- VECT R: Real vector spaces and R-linear maps.
- VECT C: Complex vector spaces and C-linear maps.
- TOP: Topological spaces and continuous maps.
- TOP ∗:Pointed topological spaces—topologicalspacestogetherwitha
choice of base point in each—and base-point-preserving continuous
maps.
- SIMP: Abstract simplicial complexes and simplicial maps.
Ineachcase,theverificationoftheaxiomsofacategoryisstraightforward.
Themainpointistoshowthatacompositionoftheappropriatestructure-
preserving maps again preserves the structure. Associativity is automatic
because it holds for composition of maps.
InanycategoryC,amorphismf ∈HomC(X,Y)iscalledanisomorphism
if there exists a morphism g ∈ HomC(Y,X) such that f ◦g = Id
Y
and
g◦f =Id .Forexample,inSET,theisomorphismsarejustthebijections;
X
in GROUP they are the group isomorphisms; and in TOP they are the
homeomorphisms.
AsubcategoryofCisacategoryDwhoseobjectsare(someofthe)objects
of C and whose sets of morphisms are subsets of the morphisms in C, with
the composition law and identities inherited from C. A full subcategory is

---

172 7. Homotopy and the Fundamental Group
one in which HomD(X,Y)=HomC(X,Y) whenever X,Y are objects of D.
For example, AB is a full subcategory of GROUP.
The real power of category theory becomes apparent when we consider
relations between categories. Suppose C and D are categories. A covariant
functorF fromCtoDisarulethatassignstoeachobjectX inCanobject
F(X) in D, and to each morphism f ∈HomC(X,Y) an induced morphism
F(f)∈HomD(F(X),F(Y)), in such a way that composition and identities
are preserved:
F(g◦h)=F(g)◦F(h); F(Id
X
)=IdF(X).
In many cases, if the functor is understood, it is traditional to write the
induced morphism F(g) as g∗.
It is also frequently useful to consider contravariant functors, which
are defined in exactly the same way as covariant functors, except that
the induced morphisms go in the reverse direction: If g: X → Y, then
F(g): F(Y)→F(X); and the composition law becomes
F(g◦h)=F(h)◦F(g).
It is common for the morphism F(f) induced by a contravariant functor F
to be written f∗ if the functor is understood. (Note the upper star: The
use of a lower star to denote a covariant induced morphism and an upper
star to denote a contravariant one is universal.)
Here are some important examples of functors.
Example 7.31 (Covariant Functors).
- The fundamental group functor π1: TOP ∗ →GROUP assigns to each
pointed topological space (X,q) its fundamental group based at q,
and to each base-point-preserving continuous map its induced homo-
morphism. The fact that it is a covariant functor is the content of
Proposition 7.16.
- Thefunctorπ0: TOP→SETassignstoeachtopologicalspaceitsset
ofpathcomponents.Foranycontinuousmapf: X →Y,theinduced
mapf∗: π0(X)→π0(Y)justtakesapathcomponentX0 ofX to the
path component of Y containing f(X0).
- Theforgetful functor F: TOP→SETjustassignstoeachtopological
space its underlying set, and to each continuous map its underlying
set map. In fact, such a functor exists for any category whose ob-
jects are sets with some extra structure and whose morphisms are
structure-preserving maps.
- The geometric realization functor from SIMP to TOP takes an ab-
stract complex K to its geometric realization, and a simplicial map

---

Categories and Functors 173
f: K → L to the continuous map |f|: |K| → |L|. It is a functor
because of Lemma 5.5.
Example 7.32 (Contravariant Functors).
- The dual space functor from VECT R to itself assigns to each vector
space V its dual space V∗ (the vector space of linear maps V →
R), and to each linear map ϕ: V → W the dual map or transpose
ϕ∗: W∗ → V∗ defined by ϕ∗(f)x = f(ϕx). The verification of the
functorial properties can be found in most linear algebra texts.
- ThefunctorC: TOP→CRINGassignstoeachtopologicalspaceX its
commutative ring C(X) of continuous real-valued functions f: X →
R.Foranycontinuousmapϕ: X →Y,theinducedmapϕ∗: C(Y)→
C(X) is given by ϕ∗(f)=f ◦ϕ.
- If X and Z are abelian groups, the set Hom(X,Z) of group homo-
morphismsisalsoanabeliangroupunderpointwiseaddition.Weget
a contravariant functor from AB to itself by sending each group X
to the group Hom(X,Z), and each homomorphism f: X → Y to
the dual homomorphism f∗: Hom(Y,Z) → Hom(X,Z) defined by
f∗(g)=g◦f.
An immediate consequence of the definitions is that any (covariant or
contravariant) functor from C to D takes isomorphisms in C to isomor-
phismsinD:Theproofisexactlythesameastheproofforthefundamental
group functor (Corollary 7.17).
The examples considered so far are all categories whose objects are sets
with some structure and whose morphisms are structure-preserving maps.
Here are some examples that are not of this type.
Example 7.33 (Homotopy Categories).
- ThehomotopycategoryHTOPisthecategorywhoseobjectsaretopo-
logicalspacesasinTOP,butwhosemorphismsarehomotopy classes
of continuous maps. Since composition preserves the homotopy rela-
tion,thisisindeedacategory.Theisomorphismsinthiscategoryare
the (homotopy classes of) homotopy equivalences.
- A closely related category is the pointed homotopy category HTOP ∗,
which has the same objects as TOP ∗ but whose morphisms are the
equivalence classes of continuous maps modulo homotopy relative
to the base point. One consequence of the homotopy invariance of
the fundamental group is that π1 defines a functor from HTOP ∗ to
GROUP.

---

174 7. Homotopy and the Fundamental Group
Example 7.34 (Groups as Categories). Suppose C is a category with
oneobject,inwhicheverymorphismisanisomorphism.Ifwecalltheobject
X,theentirestructureofthecategoryiscontainedinthesetHomC(X,X)
of morphisms and its composition law. The axioms for a category say that
any two morphisms can be composed to obtain a third morphism, that
composition is associative, and that there is an identity morphism. The
additional assumption that every morphism is an isomorphism means that
each morphism has an inverse. In other words, HomC(X,X) is a group!
Functors between such categories are just group homomorphisms. In fact,
every group can be identified with such a category. One way to see this is
to identify a group G with the subcategory of SET consisting of the one
object G and the maps L : G→G given by left translation.
g
Another ubiquitous and useful technique in category theory goes by the
nameof“universalmappingproperties.”Thesegiveaunifiedwaytodefine
common constructions that arise in many categories, such as products and
sums.
Let{X :α∈A}beanyindexedcollectionofobjectsinacategoryC.An
α
object P together with a set of morphisms π : P →X called projections
α α
is said to be a product of the objects {X } if given any object W in C and
α
morphisms f : W →X , there exists a unique morphism f: W →P such
α α
that each of the following diagrams commutes:
P
(cid:3)(cid:4)
f (cid:3) π α
(cid:3) (cid:5)
(cid:2)
W X .
f α
α
Lemma 7.35. If a product exists in any category, it is unique up to an
isomorphism that respects the projections.
Proof. If (P,{π }) and (P(cid:5),{π(cid:5) }) are both products of objects {X },
α α α
the defining property guarantees the existence of maps f: P → P(cid:5) and
f(cid:5): P(cid:5) →P satisfying π(cid:5) ◦f =π and π ◦f(cid:5) =π(cid:5) . Arguing exactly as in
α α α α
theproofthattheproducttopologyonX1 ×···×X
n
istheuniqueonesat-
isfying the characteristic property (Theorem 3.10), we conclude that f◦f(cid:5)
and f(cid:5)◦f are both identity maps.
Inanyparticularcategory,productsmayormaynotexist.Herearesome
examples of familiar categories in which products always exist.
Example 7.36 (Categorical Products).
(a) The product of a collection of sets in the category SET is just their
Cartesian product.

---

Categories and Functors 175
(b) In the category TOP of topological spaces and continuous maps, the
productoffinitelymanyspacesX1,…,X
n
isthespaceX1 ×···×X
n
with the product topology. The characteristic property of the prod-
uct topology guarantees that the product space satisfies the defining
conditionforaproduct.(Thecategoricaldefinitionofproduct,bythe
way, determines the correct definition of the product topology on a
product of infinitely many spaces; see Problem 7-12.)
(c) The produ(cid:28)ct of groups {G
α
:α∈A} in GROUP is their direct prod-
uct group G , with the group structure obtained by multiplying
α α
elements componentwise.
Exercise 7.8. Prove that each of the above constructions satisfies the
defining property of a product in its category.
If we reverse all the morphisms in the definition of a product, we get
a dual concept called a sum. A sum of objects {X } in a category C is
α
an object S together with morphisms ι : X → S called injections such
α α
that given any object W in C and morphisms f : X → W, there exists
α α
a unique morphism f: S → W such that each of the following diagrams
commutes:
S
(cid:8)(cid:6)
ι α (cid:6)f
(cid:6)(cid:7)
(cid:2)
X W.
α f
α
Lemma 7.37. If a sum exists in a category, it is unique up to an isomor-
phism that respects the injections.
Exercise 7.9. Prove Lemma 7.37.
Some examples of categorical sums are given in the problems.

---

176 7. Homotopy and the Fundamental Group
Problems
7-1. Let B ⊂ Rn be any convex set, X any topological space, and A any
subset of X. Show that any two continuous maps f,g: X → B that
agree on A are homotopic relative to A.
7-2. Prove the following facts about retracts.
(a) A retract of a Hausdorff space is closed.
(b) A retract of a connected space is connected.
(c) A retract of a compact space is compact.
(d) A retract of a simply connected space is simply connected.
(e) A retract of a retract is a retract, i.e., if A ⊂ B ⊂ X, A is a
retract of B, and B is a retract of X, then A is a retract of X.
7-3. Show that the M¨obius band (see Chapter 5) is homotopy equivalent
to S1.
7-4. Let X be a path connected space and p,q ∈ X. Determine an alge-
braic necessary and sufficient condition on the fundamental group of
X underwhichallpathclassesfromptoqgivethesameisomorphism
of π1(X,p) with π1(X,q).
7-5. For any compact surface S, show that S with one point removed is
homotopy equivalent to a bouquet of finitely many circles.
7-6. Let K be a simplicial complex and σ ∈K any simplex. Show that |σ|
has a neighborhood U ⊂ |K| such th(cid:2)at |σ| is a strong deformation
retract of U. [Hint: Let U = |K| (cid:3) {|τ| : τ ∩ σ = ∅}. For any
k-simplex τ = (cid:22)v0,…,v
k
(cid:23) whose intersection with σ is nonempty,
define π: τ ∩U →τ ∩U by
(cid:20) (cid:21) (cid:20) (cid:21) (cid:20) (cid:21)
(cid:14)k (cid:14)l −1 (cid:14)l
π t v = t t v ,
i i i i i
i=0 i=0 i=0
wherev0,…,v
l
aretheverticesofτ∩σ,andletH: (τ∩U)×I →τ∩U
bethestraight-linehomotopybetweenIdandπ.ShowthatH defines
a strong deformation retraction of U onto |σ|.]
7-7. GiveanotherproofofLemma7.29byconsideringthemapF: I×I →
Y defined by F(s,t)=H(f(s),t) and applying Lemma 7.12.
7-8. Show that any two vertices in a tree are joined by a unique reduced
edge path.

---

Problems 177
7-9. Given any collection(cid:6) {X
α
: α ∈ A} of topological spaces, show that
theirdisjointunion
α
X
α
,togetherwith(cid:6)thedisjointuniontopology
and the natural inclusions ι : X (cid:9)→ X , is their sum in the
α α α α
category TOP.
(cid:29)
7-10. Given any collection of abelian groups(cid:28) {G
α
: α ∈ A}, let
α
G
α
be the subgroup of the direct product G consisting of all those
α α
elements {g α } α∈A such that g α is the identity element(cid:29)t in G α for all
but finitely many α; and for each α let ι : G (cid:9)→ G be the
α α α α
obvious injection. Show that this group, called the direct sum of the
groups G , is the sum of the G ’s in the category AB.
α α
7-11. Show that the construction described in Problem 7-10 does not yield
the sum in the category GROUP as follows: Take G1 = G2 = Z,
andfindhomomorphismsf1 andf2 fromZtosome(necessarilynon-
abelian) group H such that no homomorphism f: Z⊕Z→H makes
the following diagram commute for i=1,2:
Z⊕Z
(cid:8)(cid:6)
ι i (cid:6)f
(cid:6)(cid:7)
(cid:2)
Z H.
f
i
(We will see how to construct the sum in GROUP in Chapter 9.)
7-12. Given any collection {X
α
: α ∈ (cid:28)A} of topological spaces, define a
basis in th(cid:28)e Cartesian product
α
X
α
consisting of product sets of
the form
α
U
α
, where U
α
is open in X
α
and U
α
=(cid:28)X
α
for all but
finitely many α. Show that this is a basis, and that X with this
α α
topology is the product of the spaces X in the category TOP.
α
7-13. Showthatanyvertexinaconnectedfinitetreeisastrongdeformation
retract of the tree.

---

8
Circles and Spheres
So far, we have not actually computed any nontrivial fundamental groups.
The main goal of this chapter is to remedy this by computing the funda-
mental group of the circle. We will show, as promised, that π1(S1,1) is an
infinite cyclic group generated by the path α that goes once around the
circle counterclockwise at constant speed. Thus each element of π1(S1,1)
is uniquely determined by an integer, called its “winding number,” which
counts the net number of times and in which direction the path winds
around the circle.
Here is the essence of the plan. We would like to show that any loop in
the circle is in the path class [α]n for a unique integer n. The idea is to
represent a path by giving its angle θ(s) as a function of the parameter,
and then the winding number should be essentially 1/(2π) times the total
change in angle, θ(1)−θ(0).
Sincetheangleθisnotawell-definedcontinuousfunctiononthecircle,in
ordertomakerigoroussenseofthis,weneedtoundertakeadetailedstudy
oftheexponentialquotientmapε: R→S1 definedattheendofChapter3.
Ananglefunctionforaloopf isjust(uptoaconstantmultiple)a“lift”of
f to a path in R. Because R is simply connected, we can always construct
a homotopy between two lifts that have the same total change in angle.
Therearethreekeyliftinglemmasthatmakethisallwork.Inthebegin-
ning of the chapter we state those lifting lemmas, and then we use them
to prove that the fundamental group of the circle is infinite cyclic. In the
next section we prove the lifting lemmas. These three properties will make
another very important appearance later in the book, when we discuss
covering spaces.

---

180 8. Circles and Spheres
At the end of the chapter we compute the fundamental groups of the
higher-dimensional spheres and product spaces, and show that the funda-
mental group of any manifold is countable.
The Fundamental Group of the Circle
Throughout this chapter we will think of the circle as lying in the complex
plane, and we will always use the base point 1 ∈ C, which corresponds to
(1,0)∈R2.
Let α: I → S1 denote the loop α(s) = e2πis. The complete structure of
the fundamental group of the circle is described by the following theorem.
Theorem 8.1. The group π1(S1,1) is infinite cyclic, with generator [α].
To prove this theorem we will use a concrete representative of the path
class[α]n,definedasfollows.Foranyinteger n,letα : I →S1 betheloop
n
α n (s)=e2πins. It is easy to see that α n is a reparametrization of α n−1 · α,
so by induction [α ]=[α]n.
n
As mentioned in the introduction to this chapter, the proof of the theo-
remisbasedonacloseexaminationofthequotientmapε: R→S1 defined
by ε(x) = e2πix. If ϕ: B → S1 is any continuous map, a lift of ϕ is a
continuous map ϕ(cid:7): B →R such that the following diagram commutes:
R
(cid:3)(cid:4)
(cid:3)
ϕ(cid:7) ε
(cid:3)
(cid:3) (cid:5)
(cid:2)
B ϕ S1.
For example, if f: I → S1 is a path in S1, then a lift f (cid:7) of f can be
(cid:7)
interpreted geometrically by observing that θ(s) = 2πf(s) is a continuous
choice of angle function such that f(s)=eiθ(s).
It is important to be aware that some maps may have no lifts at all. For
example, suppose σ: S1 →R were a lift of the identity map of S1:
R
(cid:3)(cid:4)
(cid:3)
σ ε
(cid:3)
(cid:3) (cid:5)
(cid:2)
S1 S1.
IdS1
Then the equation ε ◦ σ = IdS1 means that 2πσ is a continuous choice
of angle function on the circle. It is intuitively evident that this cannot
exist, because any choice of angle function would have to change by 2π
as one goes once around the circle, and thus could not be continuous on

---

The Fundamental Group of the Circle 181
the whole circle. Assuming for the moment the result of Theorem 8.1, we
can prove rigorously that σ cannot exist just by noting that if there were
such a map, the induced homomorphism ε∗ ◦σ∗ would be the identity on
π1(S1,1), which would mean in particular that ε∗: π1(R,0) → π1(S1,1)
was surjective. Since π1(R,0) is the trivial group and π1(S1,1) is not, this
is impossible.
The first important fact about lifts is the following uniqueness lemma.
This is not actually used directly in the computation of π1(S1), but it is
necessary for proving the other two lifting properties.
Lemma 8.2 (Unique Lifting Property of the Circle). SupposeB is
connected, ϕ: B →S1 is continuous, and ϕ(cid:7) 1,ϕ(cid:7) 2: B →R are lifts of ϕ that
agree at some point of B. Then ϕ(cid:7) 1 ≡ϕ(cid:7) 2.
The next lifting lemma shows that paths in the circle, at least, always
have lifts.
Lemma 8.3 (Path Lifting Property of the Circle). Suppose
f: I → S1 is any path, and r0 ∈ R is any point in the fiber of ε
over f(0). Then there exists a unique lift f (cid:7) : I → R of f such that
(cid:7)
f(0)=r0.
Our third lifting lemma concerns lifts of homotopies: It says that lifts of
path homotopic paths are path homotopic, as long as they both start at
the same point.
Lemma 8.4 (Homotopy Lifting Property of the Circle). Suppose
f0,f1: I →S1 are path homotopic, and f (cid:7) 0,f (cid:7) 1: I →R are lifts of f0 and f1
with the same initial points. Then f (cid:7) 0 ∼f (cid:7) 1.
Assuming these lifting lemmas, let us now carry out the proof of our
theorem about the fundamental group of the circle.
Proof of Theorem 8.1. Define a map j: Z → π1(S1,1) by j(n) = [α]n. It
suffices to show that j is an isomorphism (considering Z as an additive
group). Because [α]n+m = [α]n[α]m, j is a homomorphism. We will show
that it is injective and surjective.
To prove surjectivity, let [f] be any element of π1(S1,1). By the path
lifting property of the circle, f has a lift f (cid:7) : I → R such that f (cid:7) (0) = 0
(Figure 8.1). Now, e2πif (cid:7)(1) = ε◦f (cid:7) (1) = f(1) = 1, so f (cid:7) (1) is an integer n.
We will show that [f]=[α ]=j(n).
n
If we let b : I → R be the path b (s) = ns, the two paths f (cid:7) and b
n n n
bothstartat0andendatn.BecauseRissimplyconnected,f (cid:7)∼b .Since
n
continuous maps preserve path homotopy, this implies f =ε◦f (cid:7)∼ε◦b =
n
α , thus proving that j is surjective.
n
To prove injectivity, suppose some n∈Z is mapped by j to the identity
element [c1] ∈ π1(S1,1), or in other words, [α]n = [c1]. Representing the

---

182 8. Circles and Spheres
n
(cid:7)
f b
n
0
ε
f 1
FIGURE 8.1. Proof that every path in S1 is homotopic to αn.
path class [α]n by α
n
as above, the assumption is α
n
∼ c1. If α(cid:7)
n
and (cid:7)c1
are lifts of α
n
and c1 starting at 0, the homotopy lifting property of the
circleguaranteesthatα(cid:7)
n
∼(cid:7)c1 inR.Inparticular,theybothhavethesame
terminal point. Now the lift of α starting at 0∈R is easily seen to be b ,
n n
and the lift of c1 is the constant loop c0. Thus n=b
n
(1)=c0(1)=0, so j
is injective.
Acloseexaminationofthisproofshowsthatwehaveactuallyconstructed
an explicit inverse for j, which is of interest in its own right. Define a map
N: π1(S1,1)→Zasfollows:Forany[f]∈π1(S1,1),letN[f]=f (cid:7) (1),where
f (cid:7) is the lift of f starting at 0 ∈ R. Such a lift exists by the path lifting
(cid:7)
property,andf(1)isindependentofthechoiceoff bythehomotopylifting
property. The proof above shows that N =j−1.
(cid:7)
If we think of 2πf as a continuous choice of angle function for f, then
2πN[f] represents, intuitively, the total change in the angle of f(s) as s
goes from 0 to 1, and N[f] represents the number of times f winds around
the circle. For this reason, N[f] is called the winding number of the path
f.

---

Proofs of the Lifting Lemmas 183
(cid:7)
U
n
R
ε
S1
q
U
FIGURE 8.2. Evenly covered neighborhood in S1.
Proofs of the Lifting Lemmas
Before proving the three lifting lemmas, we need some preliminary results.
The first is a precise description of the behavior of the quotient map ε.
Lemma 8.5. Each point q ∈ S1 has a neighborhood U such that ε−1(U)
(cid:7)
is a disjoint union of countably many open intervals U , on each of which
n
(cid:7)
the restriction of ε is a homeomorphism from U onto U (Figure 8.2).
n
Proof. This is just a straightforward computation from the definition of ε.
We can take, for example, U = S1(cid:3){−q}; then the sets U (cid:7) are the open
n
intervals of the form (r +n,r +n+1), where r is a fixed number such
that ε(r)=−q and n ranges over the integers. For each n, ε: U (cid:7) →U is a
n
bijective open map and therefore a homeomorphism.

---

184 8. Circles and Spheres
An open set U ⊂ S1 that has the properties described in this lemma is
saidtobeevenlycovered.Themostimportantpropertyofanevenlycovered
open set is that it admits local right inverses for ε, as we now describe.
First, a bit of terminology. If p: X →Y is any surjective continuous map,
a section of p is a continuous map σ: Y →X such that p◦σ =Id (i.e., a
Y
right inverse for p):
X
p σ
Y.
If U ⊂ Y is an open set, a local section of p over U is a continuous map
σ: U →X such that p◦σ =Id .
U
Lemma 8.6 (Local Section Property of the Circle). Let U ⊂S1 be
an evenly covered open set. For any q ∈U and any r in the fiber of ε over
q, there is a local section σ of ε over U such that σ(q)=r.
Proof. By definition of an evenly covered open set, r is contained in some
open set U (cid:7) ⊂ R such that ε: U (cid:7) → U is a homeomorphism. Thus σ =
n n
(ε| (cid:7) )−1 is the desired local section.
Un
Proof of the Unique Lifting Property. LetS={b∈B :ϕ(cid:7) 1(b)=ϕ(cid:7) 2(b)}.By
hypothesis S is not empty. Since B is connected, if we can show that S is
open and closed in B, it must be all of B.
To show that S is open, let b ∈ S. Write r = ϕ(cid:7) 1(b) = ϕ(cid:7) 2(b) and q =
ε(r) = ϕ(b). Let U ⊂ S1 be an evenly covered neighborhood of q, and
let U (cid:7) be the component of ε−1(U) containing r (Figure 8.3). If we set
V = ϕ(cid:7)− 1 1 (U (cid:7) )∩ϕ(cid:7)− 2 1 (U (cid:7) ), then V is a neighborhood of b on which both ϕ(cid:7) 1
and ϕ(cid:7) 2 take their values in U (cid:7) . Now, the fact that ϕ(cid:7) 1 and ϕ(cid:7) 2 are lifts of ϕ
translates to ϕ = ε◦ϕ(cid:7) 1 = ε◦ϕ(cid:7) 2. Since ε is injective on U (cid:7) , we conclude
that ϕ(cid:7) 1 and ϕ(cid:7) 2 agree on V, which is to say that V ⊂S, so S is open.
To show that it is closed, we will show that its complement is open. Let
b (cid:14)∈ S, and set r1 = ϕ(cid:7) 1(b) and r2 = ϕ(cid:7) 2(b), so that r1 (cid:14)= r2. As above, let
q = ε(r1) = ε(r2) = ϕ(b), and let U be an evenly covered neighborhood
(cid:7) (cid:7)
of q. Then there are disjoint neighborhoods U1 of r1 and U2 of r2 such
(cid:7) (cid:7)
that ε is a homeomorphism from U1 to U and from U2 to U. Letting
V = ϕ(cid:7) 1 −1 (U (cid:7) 1)∩ϕ(cid:7)− 2 1 (U (cid:7) 2), we conclude that ϕ(cid:7) 1(V) ⊂ U (cid:7) 1 and ϕ(cid:7) 2(V) ⊂ U (cid:7) 2,
soϕ(cid:7) 1 (cid:14)=ϕ(cid:7) 2 onV,whichistosaythat V ∩S=∅.ThusSisclosed,and the
proof is complete.
Proof of the path lifting property. Let f: I → S1 be a path, and r0 ∈
ε−1(f(0)) as in the statement of the lemma. If U is an open cover of the
circle by evenly covered open sets, the collection {f−1(U) : U ∈ U} is an
open cover of I. Let δ be a Lebesgue number for this cover. Choosing an

---

Proofs of the Lifting Lemmas 185
ϕ(cid:7) 1 r (cid:7)
U
ϕ(cid:7)−1 (U (cid:7) ) b
1
ϕ(cid:7)
2
V
ϕ(cid:7)−1
(U
(cid:7)
)
ε
2
ϕ
B
q
U
FIGURE 8.3. Proof of the unique lifting property.
integer n large enough that 1/n < δ, the Lebesgue number lemma says
that each interval [k/n,(k+1)/n] of length 1/n is contained in one of the
sets f−1(U), which is to say that it is mapped by f into an evenly covered
open set.
Wedefinetheliftf (cid:7) : I →Rinductivelyasfollows.Firstchooseanevenly
covered open set U0 such that f[0,1/n] ⊂ U0. Letting σ0: U0 → R denote
the local section such that σ0(f(0))=r0, we set
f (cid:7) =σ0 ◦f on [0,1/n].
(cid:7) (cid:7)
It follows immediately that f is continuous and satisfies f(0) = r0 and
ε◦f (cid:7) =f.
Proceeding by induction, suppose we have defined a continuous lift of f
onanintervaloftheform[0,k/n]forsomeintegerk.Asbefore,f[k/n,(k+
1)/n] is contained in an evenly covered set U . Letting σ : U →R be the
k k k
(cid:7)
local section such that σ (f(k/n))=f(k/n), we set
k
f (cid:7) =σ ◦f on [k/n,(k+1)/n].
k

---

186 8. Circles and Spheres
The resulting map is continuous by the gluing lemma. By induction we
(cid:7)
obtainaliftf definedonallofI.Itisuniquebytheuniqueliftingproperty.
Proof of the homotopy lifting property. Nowsupposef0,f1 arepathhomo-
(cid:7) (cid:7)
topic paths in the circle, and f0,f1 are any lifts of them starting at the
same point r0 ∈ R. Let H: f0 ∼ f1 be a path homotopy. This means that
H: I×I →S1 satisfies
H(s,0)=f0(s);
H(s,1)=f1(s);
H(0,t)=f0(0)=f1(0);
H(1,t)=f0(1)=f1(1).
We will show below that there exists a lift of H to a map H (cid:7) : I×I →R
(cid:7)
suchthatH(0,0)=r0.Assumingthis,weargueasfollows.First,notethat
ε◦H (cid:7) (0,t)=H(0,t)=f0(0).Therefore,t(cid:10)→H (cid:7) (0,t)isaliftoftheconstant
loopatf0(0)toapathstartingatr0;bytheuniqueliftingproperty,itmust
(cid:7)
be the constant loop at r0, so H(0,t) = r0 for all t. The same argument
(cid:7) (cid:7)
showsthatH(1,t)isconstantforallt,soH isapathhomotopy.Moreover,
(cid:7) (cid:7) (cid:7)
H0(s) = H(s,0) is a lift of f0 starting at r0, and similarly, H1 is a lift of
f1 starting at r0. By the unique lifting property, these must be equal to
(cid:7) (cid:7) (cid:7)
the given lifts f0 and f1, respectively, and H provides a path homotopy
between them.
(cid:7)
All that remains is to prove the existence of the lift H. As in the proof
ofthepathliftingproperty,thereexistsδ >0suchthatanysubsetofI×I
whosediameterislessthanδismappedbyH intoanevenlycoveredsubset
ofS1.Choosenlar√geenoughthateachsquareofside1/nhasdiameterless
than δ. (Any n> 2/δ will do.)
For any integers i,j such that 0≤i,j ≤n−1, let S denote the square
ij
[i/n,(i+1)/n]×[j/n,(j+1)/n] (Figure 8.4). For any point x ∈ R in the
(cid:7)
fiber of ε over H(i/n,j/n), there exists a unique lift H of H over S
ij ij
satisfying H (cid:7) (i/n,j/n) = x, given by H (cid:7) = σ◦H , where σ is the local
ij ij ij
section of ε such that σ(H(i/n,j/n))=x.
WedefineH (cid:7) inductivelyonI×I asfollows.OnS00,letH (cid:7) 00 betheliftof
(cid:7) (cid:7)
H such that H(0,0)=r0. On the next square to the right, S10, let H10 be
(cid:7) (cid:7)
theliftsuchthatH10(1/n,0)=H00(1/n,0).Wenowhavetwoliftsdefined
onthelinesegment{(1/n,t):0≤t≤1/n}wherethetwosquaresoverlap.
But on this line segment, the paths t (cid:10)→ H (cid:7) 00(1/n,t) and t (cid:10)→ H (cid:7) 10(1/n,t)
arebothliftsofthepatht(cid:10)→H(1/n,t)startingatthesamepoint;thusby
the unique lifting property they are equal.
Continuing in this way, we define lifts on each of the squares S i0, i =
0,…,n−1,andthenonthesquaresofthesecondrow,andsoon.Suppose
by induction that we have defined lifts H (cid:7) i(cid:3)j(cid:3) on all squares S i(cid:3)j(cid:3) for j(cid:5) <j,

---

Fundamental Groups of Spheres 187
(cid:7)
U
(cid:7)
H(i/n,j/n)
(cid:7)
H
ε
S H
ij
j/n
H(i/n,j/n)
i/n
U
FIGURE 8.4. Proof of the homotopy lifting property (inductive step).
andforj(cid:5) =j andi(cid:5) <i,andallsuchliftsagreewheretheyoverlap.Welet
(cid:7)
H betheuniqueliftofH onS thatagreeswithany(henceall)previous
ij ij
liftsatthelowerleftcorner(i/n,j/n).Atatypicalsuchsquare,wehaveto
checkthatthenewliftagreeswithtwodifferentoldones:onecomingfrom
thesquareS i−1,j totheleft,andonecomingfromthesquareS i,j−1 below.
Just as in the preceding paragraph, the unique lifting property guarantees
that the old and new lifts agree on both of these line segments.
(cid:7) (cid:7) (cid:7)
In the end we obtain the desired lift H by letting H = H on S ; it is
ij ij
continuous by the gluing lemma.
Fundamental Groups of Spheres
The situation is much simpler for the higher-dimensional spheres. The
sphere minus the north pole is homeomorphic to Rn by stereographic pro-
jection(seeExample3.6).In fact,composingstereographicprojectionwith
a suitable rotation of the sphere, it is easy to see that the sphere minus
any point is homeomorphic to Rn. Therefore, if we knew that any loop in

---

188 8. Circles and Spheres
Sn omitted at least one point in the sphere, we could consider it as a loop
in Rn; since it is null homotopic there, it is null homotopic in Sn.
Unfortunately,anarbitraryloopmightnotomitanypoints.Forexample,
thereisacontinuoussurjectivemapf: I →I×I (a“space-fillingcurve”—
see, e.g., [Rud76]). Composing this with a surjective map I×I →S2 such
as the one constructed in Proposition 6.2(b) yields a path whose image is
all of S2. But as the proof of the next proposition shows, we can modify
any curve by a homotopy so that it does miss a point.
Theorem 8.7. For n≥2, Sn is simply connected.
Proof. Let N =(0,…,0,1) denote the north pole, and S =−N the south
pole.BoththeopensetsU =Sn(cid:3){N}andV =Sn(cid:3){S}arehomeomorphic
toRn.Iff: I →Sn isanypath,bytheLebesguenumberlemmathereisan
integer n such that on each subinterval [k/n,(k+1)/n], f takes its values
either in U or in V. Now, V (cid:3){N} is homeomorphic to Rn(cid:3){0}, which
is connected. (Here is where the dimensional restriction comes in—when
n=1, Rn(cid:3){0} is disconnected.) Thus, for each such segment that lies in
V,thereisanotherpathinV withthesameendpointsthatmissesN;since
V is simply connected, these two paths are path homotopic in V and thus
inSn.Ofcourse,eachsegmentthatliesin U alreadymissesN.Thisshows
thatf ishomotopictoapathinSn(cid:3){N}≈Rn,sof isnullhomotopic.
Corollary 8.8. For n≥3, Rn(cid:3){0} is simply connected.
Proof. The map F: Rn (cid:3){0} → Sn−1 given by F(x) = x/|x| is a strong
deformation retraction (by a straight-line homotopy).
Fundamental Groups of Product Spaces
In this section we will show how to compute the fundamental group of an
arbitrary(finite)productoftopologicalspacesintermsofthefundamental
groups of the factors. As an application, we will compute the fundamental
groups of tori.
Let X1,…,X
n
be topological spaces, and let p
i
: X1 ×···×X
n
→ X
i
denoteprojectionontheithfactor.(Weareavoidingourusualnotationπ
i
for the projections here so as not to create confusion with the notation π1
for the fundamental group.) Choosing base points q ∈X , we get maps
i i
p
i∗
: π1(X1 ×···×X
n
,(q1,…,q
n
))→π1(X
i
,q
i
).
Putting these together, we define a map
p(cid:7): π1(X1 ×···×X
n
,(q1,…,q
n
))→π1(X1,q1)×···×π1(X
n
,q
n
)

---

Fundamental Groups of Manifolds 189
by
p(cid:7)[f]=(p1∗ [f],…,p
n∗
[f]). (8.1)
Proposition 8.9 (Fundamental Group of a Product). If X1, … ,
X
n
are any topological spaces, the map p(cid:7): π1(X1 ×···×X
n
,(q1,…,q
n
))→
π1(X1,q1)×···×π1(X
n
,q
n
) defined by (8.1) is an isomorphism.
Proof. First we will show that p(cid:7) is surjective. Let [f
i
] ∈ π1(X
i
,q
i
) be
arbitrary for i = 1,…,n. Define a loop f in the product space by
f(s) = (f1(s),…,f
n
(s)). Since the component functions of f satisfy
f
i
=p
i
◦f,wecomputep(cid:7)[f]=(p1∗ [f],…,p
n∗
[f])=([p1 ◦f],…,[p
n
◦f])=
([f1],…,[f
n
]).
To show injectivity, suppose f is a loop in the product space, and p(cid:7)[f] is
the identity element of π1(X1,q1)×···×π1(X
n
,q
n
). Writing f in terms of
itscomponentfunctionsasf(s)=(f1(s),…,f
n
(s)),thehypothesismeans
that [c ] = p [f] = [p ◦f] = [f ] for each i. If we choose homotopies
qi i∗ i i
H
i
: f
i
∼ c
qi
, it follows easily that the map H: X1 × ··· × X
n
× I →
X1 ×···×X
n
given by
H(x1,…,x
n
,t)=(H1(x1,t),…,H
n
(x
n
,t))
is a homotopy from f to the constant loop c(q1,…,qn ).
Corollary 8.10 (Fundamental Groups of Tori). Let Tn =S1×···×
S1 be the n-dimensional torus, and let α denote the standard loop in the
i
ith copy of S1:
α (s)=(1,…,1,e2πis,1,…,1).
i
Using q = (1,…,1) as base point, the map ϕ: Zn → π1(Tn,q) given by
ϕ(k1,…,k
n
)=[α1]k1···[α
n
]kn is an isomorphism.
Fundamental Groups of Manifolds
We conclude this chapter by proving an important theorem about funda-
mentalgroupsofmanifolds.Thisdoesnothavetodowithcirclesorspheres
per se, but it does use techniques similar to those used in the other proofs
in this chapter, so this is a convenient time to insert it.
Theorem 8.11. The fundamental group of a manifold is countable.
Proof. Let M be a manifold, and let U be a countable cover of M by
Euclidean balls. For each U,U(cid:5) ∈ U the intersection U ∩U(cid:5) has at most
countably many components; choose a point in each such component and

---

190 8. Circles and Spheres
x k−1 pU xk k −1,xk x
k
g k−1 f
k g
k
(cid:12) (cid:13)
(cid:12) (cid:13) f k
f k−1 n
n
U k−1
f
U
k
U k+1
FIGURE 8.5. Proof that a manifold has countable fundamental group.
let X denote the (countable) set consisting of all the chosen points as U,U(cid:5)
range over all the sets in U. For each U ∈ U and x,x(cid:5) ∈ X such that
x,x(cid:5) ∈U, choose a definite path pU from x to x(cid:5) in U.
x,x(cid:3)
Now choose any point q ∈X as base point. Let us say that a loop based
at q is special if it is a finite product of paths of the form pU . Because
x,x(cid:3)
both U and X are countable sets, there are only countably many special
loops.Eachspecialloopdeterminesanelementofπ1(M,q).Ifwecanshow
that every element of π1(M,q) is obtained in this way, we will be done,
because we will have exhibited a surjective map from a countable set onto
π1(M,q).
So suppose f is any loop based at q. By the Lebesgue number lemma
there is an integer n such that f maps each subinterval [(k −1)/n,k/n]
into one of the balls in U; call this ball U
k
. Let f
·
k
=
·
f| [(k−1)/n,k/n],
reparametrized on the unit interval, so that [f]=[f1] ··· [f
n
].
Sinceforeachk =1,…,n−1,f(k/n)∈U
k
∩U k+1,thereissomex
k
∈X
that lies in the same component of U k ∩U k+1 as f(k/n). Choose a path g k
in U k ∩U k+1 from x k to f(k/n) (Figure 8.5), and set f (cid:7) k =g k−1 · f k · g k −1
(taking x = q and g to be the constant path c when k = 0 or n). It is
k k q
immediatethat[f]=[f (cid:7) 1] · ··· · [f (cid:7)
n
],becausealltheg
k
’scancelout.Butfor
(cid:7)
eachk,f
k
isapathinU
k
fromx k−1tox
k
,andsinceU
k
issimplyconnected,
(cid:7)
f k is path homotopic to pU xk k −1xk . This shows that f is path homotopic to
a special loop and completes the proof.

---

Problems 191
Problems
8-1. Prove that the circle is not a retract of the closed disk.
8-2. Identifying the circle with the subspace S1 ×{1} ⊂ T2, prove that
the circle is not a deformation retract of the torus.
8-3. Provethatthefundamentalgroupofanytopologicalgroupisabelian.
[Hint: If f and g are loops based at 1∈G, consider the map F from
I×I into G given by F(s,t)=f(s)g(t) and use Lemma 7.12.]
8-4. Suppose U ⊂ R2 is an open set and x ∈ U. Show that U (cid:3){x} is
not simply connected. [Hint: Let S be a small circle around x, and
consider the sequence of inclusions S (cid:9)→U (cid:3){x}(cid:9)→R2(cid:3){x}.]
8-5. Showthatatopologicalspacecannotbesimultaneouslya2-manifold
andann-manifoldforsomen>2.[Hint:Ifn>2,anyn-manifoldhas
a basis of open sets in which the complement of any point is simply
connected.]
8-6. Let M be a 2-dimensional manifold with boundary. Show that the
setofboundarypointsofM isdisjointfromthesetofinteriorpoints.
Conclude that a 2-manifold with boundary is a manifold if and only
if its boundary is empty.
8-7. Let ϕ: S1 → S1 be a continuous map such that ϕ(1) = 1. Because
π1(S1,1) is infinite cyclic, there is an integer n, called the degree of
ϕ and denoted by degϕ, such that ϕ(γ) = γn for all γ ∈ π1(S1,1).
If ϕ: S1 → S1 is an arbitrary continuous map, we define the degree
of ϕ to be the degree of ρ ◦ ϕ, where ρ: S1 → S1 is the rotation
ρ(z)=z/ϕ(1) (in complex notation), which takes ϕ(1) to 1.
(a) Show that two maps ϕ,ψ: S1 →S1 are homotopic if and only if
they have the same degree.
(b) Showthatdeg(ϕ◦ψ)=degϕdegψforanytwocontinuousmaps
ϕ,ψ: S1 →S1.
(c) For each n ∈ Z, compute the degrees of the nth power map
p (z)=zn and its conjugate p (z)=zn.
n n
(d) Show that ϕ: S1 → S1 has an extension to a continuous map
Φ: B2 →S1 if and only if it has degree zero.
8-8. Provethefundamentaltheoremofalgebra:Everycomplexpolynomial
ofpositivedegreehasazero.[Hint:Ifp(z)=zn+a n−1zn−1+···+a0,
write p (z) = εnp(z/ε) and show that there exists ε > 0 such that
ε
|p ε (z)−zn| < 1 when z ∈ S1. If p has no zeros, prove that p ε | S1 is
homotopictop (z)=zn,andusetheresultsofProblem8-7toderive
n
a contradiction.]

---

192 8. Circles and Spheres
8-9. The Brouwer fixed point theorem says that any continuous map
f: Bn → Bn has a fixed point (i.e., a point x such that f(x) = x).
Prove this in the case n = 2 as follows: If f: B2 → B2 has no fixed
point, define ϕ: B2 → S1 by ϕ(x) = (f(x)−x)/|f(x)−x|. Derive a
contradiction by showing that the restriction of ϕ to S1 is homotopic
to the identity. [If you crumple a map of the country that you are in
and drop it on the ground, this theorem guarantees that some point
on the map will lie exactly over the point it represents.]
8-10. Let V be a vector field on R2, i.e., a continuous map V : R2 →R2. A
point q ∈R2 is called a singular point of V if V(q)=0, and a regular
pointifV(q)(cid:14)=0.Asingularpointisisolatedifithasaneighborhood
containing no other singular points. Let R ⊂ R2 denote the set of
V
regular points of V. For any loop f: I → R , define the index of V
V
withrespecttof,denotedbyInd(V,f),tobethewindingnumberof
the loop f (cid:7) : I →S1, given by
(cid:7) V(f(s))
f(s)= .
|V(f(s))|
(a) Show that Ind(V,f) depends only on the path class of f.
(b) If q is an isolated singular point of V, show that Ind(V,f ) is
ε
independentofεforεsufficientlysmall,wheref (s)=q+εα(s),
ε
and α is the standard counterclockwise loop around the unit
circle. This integer is called the index of V at q, and is denoted
by Ind(V,q).
(c) If V has finitely many singular points in the closed unit disk,
all in the interior, show that the index of V with respect to the
loop α around the unit circle is equal to the sum of the indices
of V at the interior singular points.
(d) Compute the index of each of the following vector fields at the
origin:
V1(x,y)=(x,y);
V2(x,y)=(−x,−y);
V3(x,y)=(x+y,x−y).

---

9
Some Group Theory
Inthischapterwedepartfromtopologyforawhiletodiscussgrouptheory.
Ourgoal,ofcourse,istousethegrouptheorytosolvetopologicalproblems,
and in the next chapter we will compute the fundamental groups of all
compact surfaces, and use them to show, among other things, that the
different surfaces listed in the classification theorem of Chapter 6 are not
homeomorphic to each other.
Beforewedoso,however,weneedtodevelopsometoolsforconstructing
and describing groups. We will discuss four such tools in this chapter: free
products of groups, free groups, presentations of groups by generators and
relations, and free abelian groups. These will all play central roles in our
computations of fundamental groups in the next chapter, and the material
on free abelian groups will also be used in the discussion of homology in
Chapter 13.
This chapter assumes that you are familiar with the basic facts of group
theory as summarized in the Appendix. If your group theory is rusty, this
wouldbeagoodtimetopulloutanalgebratextandrefreshyourmemory.
Free Products
Thereisafamiliarwaytocreateagroupasaproductoftwoormoreother
groups: The direct product of groupsG1,…,G
n
(see the Appendix) is the
Cartesian product set G1 ×···×G
n
with the group structure obtained by
multiplying the entries in two n-tuples component by component.

---

194 9. Some Group Theory
For each i, the direct product G1 ×···×G
n
has a subgroup {1}×···×
{1}×G ×{1}×···×{1} isomorphic to G , and it is easy to verify that
i i
elements of two distinct such subgroups commute with each other. As we
mentionedinChapter7,thisconstructionyieldstheproductinthecategory
of groups.
In our study of fundamental groups, we will need to build another kind
of product, in which the elements of different groups are not assumed to
commute.Thissituationarises,forexample,incomputingthefundamental
group of the wedge X ∨Y of two spaces X and Y, defined in Example
3.25. As we will see in the next chapter, the fundamental group of X ∨Y
containssubgroupsisomorphictoπ1(X)andπ1(Y),andanyloopinX∨Y
is equivalent to a product of loops lying in one space or the other. But in
general, path classes of loops in X do not commute with those in Y.
In this section we will introduce a more complicated product of groups
G1,…,G
n
that includes each G
i
as a subgroup, but in which elements of
the different subgroups do not commute with each other. It is called the
“free product,” and roughly speaking, it is just the set of expressions you
can get by formally multiplying together elements of the different groups,
with no relations assumed other than those that come from the multipli-
cation in each group G . It turns out (despite its name) to be the sum in
i
the category of groups.
Because terms such as “expressions you can get” and “multiplying ele-
mentsofdifferentgroups”aretoovaguetouseinmathematicalarguments,
theactualconstructionofthefreeproductisratherinvolved.Webeginwith
some preliminary terminology.
Let {G α } α∈A be an indexed collection of groups. The index set A can
be finite or infinite; for our applications we will need only the finite case,
so you are free to think of finite collections throughout this chapter. We
will usually omit mention of A and denote the collection simply by {G },
α
withGreeklettersunderstoodtorangeoverallelementsofsomeimplicitly
understood index set.
A word in {G(cid:6)α } is a finite sequence of length m ≥ 0 of elements of the
disjoint union G . In other words, a word is an ordered m-tuple of the
α α
form (g1,…,g
m
), where each g
i
is an element of some G
α
. (Recall that
formally, an element of the disjoint union is a pair (g,α), where α is a
“tag” to distinguish which group g came from. We will suppress the tag
in our notation, but remember that elements of groups corresponding to
different indices have to be considered distinct, even if the groups are the
same.) The sequence of length zero, called the empty word, is denoted by
( ). Let W denote the set of all words in {G }. We denote the identity
α
element of G by 1 .
α α
Define a multiplication operation in W by concatenation:
(g1,…,g
m
)(h1,…,h
l
)=(g1,…,g
m
,h1,…,h
l
).

---

Free Products 195
Clearly,thismultiplicationisassociative,andhastheemptywordasatwo-
sidedidentityelement.However,therearetwoproblemswiththisstructure
asitstands:First,Wisnotagroupunderthisoperationbecausethereare
noinverses;andsecond,thegroupstructuresofthevariousgroupsG have
α
not played a role in the definition so far.
Tosolvebothoftheseproblems,wedefineanequivalencerelationonthe
set of words as follows. An elementary reduction is an operation of one of
the following forms:
(g1,…,g i ,g i+1,…,g m )(cid:10)→(g1,…,g i g i+1,…,g m ) if g i ,g i+1 ∈ some G α ;
(g1,…,g i−1,1
α
,g i+1,…,g
m
)(cid:10)→(g1,…,g i−1,g i+1,…,g
m
).
The first operation just multiplies together two consecutive entries, pro-
vided that they are elements of the same group, and the second deletes
any identity element that appears in a word. We say that two words are
equivalent, written W ∼ W(cid:5), if one can be transformed into the other by
a finite sequence of elementary reductions or their inverses; this is obvi-
ously an equivalence relation. The set of equivalen∗ce classes is called the
free product of the groups {G }, and is denoted by G . In the case of a
α α α
finite set of groups, we just write G1 ∗···∗G
n
.
Lemma 9.1. Given any collection of groups {G }, their free product is a
α
groupunderthemultiplicationoperationinducedbymultiplicationofwords.
Proof. First we need to check that multiplication of words respects the
equivalence relation. If V(cid:5) is obtained from V by an elementary reduction,
then it is easy to see that V(cid:5)W is similarly obtained from VW, as is WV(cid:5)
from WV. If V ∼V(cid:5) and W ∼W(cid:5), it follows by induction on the number
of elementary reductions that VW ∼ V(cid:5)W(cid:5). Thus multiplication is well-
defined on equivalence classes.
The equivalence class of the empty word ( ) is obviously an identity
element, and multiplication is associative on equivalence classes because it
already is on words. Finally, for any word (g1,…,g
m
), it is easy to check
that
(g1,…,g
m
)(g
m
−1,…,g
1
−1 )∼( )∼(g
m
−1,…,g
1
−1 )(g1,…,g
m
),
so the equivalence class of (g−1,…,g −1 ) is an inverse for that of
m 1
(g1,…,g
m
).
Henceforth, we will denote the identity element of the free product (the
equivalence class of the empty word) by 1.
Formanypurposesitisimportanttohaveauniquerepresentativeofeach
equivalence class in the free product. We say that a word (g1,…,g
m
) is
reduced if it cannot be shortened by an elementary reduction. Specifically,
this means that no element g is the identity of its group, and no two
i

---

196 9. Some Group Theory
consecutive elements g i ,g i+1 come from the same group. It is easy to see
that any word is equivalent to a reduced word: Just perform elementary
reductions until it is impossible to perform any more. What is not so easy
to see is that the reduced word representing any given equivalence class is
unique.
∗
Proposition 9.2. Every element of G is represented by a unique re-
α α
duced word.
Proof. We showed above that every equivalence class contains a reduced
word,soweneedonlycheckthattworeducedwordsrepresentingthesame
equivalenceclassmustbeequal.Thisamountstoconstructinga“canonical
reduction algorithm.”
Let R denote the set of reduced words. We begin by constructing a map
W×R→R,
which sends (g1,…,g
m
)∈W and (h1,…,h
l
)∈R to a reduced word that
·
we denote by (g1,…,g
m
) (h1,…,h
l
) ∈ R. We will define the map by
induction on m, the length of the word in W. For m=0, define
·
( ) (h1,…,h
l
)=(h1,…,h
l
).
For m=1 and g ∈G , set
α
⎧
⎪⎪⎪⎨ (h2,…,h
l
), h1 ∈G
α
and gh1 =1
α
;
(g) · (h1,…,h
l
)=
⎪⎪⎪⎩
(
(
g
h
h
1,
1
.
,
.
.
.
.
,
.
h
,h
l )
l
,
), h
h
1
1
∈
(cid:14)∈
G
G
α
α
a
a
n
n
d
d
g
g
h
=
1 (cid:14)=
1 α
1
;
α ;
(g,h1,…,h
l
), h1 (cid:14)∈G
α
and g (cid:14)=1
α
.
(Theideaisjusttomultiplythetwowordsandreducethemintheobvious
way; what is important about this definition is that there are no arbitrary
choices involved.) For m>1, define the map recursively:
(cid:12) (cid:13)
· · ·
(g1,…,g
m
) (h1,…,h
l
)=(g1) (g2,…,g
m
) (h1,…,h
l
)
· · · ·
=(g1) (g2) ··· (g
m
) (h1,…,h
l
),
where we understand the dot operation to be performed from right to left:
· · · ·
U V W =U (V W).
The key feature of this operation is that it takes equivalent words to the
samereducedword:IfW ∼W(cid:5),thenW · V =W(cid:5)· V forallreducedwords
V. To prove this, it suffices to assume that W(cid:5) is obtained from W by an
elementary reduction. There are two cases, corresponding to the two types
of elementary reduction. Suppose first that W =(g1,…,g
i
,g i+1,…,g
m
),

---

Free Products 197
and W(cid:5) =(g1,…,g
i
g i+1,…,g
m
) is obtained by multiplying together two
consecutive elements g i ,g i+1 from the same group G α . Then
· · · · · · · · ·
W V =(g1) ··· (g i−1) (g
i
) (g i+1) (g i+2) ··· (g
m
) V.
· · ·
Writing (g i+2) ··· (g
m
) V =(h1,…,h
l
), it suffices to show that
· · ·
(g
i
) (g i+1) (h1,…,h
l
)=(g
i
g i+1) (h1,…,h
l
).
Applyingthedefinitionofthedotoperatortwiceandkeepingcarefultrack
of the various cases, you can compute
· ·
(g
i
) (g i+1) (h1,…,h
l
)
⎧
⎪⎪⎪⎨ (h2,…,h
l
), h1 ∈G
α
, g
i
g i+1h1 =1
α
;
=
(g
i
g i+1h1,…,h
l
), h1 ∈G
α
, g
i
g i+1h1 (cid:14)=1
α
;
⎪⎪⎪⎩ (h1,…,h l ), h1 (cid:14)∈G α , g i g i+1 =1 α ;
(g i g i+1,h1,…,h l ), h1 (cid:14)∈G α , g i g i+1 (cid:14)=1 α .
·
On the other hand, (g
i
g i+1) (h1,…,h
l
) is equal to the same value by
definition. The second case, in which W contains an identity element that
isdeletedtoobtainW(cid:5),followsinasimilarwayfromthefactthat(1 ) · V =
α
V.
Now we define our canonical reduction operator r: W → R by r(W) =
·
W ().Clearly,ifW isalreadyreduced,thenr(W)=W.Moreover,bythe
argument above, if W ∼ W(cid:5), then r(W) = r(W(cid:5)). Thus, if W ∼ W(cid:5) and
both are reduced words, we have W = r(W) = r(W(cid:5)) = W(cid:5). This proves
the proposition.
∗
ForeachgroupG ,thereisacanonicalmapι : G → G ,definedby
α α α α α
sendingg ∈G totheequivalenceclassoftheword(g).Eachofthesemaps
α
is a homomorphism, since (g1g2) ∼ (g1)(g2) for g1,g2 ∈ G
α
. Each map is
also injective: If g (cid:14)= 1 , both the words ι (g) = (g) and ι (1 ) = ( ) are
α α α α
reduced,andthereforecannotrepresentthesameequivalenceclassbecause
of the preceding proposition. We usually identify G with its image under
α
the injection ι , and write the equivalence class of the word (g) simply as
α
g.Therefore,theequivalenceclassofaword(g1,g2,…,g
m
)canbewritten
g1g2 ···g
m
;byaslightabuseofterminology,wewillalsocallsuchaproduct
a word, and say that it is reduced if the word (g1,g2,…,g
m
) is reduced.
Multiplication in the free product is indicated by juxtaposition of such
words. Thus we have finally succeeded in making mathematical sense of
products of elements in different groups.
Example 9.3. Let Z/(cid:22)2(cid:23) denote the group of integers modulo 2. The free
product Z/(cid:22)2(cid:23)∗Z/(cid:22)2(cid:23) can be described as follows. If we letβ and γ denote

---

198 9. Some Group Theory
thenontrivialelementsofthefirstandsecondcopiesofZ/(cid:22)2(cid:23),respectively,
each element of Z/(cid:22)2(cid:23)∗Z/(cid:22)2(cid:23) other than the identity has a unique repre-
sentationasastringofalternatingβ’sandγ’s.Multiplicationisperformed
byconcatenatingthestringsanddeletingallconsecutivepairsofβ’sorγ’s.
For example,
(βγβγβ)(γβγβ)=βγβγβγβγβ;
(γβγβ)(βγβγβ)=β.
This group is not abelian.
Example 9.4. Later we will need to consider the free product π1(S1,1)∗
π1(S1,1).Lettingα(s)=e2πis asintheprecedingchapter,andlettingβ,γ
denote the path classes of α in the first and second copies of π1(S1,1),
respectively, each element of π1(S1,1)∗π1(S1,1) other than the identity
has a unique expression of the form βi1γj1···βimγjm, where i1 or j
m
may
be zero, but none of the other exponents is zero.
The free product of groups has an important characteristic property.
Theorem 9.5 (Characteristic Property of the Free Product).
For any group H and any collection of∗homomorphisms ϕ
α
: G
α
→ H,
there exists a unique homomorphism Φ: G →H such that for each α
α α
the following diagram commutes:
∗
G
α α
(cid:8)(cid:6)
ι α (cid:6)Φ
(cid:6)(cid:7)
G (cid:2) H. (9.1)
α ϕ
α
Proof. Supposewearegivenacollectionofhomomorphismsϕ : G →H.
α α
The requirement that Φ◦ι =ϕ implies that the desired homomorphism
α α
Φ must satisfy
Φ(g)=ϕ (g) if g ∈G , (9.2)
α α
where,asusual,weidentifyG withitsimageunderι .SinceΦissupposed
α α
to be a homomorphism, it must satisfy
Φ(g1 ···g
m
)=Φ(g1)···Φ(g
m
). (9.3)
(cid:7)
Therefore, if Φ and Φ both satisfy the conclusion, they must be equal
because both must satisfy (9.2) and (9.3). This proves that Φ is unique if
it exists.
ToproveexistenceofΦ,weuse(9.2)and(9.3)todefineit.Thisisclearly
a homomorphism that satisfies the required properties, provided that it is

---

Free Groups 199
well-defined.Toverifythatitiswell-defined,weneedtocheckthatitgives
the same result when applied to equivalent words. As usual, we need only
check elementary reductions. If g i ,g i+1 ∈G α , we have
Φ(g
i
g i+1)=ϕ
α
(g
i
g i+1)=ϕ
α
(g
i
)ϕ
α
(g i+1)=Φ(g
i
)Φ(g i+1),
from which it follows that the definition of Φ is unchanged by multiply-
ing together successive elements of the same group. Similarly, Φ(1 ) =
α
ϕ (1 )=1∈H, which shows that Φ is unchanged by deleting an identity
α α
element. This completes the proof.
Corollary 9.6. The free product is the sum in the category of groups.
Proof. The characteristic property is exactly the defining property of the
sum in a category.
Corollary 9.7. The free product is the unique group (up to isomorphism)
satisfying the characteristic property.
Proof. Lemma 7.37 shows that sums in any category are unique up to
isomorphism.
In some texts, a free product is defined as any group satisfying the char-
acteristicproperty,orasthesuminthecategoryofgroups.Onemustthen
prove the existence of such a group by some construction such as the one
wehavegivenbeforeoneisentitledtotalkabout“the”freeproduct.Once
existenceisproved,uniquenessfollowsautomaticallyfromcategorytheory.
Thenicethingaboutthisuniquenessresultisthatnomatterwhatspecific
construction is used to define the free product (and you will find many in
the literature), they are all the same up to isomorphism.
Free Groups
In this section we will use the free product construction to create a new
class of groups called “free groups,” consisting of all possible products of a
set of “generators,” with no relations imposed at all. We begin with a few
more definitions.
LetGbeagroup.AsubsetS ⊂GissaidtogenerateG,andtheelements
of S are called generators for G, if every element of G can be written as
a product of elements of S. Of course, any group has a set of generators,
since we can take S to be the whole group G. But it is more interesting to
find a small set of generators when possible.
For example, a cyclic group is a group with one generator (see the Ap-
pendix). The cyclic groups are all isomorphic either to Z or to Z/(cid:22)n(cid:23) for
some n (Exercise A.26).

---

200 9. Some Group Theory
In this section we will be concerned mostly with infinite cyclic groups.
Given any object α, we can form an infinite cyclic group generated by
α, denoted by (cid:22)α(cid:23), as follows: (cid:22)α(cid:23) is the set {α}×Z with multiplication
(α,m)(α,k) = (α,k+m). We identify α with the element (α,1); thus we
can abbreviate (α,m) by αm, and think of (cid:22)α(cid:23) as the group of all integral
powers of α with the obvious multiplication.
Now suppose we are given any set S. We define the free group on S,
denoted by (cid:22)S(cid:23), to be the free product of all the infinite cyclic groups
generated by elements of S:
∗
(cid:22)S(cid:23)= (cid:22)α(cid:23).
α∈S
There is a natural injection ι: S (cid:9)→(cid:22)S(cid:23), defined by sending each α∈S to
the word α ∈ (cid:22)S(cid:23). Thus we can consider S as a subset of (cid:22)S(cid:23), and each
elementof(cid:22)S(cid:23)canbeexpressedasawordα
1
n1α
2
n2···α
m
nm,whereeachα
i
is
someelementofS andeachn isaninteger.Multiplicationisperformedby
i
juxtapositionandcombiningconsecutivepowersofthesameα bytherule
i
α
i
nα
i
k = α
i
n+k. In case S = {α1,…,α
n
} is a finite set, we denote the free
group on S by (cid:22)α1,…,α
n
(cid:23) instead of the more accurate but cumbersome
notation (cid:22){α1,…,α
n
}(cid:23). (We will rely on the context and typographical
differences to make clear the distinction between the free group (cid:22)S(cid:23) on the
elements of the set S and the infinite cyclic group (cid:22)α(cid:23), which is also equal
to the free group on the singleton {α}.)
Example 9.8. The free group on the empty set, denoted by (cid:22) (cid:23), is by
convention just the trivial group {1}. The free group on a singleton {α} is
the infinite cyclic group (cid:22)α(cid:23). The free group on the two-element set {β,γ}
is (cid:22)β,γ(cid:23)=(cid:22)β(cid:23)∗(cid:22)γ(cid:23), which is the same as the group described in Example
9.4.
Theorem 9.9 (Characteristic Property of the Free Group). Let
S be a set. For any group H and any map ϕ: S →H, there exists a unique
homomorphism ϕ(cid:7): (cid:22)S(cid:23)→H extending ϕ:
(cid:22)S(cid:23)
(cid:8)(cid:6)
ι (cid:6)ϕ(cid:7)
(cid:6)(cid:7)
(cid:2) (9.4)
S ϕ H.
Proof. This can be proved directly as in the proof of Theorem 9.5. Alter-
natively, recalling that the free group is defined as a free product, we can
proceed as follows. There is a one-to-one correspondence between set func-
tions ϕ: S → H and collections of homomorphisms ϕ : (cid:22)α(cid:23) → H for all
α

---

Presentations of Groups 201
α∈S, by the equation
ϕ (αn)=ϕ(α)n.
α
Translating the characteristic property of the free product to this special
case and using this correspondence yields the result. The details are left as
an exercise.
Exercise 9.1. Carry out the details of the proof of Theorem 9.9.
Exercise 9.2. Prove that the free group on S is the unique group (up to
isomorphism) satisfying the characteristic property.
Presentations of Groups
It is often convenient to describe a group by giving a set of generators for
it,andlistingafewrules,or“relations,”thatdescribehowtomultiplythe
generators together. For example, the cyclic group of order n generated by
γ might be described as the group generated by γ with the single relation
γn = 1; all other relations in the group, such as γ3n = 1 or γk−n = γk,
follow from this one. The direct product group Z×Z might be described
as the group with two generators β,γ satisfying the relation βγ =γβ. The
free group (cid:22)β,γ(cid:23) can be described as the group generated by β,γ with no
relations.
Sofar,thisismathematicallyveryvague.Whatdoesitmeantosaythat
“all other relations follow from a given one”? In this section we develop a
way to make these notions precise.
We define a group presentation to be an ordered pair, denoted by (cid:22)S|R(cid:23),
whereS isanarbitrarysetandRisasetofelementsofthefreegroup(cid:22)S(cid:23).
TheelementsofSandRarecalledthegeneratorsandrelators,respectively,
of the presentation. A group presentation defines a group, also denoted by
(cid:22)S|R(cid:23), as the following quotient:
(cid:22)S|R(cid:23)=(cid:22)S(cid:23)/R,
where R is the normal closure of R in (cid:22)S(cid:23), which is the intersection of all
normal subgroups of (cid:22)S(cid:23) containing R; thus R is the “smallest” normal
subgroup containing R.
Since the quotient of a group by a normal subgroup is again a group
(see the Appendix), (cid:22)S|R(cid:23) is indeed a group. Each of the generators s∈S
determines an element in (cid:22)S|R(cid:23) (its coset in the quotient group), which we
usually write also as s. Each of the relators r ∈ R represents a particular
product of generators and their inverses that is equal to 1 in the quotient.

---

202 9. Some Group Theory
Hereistheintuitionbehindthisconstruction.IfGisanygroupgenerated
by S, there is a surjective homomorphism Φ: (cid:22)S(cid:23)→G, whose existence is
guaranteedbythecharacteristicpropertyofthefreegroup.Ifallthewords
of R are to be equal to the identity in G, then the kernel of Φ must at
least contain R, and since it is normal, it must contain R; thus by the first
isomorphism theorem (Theorem A.13 in the Appendix), G is isomorphic
to a quotient of (cid:22)S(cid:23) by a normal subgroup containing R. By dividing out
exactly R, we ensure that the only relations that hold in (cid:22)S|R(cid:23) are those
that are forced by the relators in R. Thus, in a certain sense, (cid:22)S|R(cid:23) is the
“largest” group generated by S in which all the products represented by
elements of R are equal to 1.
If G is a group and there exists an isomorphism
(cid:22)S|R(cid:23)∼
=G, we say that
(cid:22)S|R(cid:23) is a presentation of G. At this point, the question naturally arises
whether every group has a presentation. In fact, the answer is yes, but
the result is not as satisfying as we might have hoped. Given a group G,
the set of all elements of G certainly generates G. By the characteristic
property of the free group, the identity map of G to itself has a unique
extension to a homomorphism Φ: (cid:22)G(cid:23)→G. If we set R=KerΦ, then the
first isomorphism theorem says that G ∼ = (cid:22)G(cid:23)/R. Since R is normal, it is
equal to its normal closure, and therefore G has the presentation (cid:22)G|R(cid:23).
This is highly inefficient, of course, since both (cid:22)G(cid:23) and R are vastly larger
than G itself.
If G admits a presentation (cid:22)S|R(cid:23) in which both S and R are finite sets,
wesaythatGisfinitelypresented.Inthiscase,weusuallywritethepresen-
tationas(cid:22)α1,…,α
n
|r1,…,r
m
(cid:23).Sincether
i
actuallyallbecomeequalto
the identity in the group defined by the presentation, it is also often con-
venient to replace the relators by the equations obtained by setting them
equal to the identity, called relations of the presentation, as in
(cid:22)α1,…,α
n
|r1 =1,…,r
m
=1(cid:23)
or even
(cid:22)α1,…,α
n
|r1 =q1,…,r
m
=q
m
(cid:23).
We take this to be an alternative notation for (cid:22)α1,…,α
n
| r1q
1
−1 , … ,
r q−1(cid:23).
m m
We conclude this section by describing one important example in detail.
Proposition 9.10. ThegroupZ×Zhasthepresentation(cid:22)β,γ |βγ =γβ(cid:23).
Proof. For brevity, write G = (cid:22)β,γ | βγ = γβ(cid:23) = (cid:22)β,γ | βγβ−1γ−1(cid:23). As
usual, we will use the symbols β and γ to denote either the generators of
the free group (cid:22)β,γ(cid:23) or their images in the quotient group G. We begin by
noting that G is abelian: The equation βγβ−1γ−1 = 1, which holds in G
by definition, immediately implies βγ = γβ, and then a simple induction

---

Free Abelian Groups 203
shows that any products of powers of β and γ commute with each other.
Since β and γ generate G, this suffices.
WewillprovethepropositionbydefininghomomorphismsΦ: G→Z×Z
and Ψ: Z×Z → G and showing that they are inverses of each other. To
define Φ, we first define Φ (cid:7) : (cid:22)β,γ(cid:23) → Z×Z by setting Φ (cid:7) (β) = (1,0) and
(cid:7) (cid:7)
Φ(γ)=(0,1); this uniquely determines Φ by the characteristic property of
(cid:7)
the free group. Explicitly, Φ is given by
Φ (cid:7) (βi1γj1···βimγjm)=(i1+···+i
m
,j1+···+j
m
). (9.5)
Because βγβ−1γ−1 ∈ KerΦ (cid:7) by direct computation, Φ (cid:7) descends to a map
Φ: G→Z×Z still given by (9.5).
In the other direction, we define Ψ: Z×Z→G by
Ψ(m,n)=βmγn.
It follows from the fact that G is abelian that Ψ is a homomorphism. A
simple computation shows that Ψ ◦ Φ(β) = β, Ψ ◦ Φ(γ) = γ, and Φ ◦
Ψ(m,n)=(m,n). Thus Φ and Ψ are inverses, so G ∼ =Z×Z.
In some ways, a presentation gives a very simple and concrete way to
understandthepropertiesofagroup,andwewilldescribethefundamental
groups of surfaces in the next chapter by giving presentations. However,
you should be aware that even with a finite presentation in hand, some
very basic questions about a group may still be difficult or impossible to
answer. For example, two of the most basic problems concerning group
presentations were first posed around 1910 by topologists Heinrich Tietze
and Max Dehn, shortly after the invention of the fundamental group: The
isomorphismproblemforgroupsistodecide,giventwofinitepresentations,
whether the resulting groups are isomorphic; and the word problem is to
decide, given a finite presentation (cid:22)S|R(cid:23) and a specific word formed from
elements of S, whether that word represents the identity element of the
group (cid:22)S|R(cid:23). It was shown in the 1950s that there is no algorithm for
solving either of these problems that is guaranteed to yield an answer for
everypresentationinafiniteamountoftime!(See[Sti82]forreferencesand
historical background.) These ideas form the basis for the subject called
combinatorial group theory, which is a lively research field at the intersec-
tion of algebra, topology, and geometry.
Free Abelian Groups
There is an analogue of free groups in the category of abelian groups. In
this section, since all our groups will be abelian, we will always write the
group operation additively, and denote the identity element by 0 and the

---

204 9. Some Group Theory
inverseofxby−x.IfGisanabeliangroup,g ∈G,andn∈Z,thenotation
ng means the n-fold sum g+···+g, and nG is the subgroup {ng :g ∈G}.
GivenanonemptysetS,letZ(cid:22)S(cid:23)denotethesetofallfunctionsk: S →Z
such that k(s)=0 for all but finitely many s∈S. This is easily seen to be
an abelian group under addition, called the free abelian group on S. Just
as we did for the free vector space defined in Chapter 5, we can identify
each s ∈ S with the element of Z(cid:22)S(cid:23) that takes the value 1 on s and zero
oneveryotherelementofS,soweconsiderS asasubsetofZ(cid:22)S(cid:23),andeach
element of Z(cid:22)S(cid:23) can be written uniquely as a finite sum of the form
(cid:14)n
k s
i i
i=1
where s
i
are elements of S and k
i
are integers. When S ={s1,…,s
n
} is a
finiteset,wewillusuallywritethefreeabeliangrouponS asZ(cid:22)s1,…,s
n
(cid:23).
By convention, the free abelian group on the empty set is the trivial group
{0} (we consider a “linear combination of no elements” to sum to 0).
Lemma 9.11 (Properties of Free Abelian Groups). Let S be a
nonempty set.
(a) Characteristic Property: Given any abelian group H and any
set map f: S →H, there exists a unique homomorphism f (cid:7) : Z(cid:22)S(cid:23)→
H extending f.
(cid:29)
(b) Z(cid:22)S(cid:23)isisomorphictothedirectsum (cid:22)s(cid:23)ofalltheinfinitecyclic
s∈S
groups generated by elements of S.
(c) If S = {s1,…,s
n
} is finite, then Z(cid:22)s1,…,s
n
(cid:23) is isomorphic to Zn
via the map (k1,…,k
n
)(cid:10)→k1s1+···+k
n
s
n
.
Exercise 9.3. Prove Lemma 9.11.
Let G be an abelian group. By analogy with vector spaces, a finite sum
of elements of G with integer coefficients is called a linear combination of
elementsofG.AnonemptysubsetS ⊂Gissaidtobelinearly independent
if the only linear combination of elements of S that equals zero is the one
forwhichallthecoefficientsarezero.AbasisforGisalinearlyindependent
subset that generates G. Just as in the case of vector spaces, if S is a basis
for G, every element of G can be written uniquely as a linear combination
of elements of S. For example, S is a basis for the free abelian group Z(cid:22)S(cid:23).
The set of elements e = (0,…,1,…,0) (with a 1 in the ith place) for
i
i=1,…,n is a basis for Zn, which we call the standard basis.
If a group G is isomorphic to Z(cid:22)S(cid:23) for some set S, G is also said to be
free abelian.

---

Free Abelian Groups 205
Exercise 9.4.
(a) Showthatanabeliangroupisfreeabelianifandonlyifithasabasis.
(b) Show that any two free abelian groups whose bases have the same
cardinality are isomorphic.
Lemma 9.12. If G has a finite basis, then every finite basis has the same
number of elements.
Proof. Suppose G has a basis with n elements. Then G ∼ = Zn by Lemma
9.11(c), and the quotient group G/2G is easily seen to be isomorphic to
(Z/(cid:22)2(cid:23))n, which has exactly 2n elements. Since the order of G/2G is inde-
pendent of the choice of basis, every finite basis must have n elements.
In view of this lemma, if G is a free abelian group with a finite basis, we
define the rank of G to be the number of elements in any finite basis. (In
fact, in that case every basis is finite—see Problem 9-6.) If G has no finite
basis, we say it has infinite rank.
Proposition 9.13. Suppose G is a free abelian group of finite rank. Any
subgroup of G is free abelian of rank less than or equal to that of G.
Proof. We may assume without loss of generality that G = Zn. We will
provethepropositionbyinductiononn.Forn=1,itfollowsfromthefact
that any subgroup of a cyclic group is cyclic.
Suppose the result is true for subgroups of Zn−1, and let H be any
subgroup of Zn. Identifying Zn−1 with the subgroup {(k1,…,k n−1,0)} of
Zn, the inductive hypothesis guarantees that H ∩Zn−1 is free abelian of
rank m−1 ≤ n−1, so has a basis {h1,…,h m−1 }. If H ⊂ Zn−1, we are
done. Otherwise, the image of H under the projection π : Zn → Z onto
n
thenthfactorisanontrivialcyclicsubgroupofZ.Letc∈Zbeagenerator
of this subgroup, and let h be an element of H such that π (h ) = c.
m n m
The proof will be complete once we show that {h1,…,h
m
} is a basis for
H.
Suppose a1h1 +···+a
m
h
m
= 0. Applying π
n
to this equation yields
a m c = 0, so a m = 0. Then a1 = ··· = a m−1 = 0 because of the inde-
pendence of {h1,…,h m−1 }, so {h1,…,h m } is linearly independent. Now
suppose h ∈ H is arbitrary. Then π (h) = ac for some integer a, so
n
h−ah ∈H∩Zn−1. This element can be written as a linear combination
m
of {h1,…,h m−1 }, which shows that H is generated by {h1,…,h m }.
We will need to extend the notion of rank to finitely generated abelian
groups that are not necessarily free abelian. To that end, we say that an
element g of an abelian group G is a torsion element if ng = 0 for some
nonzero n ∈ Z. If ng = n(cid:5)g(cid:5) = 0, then nn(cid:5)(g +g(cid:5)) = 0, so the set of all
torsion elements is a subgroup Gtor of G, called the torsion subgroup. We
saythatGistorsion freeiftheonlytorsionelementis0.Itiseasytocheck
that the quotient group G/Gtor is torsion free.

---

206 9. Some Group Theory
Proposition 9.14. Anyabeliangroupthatisfinitelygeneratedandtorsion
free is free abelian of finite rank.
Proof. SupposeGissuchagroup.ForanylinearlyindependentsubsetS ⊂
G, we will extend our notation slightly and let Z(cid:22)S(cid:23) denote the subgroup
of G generated by S. It is easily seen to be free abelian with S as a basis,
so this is consistent with our earlier notation.
The crux of the proof is the following claim: There exists a nonzero
integer n and a finite linearly independent set S ⊂G such that nG⊂Z(cid:22)S(cid:23).
Assuming this, the rest of the proof goes as follows. Let ϕ: G → G be
the homomorphism ϕ(g) = ng. It is injective because G is torsion free,
and the claim implies that ϕ(G) ⊂ Z(cid:22)S(cid:23). Thus G is isomorphic to the
subgroup ϕ(G) of the free abelian group Z(cid:22)S(cid:23), so by Proposition 9.13, G
is free abelian of finite rank.
We will prove the claim by induction on the number of elements in a
generating set for G. If G is generated by one element g, the claim is true
with n = 1, because the fact that G is torsion free implies that {g} is a
linearly independent set.
Now assume that the claim is true for any torsion-free group generated
by m−1 elements, and suppose G is generated by a set T ={g1,…,g
m
}
with m elements. If T is linearly independent, we just take S = T. If not,
there is a relation of the form a1g1+···+a
m
g
m
= 0 with at least one of
the coefficients, say a , not equal to zero. Letting G(cid:5) denote the subgroup
m
of G generated by {g1,…,g m−1 }, this means that a m g m ∈G(cid:5). Since G(cid:5) is
generated by m−1 elements, by induction there exist a nonzero integer n(cid:5)
and a finite linearly independent set S ⊂ G(cid:5) such that n(cid:5)G(cid:5) ⊂ Z(cid:22)S(cid:23). Let
n=a n(cid:5). Since G is generated by T, for any g ∈G we have
m
ng =a
m
n(cid:5)(b1g1+···+b
m
g
m
)
=n(cid:5)(a
m
b1g1+···+a
m
b m−1g m−1)+n(cid:5)b
m
(a
m
g
m
).
Both terms above are in n(cid:5)G(cid:5) ⊂ Z(cid:22)S(cid:23). It follows that nG ⊂ Z(cid:22)S(cid:23), which
completes the proof.
Now let G be any finitely generated abelian group. Because G/Gtor is
finitely generated and torsion free, the preceding proposition implies that
it is free abelian of finite rank. Thus we can define the rank of G to be the
rank of G/Gtor.
Example 9.15. The rank of Zn is n, and the rank of any finite group
is 0 (since every element is a torsion element). The rank of a product
group of the form G = Zn ×Z/(cid:22)k1 (cid:23)×···×Z/(cid:22)k
m
(cid:23) is n, because Gtor =
Z/(cid:22)k1 (cid:23)×···×Z/(cid:22)k
m
(cid:23).
Proposition 9.16. If G is a free abelian group of finite rank and f: G→
H is a surjective homomorphism, then rankG=rankH +rank(Kerf).

---

Free Abelian Groups 207
Proof. Write K = Kerf. By Proposition 9.13, K is a finitely generated
free abelian group, so we can choose elements k1,…,k
p
∈ G that form a
basis for K.
Sincef issurjective,ittakesasetofgeneratorsforGtoasetofgenerators
for H; thus H is finitely generated and its rank is the rank of H/Htor.
Chooseabasis (cid:7) h1,…, (cid:7) h
q
forH/Htor,andliftthemtoelementsh1,…,h
q
∈
H. By surjectivity, there are elements g ∈G such that f(g )=h .
j j j
Th(cid:15)e set {k
i
,g(cid:15)j } is linearly independent, because a relation of the form
g = m k + n g =0 implies
i i i j j j
(cid:14) (cid:14)
0=f(g)= n f(g )= n h .
j j j j
j j
Projecting
(cid:15)
this to the quotient group H/Htor, we obtain a relation of
(cid:7)
the (cid:15)form
j
n
j
h
j
= 0, which implies n
j
= 0 for each j. Therefore,
g = m k =0, so m =0.
i i i i
Let Z(cid:22)k ,g (cid:23) denote the subgroup of G generated by {k ,g }. It is free
i j i j
abelian of rank p + q = rankK + rankH, so from Proposition 9.13 we
conclude that rankK+rankH ≤rankG. The proof will be complete once
we show the reverse inequality.
Because Htor is a finitely generated torsion group, there is an integer
N such that Nt = 0 for every t ∈ Htor. Let g ∈ G be arbitrary, and let
[f(g)] den
(cid:15)
ote the equivalence class
(cid:15)
of f(g) in the quotient
(cid:15)
H/Htor. Writing
[f(g)]=
j
n
j
(cid:7) h
j
, w(cid:15)e have [f(g−
j
n
j
g
j
)]=0, so f(g−
j
n
j
g
j
)∈Htor.
This implies N(g− n g )∈K, so we can write
j j j
(cid:14) (cid:14)
Ng = Nn g + m k .
j j i i
j i
Letting ϕ: G → G be the homomorphism ϕ(g) = Ng as in the proof
of Proposition 9.14, we have shown that ϕ(G) ⊂ Z(cid:22)k ,g (cid:23). Moreover, ϕ is
i j
injectivebecauseGistorsionfree,sobyProposition9.13againweconclude
that rankG≤p+q =rankK+rankH.

---

208 9. Some Group Theory
Problems
9-1. Showthatanyfreeproductoftwoormorenontrivialgroupsisinfinite
and nonabelian.
9-2. Show that the following groups have the given presentations.
(a) Z/(cid:22)n(cid:23)∼ =(cid:22)β |βn =1(cid:23).
(b) Z/(cid:22)m(cid:23)×Z/(cid:22)n(cid:23)∼ =(cid:22)β,γ |βm =1, γn =1, βγ =γβ(cid:23).
9-3. The center of a group G is the set Z of elements of G that commute
with every element of G: Z ={g ∈G:gh=hg for all h∈G}. Show
that a free group on two or more generators has center consisting of
the identity alone.
9-4. Let G1,G2,H1,H2 be groups, and let f
i
: G
i
→ H
i
be group homo-
morphisms for i=1,2.
(a) Using the characteristic property of the free product, show that
there is a unique homomorphism f1 ∗f2: G1 ∗G2 → H1 ∗H2
such that the following diagram commutes for i=1,2:
G1 ∗G2
f1 ∗f2(cid:2)
H1 ∗H2
(cid:8) (cid:8)
ι
i
ι(cid:5)
i
(cid:2)
G H ,
i f i
i
where ι
i
: G
i
→G1 ∗G2 and ι(cid:5)
i
: H
i
→H1 ∗H2 are the canonical
injections.
(b) Show that Kerf1 ∗f2 = Imj1 ∗j2, where j
i
: Kerf
i
(cid:9)→ G
i
is
inclusion:
Kerf1 ∗Kerf2 j−1∗ →j2 G1 ∗G2 f−1∗ →f2 H1 ∗H2.
9-5. Show that the free abelian group on a set S is uniquely determined
up to isomorphism by the characteristic property (Lemma 9.11(a)).
9-6. Suppose G is a free abelian group of finite rank. Show that every
basis of G is finite.

---

10
The Seifert–Van Kampen Theorem
In this section we will develop the techniques needed to compute the fun-
damental groups of all compact surfaces, and a good many other spaces
as well. The basic tool is the Seifert–Van Kampen theorem, which gives a
formula for the fundamental group of a space that can be decomposed as
the union of two open, path connected subsets whose intersection is also
path connected.
Inthefirstsectionwestatearathergeneralversionofthetheorem.Then
we examine two special cases in which the formula simplifies considerably.
The first special case is that in which the intersection of the two subsets is
simply connected: Then the theorem says that the fundamental group of
thebigspaceisthefreeproductofthefundamentalgroupsofitssubspaces.
Asanapplication,wecomputethefundamentalgroupsofawedgeofspaces
and of a graph (a one-dimensional simplicial complex). The second special
caseisthatinwhichoneofthetwosubsetsisitselfsimplyconnected:Then
the fundamental group of the big space is the quotient of the fundamental
group of the non–simply connected piece by the path classes in the inter-
section. We use this formula to compute the fundamental groups of the
compact surfaces.
Aftertheseapplications,wegiveadetailedproofoftheSeifert–VanKam-
pen theorem. Then in the last section of the chapter we revisit the classi-
fication of compact surfaces, and prove finally that the different surfaces
on our list are all topologically distinct by showing that their fundamental
groups are not isomorphic.

---

210 10. The Seifert–Van Kampen Theorem
Statement of the Theorem
Here is the situation in which we will be able to compute fundamental
groups. Suppose we are given a space X that is the union of two open
subsets U,V ⊂ X, and suppose we can compute the fundamental groups
of U, V, and U∩V, each of which is path connected. As we will see below,
any loop in X can be written as a product of loops, each of which lies in
either U or V; such a loop can be thought of as representing an element of
thefreeproductπ1(U)∗π1(V).ButanyloopinU∩V willrepresentonlya
single element of π1(X), even though it represents two distinct elements of
the free product (one in π1(U) and one in π1(V)). Thus the fundamental
group of X can be thought of as the quotient of this free product modulo
some relations coming from π1(U ∩V) that express this redundancy.
Let us set the stage for the precise statement of the theorem. Let X be
any topological space, let U,V ⊂X be open subsets whose union is X and
whose intersection is nonempty, and choose any base point q ∈U∩V. The
four inclusion maps
U
(cid:3)(cid:4) (cid:6)
i (cid:3) (cid:6)k
(cid:3) (cid:6)(cid:7)
U ∩V X
(cid:6) (cid:3)(cid:4)
j (cid:6) (cid:3)l
(cid:6)(cid:7) (cid:3)
V
induce fundamental group homomorphisms
π1(U,q)
(cid:3)(cid:4) (cid:6)
i∗ (cid:3) (cid:6)k∗
(cid:3) (cid:6)(cid:7)
π1(U ∩V,q) π1(X,q).
(cid:6) (cid:3)(cid:4)
j∗ (cid:6) (cid:3)l∗
(cid:6)(cid:7) (cid:3)
π1(V,q)
Now insert the free product group π1(U,q)∗π1(V,q) into the middle of
the picture, and let ι
U
: π1(U,q) (cid:9)→ π1(U,q)∗π1(V,q) and ι
V
: π1(V,q) (cid:9)→
π1(U,q)∗π1(V,q) be the canonical injections. By the characteristic prop-
erty of the free product, k∗ and l∗ induce a homomorphism Φ: π1(U,q)∗
π1(V,q)→π1(X,q) such that the right half of the following diagram com-

---

Statement of the Theorem 211
mutes:
π1(U,q)
(cid:3)(cid:4) (cid:6)
(cid:3)
(cid:6)
(cid:3)
(cid:6)
(cid:3)
i∗(cid:3) ι U (cid:6) k∗
(cid:6)
(cid:3)
(cid:6)
(cid:3)
(cid:6)
(cid:3) (cid:5) (cid:6)(cid:7)
π1(U ∩V,q) F(cid:2) π1(U,q)∗π1(V,q) Φ(cid:2) π1(X,q). (10.1)
(cid:6) (cid:8) (cid:3)(cid:4)
(cid:3)
(cid:6)
(cid:3)
(cid:6)
(cid:3)
j∗ (cid:6) ι V (cid:3) l∗
(cid:6)
(cid:3)
(cid:6)
(cid:3)
(cid:6)
(cid:6)(cid:7) (cid:3)
π1(V,q)
Finally, we define a map F: π1(U ∩V,q) → π1(U,q)∗π1(V,q) by setting
F(γ) = (i∗γ)−1(j∗γ). (F is not a homomorphism.) Let F(π1(U ∩V,q))
denote the normal closure of the image of F in π1(U,q)∗π1(V,q).
Theorem 10.1 (Seifert–Van Kampen). Let X be a topological space.
Suppose U,V ⊂X are open subsets whose union is X, and suppose U, V,
and U ∩V are path connected. Then, for any q ∈ U ∩V, the homomor-
phism Φ defined by (10.1) is surjective, and its kernel is F(π1(U ∩V,q)).
Therefore,
(cid:30)
π1(X,q) ∼ =π1(U,q)∗π1(V,q) F(π1(U ∩V,q)). (10.2)
When the fundamental groups in question are finitely presented, the
theorem has a useful reformulation in terms of generators and relations.
Corollary 10.2. In addition to the hypotheses of the Seifert–Van Kampen
theorem, assume that the fundamental groups of U, V, and U∩V have the
following finite presentations:
π1(U,q) ∼ =(cid:22)α1,…,α
m
|ρ1,…,ρ
r
(cid:23);
π1(V,q) ∼ =(cid:22)β1,…,β
n
|σ1,…,σ
s
(cid:23);
π1(U ∩V,q) ∼ =(cid:22)γ1,…,γ
p
|τ1,…,τ
t
(cid:23).
Then π1(X,q) has the presentation
π1(X,q)
∼ =(cid:22)α1,…,α
m
,β1,…,β
n
|ρ1,…,ρ
r
,σ1,…,σ
s
,u1 =v1,…,u
p
=v
p
(cid:23),

---

212 10. The Seifert–Van Kampen Theorem
whereforeacha=1,…,p,u
a
isanexpressionfori∗γ
a
∈π1(U,q)interms
of the generators {α1,…,α
m
}, and v
a
similarly expresses j∗γ
a
∈ π1(V,q)
in terms of {β1,…,β
n
}.
Theproofsofthesetwotheoremsarerathertechnical,sowewillpostpone
themuntillaterinthechapter.Beforeprovingthem,wewillillustratetheir
use by computing a number of fundamental groups.
It is worth remarking here that the Seifert–Van Kampen theorem can
be generalized to a covering of X by any number, finite or infinite, of path
connected open sets containing the base point. This generalization can be
found in [Sie92] or [Mas89].
Applications
AllofourapplicationsoftheSeifert–VanKampentheoremwillbeinspecial
cases in which one of the sets U, V, or U ∩V is simply connected.
First Special Case: Simply Connected Intersection
The first special case of the Seifert–Van Kampen theorem we will con-
sider is that in which U ∩V is simply connected. In that case, the group
F(π1(U ∩V,q)) is trivial, so the following corollary is immediate.
Corollary 10.3. Assume the hypotheses of the Seifert–Van Kampen the-
orem, and suppose in addition that U ∩V is simply connected. Then Φ is
an isomorphism between π1(U,q)∗π1(V,q) and π1(X,q).
As our first application, we will compute the fundamental group of
a wedge of spaces. Recall from Example 3.25 that the wedge of spaces
X1,…,X n(cid:6)withbasepointsq
j
∈X
j
isthespaceX1 ∨···∨X
n
definedasthe
quotient of
j
X
j
by the equivalence relation generated by q1 ∼···∼q
n
.
A point q in a topological space X is said to be a nondegenerate base
point if q has a neighborhood that admits a strong deformation retraction
ontoq and{q}isclosedinX.Forexample,anybasepointinamanifoldis
nondegenerate, because any Euclidean ball neighborhood admits a strong
deformation retraction onto any point. (In more advanced treatments of
homotopy theory a slightly more restrictive definition of nondegenerate
base point is used, but this one will(cid:6)suffice for our purposes.)
Observe that inclusion of X into X followed by projection onto the
j j j
quotient induces continuous injective maps ι
j
: X
j
(cid:9)→ X1 ∨ ··· ∨ X
n
. If
each base point q is nondegenerate, then these are closed maps and thus
j
embeddings. Identifying each X with its image under ι , we will consider
j j
X
j
asasubspaceofX1 ∨···∨X
n
.Welet∗denotethepointinX1 ∨···∨X
n
that is the equivalence class of the base points q1,…,q
n
.

---

Applications 213
Lemma 10.4. Suppose q ∈ X is a nondegenerate base point for i =
i i
1,…,n. Then ∗ is a nondegenerate base point in X1 ∨···∨X
n
.
Proof. For each i, choose a neighborhood U
i
of q
i
that admits a(cid:6)strong
defor(cid:6)mationretractionH
i
: U
i
×I →U
i
onto{q
i
}.DefineamapH:
i
U
i
×
I →
i
U
i
bylettingH =H i(cid:6)onU
i
×I.Therestrictionofthequotientmap
π to the saturated open set U is a quotient map to a neighborhood U
i i
of ∗. Since π◦H respects the identifications made by π, it descends to the
quotient and yields a strong deformation retraction of U onto {∗}. To see
that {∗} is closed in X1 ∨···∨X
n
, we need only observe that its inverse
imageunderπ is{q1,…,q
n
},whichisclosedinthedisjointunionbecause
its intersection {q } with X is closed in X by hypothesis. Thus {∗} is
i i i
closed.
Proposition 10.5. Let X1,…,X
n
be spaces with nondegenerate base
points q ∈X . The map
j j
Φ: π1(X1,q1)∗···∗π1(X
n
,q
n
)→π1(X1 ∨···∨X
n
,∗)
induced by ι
j∗
: π1(X
j
,q
j
)→π1(X1 ∨···∨X
n
,∗) is an isomorphism.
Proof. FirstconsiderthewedgeoftwospacesX1 ∨X2.Wewouldliketouse
Corollary10.3totheSeifert–VanKampentheoremwithU =X1,V =X2,
andU∩V ={q}.ThetroubleisthatthesespacesarenotopeninX1 ∨X2,
so the corollary does not apply directly. To remedy this, we replace them
by slightly “thicker” spaces using the nondegenerate base point condition.
Choose neighborhoods W in which q is a strong deformation retract,
i i
andletU =π(X1 (cid:20)W2),V =π(X2 (cid:20)W1),whereπ: X1 (cid:20)X2 →X1 ∨X2 is
the quotient map (Figure 10.1). Since X1 (cid:20)W2 and X2 (cid:20)W1 are saturated
opensetsinX1 (cid:20)X2,therestrictionofπ toeachofthemisaquotientmap
and U and V are open in the wedge.
The key fact is that the three inclusion maps
{∗}(cid:9)→U ∩V,
X1 (cid:9)→U,
X2 (cid:9)→V
areallhomotopyequivalences,becauseeachsubspaceontheleft-handside
aboveisastrongdeformationretractofthecorrespondingright-handside.
For U ∩ V, this follows immediately from the preceding lemma. For U,
choose a strong deformation retraction H2: W2 ×I → W2 of W2 onto q2,
and define G1: X1 (cid:20)W2 ×I →X1 (cid:20)W2 to be the identity on X1 ×I and
H2 onW2 ×I;itdescendstoastrongdeformationretractionofU ontoX1.
A similar construction shows V (cid:25)X2.

---

214 10. The Seifert–Van Kampen Theorem
X1
W1 q1 q2 W2 X2
π
V
∗
X1 ∨X2
U
FIGURE 10.1. Computing the fundamental group of a wedge.
Because U ∩V is contractible, Corollary 10.3 implies that the inclusion
maps U (cid:9)→X1 ∨X2 and V (cid:9)→X1 ∨X2 induce an isomorphism
π1(U,∗)∗π1(V,∗)→π1(X1 ∨X2,∗).
Moreover,theinjectionsι1: X1 (cid:9)→U andι2: X2 (cid:9)→V,whicharehomotopy
equivalences,induceisomorphismsπ1(X1,q1)→π1(U,∗)andπ1(X2,q2)→
π1(V,∗).Composingtheseisomorphismsprovesthepropositioninthecase
n=2. The case of n>2 spaces follows by induction, because Lemma 10.4
guarantees that the hypotheses of the proposition are satisfied by X1 and
X2 ∨···∨X
n
.
Example 10.6. The preceding proposition shows that the bouquet S1 ∨
···∨S1 ofncircleshasfundamentalgroupisomorphictoZ∗···∗Z,whichis
afreegrouponngenerators.In fact,itshowsmore:Sincetheisomorphism
is induced by inclusion of each copy of S1 into the bouquet, we can write
explicitgeneratorsofthisfreegroup.Ifα denotesthestandardloopinthe
i
ith copy of S1, then the fundamental group of the bouquet is just the free
group (cid:22)[α1],…,[α
n
](cid:23).
As a second application, we will compute the fundamental group of a
finite graph. Let Γ be a finite connected graph, and choose a vertex v as
base point. A maximal tree in Γ is a subgraph that is a tree and is not
contained in any larger tree. The vertex v is contained in a (nonunique)
maximal tree: Just start with a single edge containing v and keep adding
edges until it is impossible to add another edge and still obtain a tree. Let
T ⊂Γ be such a maximal tree.

---

Applications 215
w1
w(cid:5)
1
w3
w(cid:5)
3
v
w2
w(cid:5)
2
FIGURE 10.2. Generators for the fundamental group of a graph.
We will construct a set of generators for the fundamental group of Γ
as follows. Let (cid:22)w1,w
1
(cid:5)(cid:23),…,(cid:22)w
n
,w
n
(cid:5)(cid:23) be the edges of Γ that are not in T
(Figure 10.2). For each i, by maximality of T there is a reduced cycle in
T ∪(cid:22)w ,w(cid:5)(cid:23) that does not lie in T. This cycle must therefore traverse the
i i
edge(cid:22)w ,w(cid:5)(cid:23),whichimpliesthatbothoftheverticesw andw(cid:5) alsobelong
i i i i
to edges in T. Thus we can choose paths g and h in T from v to w and
i i i
w(cid:5), respectively. Let f denote the loop in Γ obtained by first following g
i i i
fromv tow ,thentraversing(cid:22)w ,w(cid:5)(cid:23),andthenfollowingh −1 fromw(cid:5) back
i i i i i
tov.Notethatthepathclass[f ]isindependentofthechoicesofg andh ,
i i i
because any two paths in T with the same endpoints are path homotopic.
Theorem 10.7 (Fundamental Group of a Finite Graph). Thefun-
damental group of a finite connected graph Γ based at a vertex v is the free
group on the path classes [f1],…,[f
n
] constructed above.
Proof. We prove the theorem by induction on n. If n=0, then Γ is a tree
and hence simply connected, so there is nothing to prove.
For n = 1, we must show that Γ is the infinite cyclic group generated
by [f1]. By assumption, there is a reduced cycle (v0,…,v
m
) in Γ (Figure
10.3(a)). If v
i
=v
j
for some i(cid:14)=j other than v0 =v
m
, we can replace the
cycle by the shorter one (v ,…,v ). So we may assume that no vertex is
i j
repeated in this cycle except v0 = v
m
. This cycle must traverse the edge
(cid:22)w1,w
1
(cid:5)(cid:23),becauseotherwiseitwouldbeareducedcycleinT.Thesubgraph
C ⊂ Γ consisting of the vertices {v0,…,v
m
} and the intervening edges is
homeomorphic to S1 because it is isomorphic as a simplicial complex to
the complex K of Example 5.7(d). We will show that inclusion C ⊂Γ is
m
a homotopy equivalence.
LetK betheunionofalltheedgesinΓ(cid:3)C togetherwiththeirvertices.
Each component K of K is a connected subgraph of Γ contained in T,
i
and is therefore a tree (since a reduced cycle in K would also be one
i
in T). Moreover, each such component shares exactly one vertex y with
i

---

216 10. The Seifert–Van Kampen Theorem
K1
w(cid:5)
1
x1 x2
y1
x
n
C
y2
y3 w1
x3
K2 K3
(a) n=1. (b) n>1.
FIGURE 10.3. Proof that the fundamental group of a graph is free.
C: If K ∩C contained two vertices y ,y(cid:5), it would be possible to find a
i i i
reduced cycle in T by following a reduced edge path in K from y to y(cid:5)
i i i
followed by the reduced edge path in C from y(cid:5) to y that does not pass
i i
through (cid:22)w1,w
1
(cid:5)(cid:23). (There must be at least one vertex in common because
Γ is connected.)
Now define a strong deformation retraction of Γ onto C as follows: On
eachK ,itisastrongdeformationretractionofK ontoy ,whichexistsby
i i i
Problem 7-13; and on C it is the identity. The resulting map is continuous
by the gluing lemma, and shows that Γ(cid:25)S1.
It remains to show that the path class [f1] is a generator of π1(Γ,v). Let
z be any vertex in C. The path a that starts at z and traverses each edge
of C in order at constant speed is clearly path homotopic to the standard
generator of S1 ≈ C (or its inverse). Choosing any path b from z to v
yields an isomorphism Φ
b
: π1(Γ,z)→π1(Γ,v) as in Theorem 7.11. Thus a
generator of π1(Γ,v) is Φ
b
[a]=[b−1·
a
·
b]. Since
b−1·
a
·
b is a path that
goes from v to w1, traverses (cid:22)w1,w
1
(cid:5)(cid:23), and returns to v, it is homotopic to
f1. (Remember that the path class of f1 is independent of which paths we
choose from v to w1 and w
1
(cid:5).) This completes the proof in the case n=1.
Now suppose n > 1, and assume that the theorem is true whenever
there are fewer than n edges in the complement of a maximal tree. We
will apply the Seifert–Van Kampen theorem in the following way. For each
i = 1,…,n, choose a point x in the interior of the edge (cid:22)w ,w(cid:5)(cid:23) (Figure
i i i
10.3(b)).LetU =Γ(cid:3){x1,…,x n−1 }andV =Γ(cid:3){x n }.BothU andV are
openinΓ,andjustasbeforeitiseasytoconstructdeformationretractions
to show that U ∩V (cid:25)T, U (cid:25)T ∪(cid:22)w ,w(cid:5)(cid:23), and V (cid:25)Γ(cid:3)Int(cid:22)w ,w(cid:5)(cid:23). By
n n n n
theinductivehypothesis,π1(V,v)=(cid:22)[f1],…,[f n−1](cid:23)andπ1(U,v)=(cid:22)[f
n
](cid:23).
Since U ∩ V is simply connected, Corollary 10.3 shows that π1(Γ,v) is
isomorphic to the free product of these two free groups, which is the free
group on [f1],…,[f
n
] as claimed.

---

Applications 217
Second Special Case: One Simply Connected Set
The other special case of the Seifert–Van Kampen theorem we will use is
thatinwhichoneoftheopensets,sayU,issimplyconnected.Inthatcase,
diagram (10.1) simplifies considerably. Because the top group π1(U,q) is
trivial,boththehomomorphismsi∗ andk∗ aretrivial,andthefreeproduct
in the middle reduces to π1(V,q). Moreover, the homomorphism Φ is just
equaltol∗,andthemapF isjustequaltoj∗,sotheentirediagramcollapses
to
π1(U
∩V,q)−j→∗ π1(V,q)−l→∗
π1(X,q).
The conclusion of the theorem reduces immediately to the following corol-
lary.
Corollary 10.8. Assume the hypotheses of the Seifert–Van Kampen the-
orem, and suppose in addition that U is simply connected. Then inclusion
l: V (cid:9)→X induces an isomorphism
(cid:30)
π1(X,q) ∼ =π1(V,q) j∗π1(U ∩V,q),
where j∗π1(U ∩V,q) is the normal closure of j∗π1(U ∩V,q) in π1(V,q). If
the fundamental groups of V and U ∩V have finite presentations
π1(V,q) ∼ =(cid:22)β1,…,β
n
|σ1,…,σ
s
(cid:23),
π1(U ∩V,q) ∼ =(cid:22)γ1,…,γ
p
|τ1,…,τ
t
(cid:23),
then π1(X,q) has the presentation
π1(X,q) ∼ =(cid:22)β1,…,β
n
|σ1,…,σ
s
,v1,…,v
p
(cid:23),
where v
a
is an expression for j∗γ
a
∈π1(V,q) in terms of {β1,…,β
m
}.
Wewillgivetwoapplicationsofthiscorollary.Thefirstistogiveanother
proof that Sn is simply connected when n≥2.
Another proof of Theorem 8.7. As in the previous proof, we take Sn =
U ∪V with U = Sn(cid:3){N} and V = Sn(cid:3){S}, both of which are simply
connected because they are homeomorphic toRn. Moreover, U∩V is path
connected because it is homeomorphic to Rn(cid:3){0}. Corollary 10.8 to the
Seifert–Van Kampen theorem says that for any point q ∈U ∩V, π1(Sn,q)
is isomorphic to a quotient of π1(V,q) by a certain subgroup. But this
quotient is trivial because π1(V,q) is itself trivial.
The next proposition will allow us to compute the fundamental groups
of all compact surfaces. Now it will become clear why we chose similar
notations for surface presentations and group presentations.

---

218 10. The Seifert–Van Kampen Theorem
v0
a
i
g
q
c
P
0
a
i
π
(cid:7)a
i
v(cid:7)
M
g(cid:7)
q(cid:7)
FIGURE 10.4. Proof of Proposition 10.9.
Proposition 10.9. Let M be a 2-manifold determined by a polygonal
surface presentation (cid:22)a1,…,a
n
| W(cid:23) with one face, in which all ver-
tices are identified to a single point. Then π1(M) has the presentation
(cid:22)a1,…,a
n
|W(cid:23).
Proof. First we set up some notation (see Figure 10.4). Let P be a regular
polygon in the plane with 2n sides, centered at the origin, and let π: P →
M denote the quotient map determined by the given presentation. Set
U = IntP and V = P (cid:3){0}, and let U (cid:7) = π(U), V (cid:7) = π(V) ⊂ M. Since
U and V are saturated open sets, the restrictions of π to U and V are
(cid:7) (cid:7) (cid:7) (cid:7)
quotientmaps,andtheirimagesU,V areopeninM.Moreover,U,V,and
U (cid:7) ∩V (cid:7) are all path connected because they are images of path connected
sets in P. Choose a base point q ∈U ∩V lying on the line segment from 0
tothevertexv0 onthey-axis,andletq(cid:7)=π(q)∈U (cid:7)∩V (cid:7) .Finally,letv(cid:7)∈M
denote the single vertex (the image of all the vertices of P). In general, we
will use symbols without tildes to denote sets, points, or paths in P, and
the same symbols with tildes to denote their images in M.
The restriction of π to U is a one-to-one quotient map and therefore a
homeomorphism. Since U is convex, it is simply connected, and therefore
(cid:7)
U is simply connected as well. Thus we will be able to use Corollary 10.2
oncewefindpresentationsforthefundamentalgroupsofV
(cid:7)
andU
(cid:7)∩V (cid:7)
.The
(cid:7)
details are a bit involved, but the basic idea is just that V is homotopy

---

Applications 219
equivalent to a bouquet of circles, so π1(V (cid:7) ,q(cid:7)) is a free group on the n
generators determined by a1,…,a
n
; and U
(cid:7)∩V (cid:7)
is homotopy equivalent to
acircle,soj∗π1(U (cid:7)∩V (cid:7) ,q(cid:7))istheinfinitecyclicgroupgeneratedbytheword
W in these generators.
Consider first V (cid:7) . Observe that its preimage V ⊂P is homotopy equiva-
lentto∂P,bythestraight-linehomotopyH thatmoveseachpointradially
outward to the boundary. The map π×Id: P ×I → M ×I is a quotient
map by Lemma 4.35 (or just by the closed map lemma). Since V ×I is a
saturated open subset of P ×I, the restriction of π×Id to it is a quotient
map. Because π ◦H respects the identifications of this quotient map, it
(cid:7) (cid:7)
descends to a strong deformation retraction H of V onto π(∂P):
V ×I H (cid:2) V
π×Id π
(cid:5) (cid:5)
V (cid:7) ×I (cid:7) (cid:2) V (cid:7) .
H
On ∂P, π identifies the edges in pairs and identifies all the vertices to
a point, so π(∂P) is homeomorphic to a bouquet of n circles, one for each
labela .(Toverifythis,youcan,forexample,constructquotientmapsfrom
i
2n disjoint intervals to S1∨···∨S1 and to π(∂P), both of which make the
(cid:7)
same identifications.) Therefore, π1(V,q) is a free group on n generators.
We need to identify these generators explicitly. For each i, let (cid:7)a denote
i
apathinM thattraversesthesingleedgelabeleda (theimageunderπ of
i
twoedgesofP)intheindicateddirection.SinceallverticesofP projectto
v(cid:7), (cid:7)a
i
is a loop based at v(cid:7). From Example 10.6, π1(S1∨···∨S1,v(cid:7)) is freely
generatedby[(cid:7)a1],…,[(cid:7)a
n
].Theisomorphismπ1(S1∨···∨S1,v(cid:7))→π1(V (cid:7) ,v(cid:7))
induced by inclusion takes these generators to themselves, thought of as
loops in V (cid:7) , so π1(V (cid:7) ,v(cid:7)) is the free group (cid:22)[(cid:7)a1],…,[(cid:7)a
n
](cid:23).
We are really interested in the base point q(cid:7), not v(cid:7). Let g be the radial
straight-line path from q to v0, let g(cid:7) = π ◦ g, a path from q(cid:7) to v(cid:7), and
consider the loops (cid:7)a(cid:5) based at q(cid:7), defined by
i
(cid:7)a(cid:5) =g(cid:7) · (cid:7)a · g(cid:7)−1.
i i
These are just the images of the loops (cid:7)a under the isomorphism from
i
π1(V (cid:7) ,v(cid:7)) to π1(V (cid:7) ,q(cid:7)) provided by the path g(cid:7)−1 as in Theorem 7.11, so we
conclude that π1(V (cid:7) ,q(cid:7)) is the free group (cid:22)[(cid:7)a(cid:5)
1
],…,[(cid:7)a(cid:5)
n
](cid:23).
Next we turn to U (cid:7)∩V (cid:7) . Since π is one-to-one on U ∩V, U (cid:7)∩V (cid:7) is home-
omorphic to U ∩V = IntP (cid:3){0}. Let C be the circle centered at 0 and
(cid:7)
passing through q, and let C be its image in M. (We may assume that q
is chosen close enough to 0 that C is contained in the interior of P.) A de-
formation retraction of IntP (cid:3){0} onto C is easily constructed by moving
each point radially inward or outward toward C at constant speed. Thus

---

220 10. The Seifert–Van Kampen Theorem
π1(U (cid:7)∩V (cid:7) ,q(cid:7)) is infinite cyclic, generated by the path class of any loop that
(cid:7)
goes around C once. Let c be a loop that goes counterclockwise around C,
and let (cid:7)c = π ◦c, a loop in U (cid:7) ∩V (cid:7) based at q(cid:7). Then π1(U (cid:7) ∩V (cid:7) ,q(cid:7)) is the
infinite cyclic group (cid:22)[(cid:7)c](cid:23).
Now Corollary 10.8 to the Seifert–Van Kampen theorem says that
π1(M,q(cid:7)) ∼ = (cid:22)[(cid:7)a(cid:5)
1
],…,[(cid:7)a(cid:5)
n
] | b(cid:23), where b is an expression for j∗[(cid:7)c] ∈ π1(V (cid:7) ,q(cid:7))
in terms of the generators [(cid:7)a(cid:5)],…,[(cid:7)a(cid:5) ]. So to complete the proof, we need
1 n
only find such an expression.
Thekeyobservationisthatg(cid:7)−1·
(cid:7)c
·
g(cid:7),aloopbasedatv(cid:7),ispathhomotopic
inV (cid:7) totheloopW (cid:8) obtainedfromW byreplacingeacha by(cid:7)a .Toseethis,
i i
we first work upstairs in P: Let H be the strong deformation retraction of
V onto ∂P, and set
F(s,t)=H(g−1·
c
·
g(s),t).
The map F is a homotopy from
g−1·
c
·
g to a path that goes once around
(cid:7)
∂P in the clockwise direction, and it descends to a homotopy in V from
g(cid:7)−1· (cid:7)c · g(cid:7)to W (cid:8) . It follows that
(cid:7)c∼g(cid:7) · g(cid:7)−1· (cid:7)c · g(cid:7) · g(cid:7)−1 ∼g(cid:7) · W (cid:8)· g(cid:7)−1 ∼W (cid:8)(cid:5),
where W (cid:8)(cid:5) is obtained from W by replacing each a by (cid:7)a(cid:5); the last equiva-
lence follows by inserting
g(cid:7)−1·
g(cid:7)between each pair
i
of sym
i
bols in the word
(cid:8)
W.
Thus we have shown that the generator [(cid:7)c] of π1(U (cid:7)∩V (cid:7) ,q(cid:7)) is mapped by
inclusion to [W (cid:8)(cid:5)] ∈ π1(V (cid:7) ,q(cid:7)), where [W (cid:8)(cid:5)] is obtained from W by replacing
each a
i
by [(cid:7)a(cid:5)
i
]. By Corollary 10.2, therefore, π1(M,q(cid:7)) has the presentation
(cid:22)[(cid:7)a(cid:5)],…,[(cid:7)a(cid:5) ] | [W (cid:8)(cid:5)](cid:23); relabeling the symbols a instead of [(cid:7)a(cid:5)] yields the
1 n i i
presentation given in the statement of the proposition.
Example 10.10. Using the results of this section, we have the following
presentations for the fundamental groups of compact, connected surfaces:
(a) π1(S2) ∼ =(cid:22) (cid:23) (the trivial group).
(b) π1(T2#···#T2)
∼ =(cid:22)β1,γ1,…,β
n
,γ
n
|β1γ1β
1
−1 γ
1
−1···β
n
γ
n
β
n
−1γ
n
−1 =1(cid:23).
(c) π1(P2#···#P2) ∼ =(cid:22)β1,…,β
n
|β
1
2···β
n
2 =1(cid:23).
In particular, for the torus this gives π1(T2) ∼ = (cid:22)β,γ | βγ = γβ(cid:23), which
agreeswiththeresultwederivedearlier.Inthecaseoftheprojectiveplane,
this gives π1(P2) ∼ =(cid:22)β |β2 =1(cid:23)∼ =Z/(cid:22)2(cid:23).

---

Proof of the Theorem 221
Proof of the Theorem
In this section we prove the Seifert–Van Kampen theorem (Theorem 10.1)
and its corollary about finite presentations (Corollary 10.2).
Proof of Theorem 10.1. Becausewewillbeconsideringpathsandtheirho-
motopy classes in various spaces, for this proof we will refine our notation
to specify explicitly where homotopies are assumed to lie. If a and b are
pathsinX thathappentolieinoneofthesubsetsU,V,orU∩V,wewill
use the notation
a∼b, a∼b, a ∼ b, a∼b
U V U∩V X
toindicatethataispathhomotopictobinU,V,U∩V,orX,respectively.
Wewrite[a]
U
forthepathclassofainπ1(U,q),andsimilarlyfortheother
sets.Thus,forexample,ifaisaloopinU∩V,thehomomorphismsinduced
by the inclusions i: U ∩V (cid:9)→U and k: U (cid:9)→X can be written
i∗([a] U∩V )=[a] U ,
k∗([a]
U
)=[a]
X
.
We will have to consider two different types of products: path class mul-
tiplication within any one fundamental group, and word multiplication in
the free product group. As usual, we will denote path and path class mul-
tiplication by a dot, as in
· ·
[a] [b] =[a b] .
U U U
To emphasize the distinction between the two products, we denote multi-
plication in the free product group by an asterisk, so, for example,
·
[a]
U
∗[b]
U
∗[c]
V
=[a b]
U
∗[c]
V
∈π1(U,q)∗π1(V,q).
Then the map Φ: π1(U,q)∗π1(V,q)→π1(X,q) can be written
Φ([a1]
U
∗[a2]
V
∗···∗[a m−1]
U
∗[a
m
]
V
)
· · · ·
=k∗[a1]
U
l∗[a2]
V
··· k∗[a m−1]
U
l∗[a
m
]
V
(10.3)
· · · ·
=[a1]
X
[a2]
X
··· [a m−1]
X
[a
m
]
X
· · · ·
=[a1 a2 ··· a m−1 a m ] X .
LetN denotethenormalclosureofF(π1(U∩V,q))inπ1(U,q)∗π1(V,q).
We need to prove three things: (1) Φ is surjective; (2) N ⊂KerΦ; and (3)
KerΦ⊂N.

---

222 10. The Seifert–Van Kampen Theorem
(cid:12) (cid:13) (cid:12) (cid:13) (cid:12) (cid:13)
a i+1 a i a i−1
n n n
a i+1 a
i
h i+1
h
h i−1
i
a
U
V
q
FIGURE 10.5. Proof that Φ is surjective.
Step 1: Φ is surjective. Let a: I →X be any loop in X based at q. By
the Lebesgue number lemma, we can choose n large enough that a maps
each subinterval [(i−1)/n,i/n] either into U or into V. (This is why it is
importantthatthesetsU andV beopen.)Lettinga denotetherestriction
i
of a to [(i−1)/n,i/n] (reparametrized so that its parameter interval is I),
the path class of a in X factors as
· ·
[a]
X
=[a1 ··· a
n
]
X
.
The problem with this factorization is that the paths a are not loops in
i
general. To remedy this, for each i = 1,…,n−1, choose a path h from
i
q to a(i/n) (Figure 10.5). If a(i/n) ∈ U ∩V, choose h to lie entirely in
i
U ∩V; otherwise, choose it to lie in whichever set U or V contains a(i/n).
(This is why the sets U, V, and U ∩V must all be path connected.) Then
set (cid:7)a i = h i−1 · a i · h − i 1 (where we let h0 and h n be the constant loop c q ),
so that each (cid:7)a is a loop based at q and lying entirely in either U or V. It
i
follows easily that a also factors as
· ·
[a]
X
=[(cid:7)a1 ··· (cid:7)a
n
]
X
.
Now consider the element
γ =[(cid:7)a1]
U
∗[(cid:7)a2]
V
∗···∗[(cid:7)a
n
]
V
∈π1(U,q)∗π1(V,q),

---

Proof of the Theorem 223
wherewechooseeitherU orV foreach(cid:7)a dependingonwhichsetcontains
i
its image. Then as in (10.3) above,
· ·
Φ(γ)=[(cid:7)a1 ··· (cid:7)a
n
]
X
=[a]
X
.
This proves that Φ is surjective.
Step 2: N ⊂KerΦ. If we can show that F(π1(U∩V,q)) is contained in
KerΦ,thenitsnormalclosureN willbecontainedinKerΦaswellbecause
KerΦ is normal.
Let [a] U∩V ∈π1(U ∩V,q) be arbitrary. Then
Φ◦F([a] U∩V )=Φ((i∗[a] U∩V )−1∗(j∗[a] U∩V ))
=Φ([a−1] ∗[a] )
U V
=[a−1·
a]
X
=1.
Step 3: KerΦ⊂N. This is the crux of the proof. Let
γ =[a1]
U
∗[a2]
V
∗···∗[a
k
]
V
∈π1(U,q)∗π1(V,q)
be an arbitrary element of the free product, and suppose that Φ(γ) = 1.
Using (10.3) again, this means that
· ·
[a1 ··· a
k
]
X
=1,
which is equivalent to
· ·
a1 ··· a
k
∼c
q
.
X
We need to show that γ ∈N.
· ·
LetH: I×I →X bethepathhomotopyfroma1 ··· a
k
toc
q
inX.By
the Lebesgue number lemma again, we can subdivide I×I into squares of
side1/nsothatH mapseachsquareS =[(i−1)/n,i/n]×[(j−1)/n,j/n]
ij
either into U or into V.
Let v denote the image under H of the vertex (i/n,j/n); and let a
ij ij
denote the restriction of H to the horizontal line segment [(i−1)/n,i/n]×
{j/n},andb therestrictiontotheverticalsegment{i/n}×[(j−1)/n,j/n],
ij
both suitably reparametrized on I (see Figure 10.6).
TherestrictionofH tothebottomedgeofI×I,wheret=0,isequalto
· ·
the path product a1 ··· a
k
. By taking n to be a sufficiently large power
of 2, we can ensure that the endpoints of the paths a in this product are
i

---

224 10. The Seifert–Van Kampen Theorem
a1n … a
in
… a
nn
H
a
ij
b i−1,j
b
ij
a i,j−1
S
ij
q
a10 … a i0 … a n0
FIGURE 10.6. Proof that KerΦ⊂N.
of the form i/n, so the path obtained by restricting H to the bottom edge
of the square can also be written
· · · · · · · ·
H0 ∼a1 ··· a k ∼(a10 ··· a p0) ··· (a r0 ··· a n0).
In the free product, this means that
· · · ·
γ =[a10 ··· a p0] U ∗···∗[a r0 ··· a n0] V .
We would like to factor this in the free product as [a10]
U
∗[a20]
U
∗··· and
soforth.Butthesepathsarenotloopsbasedatq,sowecannotyetusethis
relation directly. This is easy to fix as in Step 1: For each i and j, choose a
path h from q to v , staying in U∩V if v ∈U∩V, and otherwise in U
ij ij ij
or V; if v happens to be the base point q, choose h to be the constant
ij ij
loop c . Then define loops
q
(cid:7)a ij =h i−1,j · a ij · h − ij 1 , (cid:7) b ij =h i,j−1 · b ij · h − ij 1 , (10.4)
each of which lies entirely in U or V. Then γ can be factored as
γ =[(cid:7)a10]
U
∗[(cid:7)a20]
U
∗···∗[(cid:7)a n0]
V
. (10.5)
The main idea of the proof is this: We will show that modulo N, the
expression (10.5) for γ can be replaced by the corresponding expression
obtained by restricting H to the top edge of the first row of squares:
γ ≡[(cid:7)a11]
U
∗···∗[(cid:7)a n1]
V
(mod N).

---

Proof of the Theorem 225
Repeating this argument, we move up to the next row, and so forth by
induction, until we obtain
γ ≡[(cid:7)a1n ]
U
∗···∗[(cid:7)a
nn
]
V
(mod N).
But the entire top edge of I ×I is mapped by H to the point q, so each
(cid:7)a is equal to the constant loop c , and this last product is equal to the
in q
identity. This shows that γ ∈N, completing the proof.
Thus we need to prove the following inductive step: Assuming by induc-
tion that
γ ≡[(cid:7)a1,j−1]
U
∗···∗[(cid:7)a n,j−1]
V
(mod N), (10.6)
we need to show that γ is equivalent modulo N to the same expression
with j−1 replaced by j.
First we observe the following simple fact: Suppose a is a loop in U∩V.
Then [a] and [a] are in the same coset in the free product modulo N,
U V
because
[a] V ∗N =[a] U ∗([a] − U 1∗[a] V )∗N =[a] U ∗F([a] U∩V )∗N =[a] U ∗N.
Since N is normal, this also implies x∗[a] ∗y∗N = x∗[a] ∗N ∗y =
U U
x∗[a] ∗N ∗y = x∗[a] ∗y∗N for any x,y in the free product. Thus,
V V
as long as we are computing modulo N and a is a loop in U ∩V, we can
freely interchange [a] with [a] wherever either appears.
U V
Consider a typical square S , and suppose for definiteness that H maps
ij
S into V. The boundary of S , traversed clockwise starting at the lower
ij ij
· · −1· −1
left corner, is mapped to the path (b i−1,j a ij ) (b ij a i,j−1 ). By Lemma
7.12, this means that
a i,j−1 ∼b i−1,j · a ij · b − ij 1 . (10.7)
V
Using the definition (10.4) of the loops (cid:7)a and (cid:7) b , (10.7) yields
ij ij
(cid:7)a i,j−1 =h i−1,j−1 · a i,j−1 · h − i,j 1 −1
∼h i−1,j−1 · b i−1,j · a ij · b − ij 1· h − i,j 1 −1 (10.8)
V
∼(cid:7) b i−1,j · (cid:7)a ij ·(cid:7) b − ij 1 ,
V
since the interior factors of h ij and h i−1,j and their inverses cancel out.
Now start with the expression (10.6) for γ. For each factor [(cid:7)a i,j−1]
U
,
check whether the square S above it is mapped into U or V. If it is
ij

---

226 10. The Seifert–Van Kampen Theorem
mapped into V, then (cid:7)a i,j−1 must map into U∩V, and we can replace this
factor by [(cid:7)a i,j−1]
V
modulo N. Correct each factor whose square maps into
U similarly.
By (10.8),wecanreplaceeachsuchfactor[(cid:7)a i,j−1] V by[ (cid:7) b i−1,j ] V ∗[(cid:7)a ij ] V ∗
(cid:7) −1
[b ] , and similarly for the factors in U. Thus
ij V
γ ≡[ (cid:7) b0,j ] U ∗[(cid:7)a1j ] U ∗[ (cid:7) b1j ] − U 1∗···∗[ (cid:7) b n−1,j ] V ∗[(cid:7)a nj ] V ∗[ (cid:7) b nj ] − V 1 (mod N)
≡[(cid:7)a1j ]
U
∗···∗[(cid:7)a
nj
]
V
(mod N).
(cid:7)
Here we have used the facts that the interior b factors all cancel each
ij
(cid:7) (cid:7) (cid:7) (cid:7)
other out (replacing [b
ij
]
U
by [b
ij
]
V
when necessary), and b0j and b
nj
are
both equal to the constant loop c . This completes the inductive step and
q
thus the proof.
Proof of Corollary 10.2. To simplify the notation, let A and B denote the
free groups (cid:22)α1,…,α
m
(cid:23) and (cid:22)β1,…,β
n
(cid:23), respectively, and write R =
{ρ1,…,ρ
r
},S ={σ1,…,σ
s
},andG={u −
1
1 v1,…,u−
p
1v
p
},allconsidered
as subsets of A∗B. (Note that the relators τ in U ∩V do not enter into
i
∼
either the statement of the corollary or its proof.) Then π1(U,q) = A/R
∼
and π1(V,q) = B/S by hypothesis. We will consider these isomorphisms
as identifications, so Φ is a map from (A/R) ∗ (B/S) to π1(X,q). Let
π: A∗B → (A/R)∗(B/S) denote the homomorphism induced by the
projections A→A/R and B →B/S as in Problem 9-4.
TheSeifert–VanKampentheoremsaysthatΦissurjectiveandhaskernel
equal to F(π1(U ∩V,q)), which clearly contains π(G) by our choice of
the set G. In fact, it is equal to π(G): To see this, we need only verify
that π(G) includes all of F(π1(U ∩V,q)), which is to say every element of
(cid:12)the form (i∗γ)−1 (cid:13)(j∗γ) for γ ∈ π1(U ∩V,q). Consider the quotient group
(A/R)∗(B/S) /π(G).BydefinitionofG,eachelementoftheformu −1 v
i i
projects to 1 in this quotient, which is to say that u and v project to
i i
the same element. Given any γ ∈π1(U ∩V,q), express it as a word in the
generatorsγ1,…,γ
p
;theni∗γ andj∗γ willbeexpressedbythesameword,
but with γ replaced by u in one case and v in the other. This shows that
i i i
i∗γ andj∗γ projecttothesameelementinthequotient,whichmeansthat
(i∗γ)−1(j∗γ)∈π(G).
The composition
A∗B →π (A/R)∗(B/S)→Φ π1(X,q)
is also surjective. The corollary will follow from the first isomorphism the-
orem (Theorem A.13) once we show that its kernel is exactly R∪S∪G.
Clearly,RandS arecontainedinKer(Φ◦π).Also,π(G)⊂F(π1(U∩V,q)
byourchoiceofG,andthusπ(G)⊂KerΦ,whichmeansthatG∈Ker(Φ◦

---

Distinguishing Manifolds 227
π) as well. Therefore, the kernel of Φ◦π is a normal subgroup containing
R∪S∪G, so R∪S∪G⊂Ker(Φ◦π).
To prove the reverse inclusion, suppose w ∈ A∗B is a word such that
Φ◦π(w) = 1. This means that π(w) ∈ KerΦ = π(G) = π(G). (The last
equality follows because the homomorphic image of a normal subgroup
under a surjective map is normal; see Exercise A.25 in the Appendix.) In
other words, π(w)=π(g), where g is some element of G. This just means
that wg−1 ∈Kerπ, which by Problem 9-4 is equal to R∗S (thought of as
a subgroup of A∗B). This can be rewritten as w =hg for some h∈R∗S,
g ∈G. Since clearly R∪S∪G must contain R∗S and G, this means that
w ∈R∪S∪G, and the proof is complete.
Distinguishing Manifolds
Nowwearefinallyinapositiontofillthegapinourclassificationofsurfaces
by showing that the different surfaces on our list are actually topologically
distinct. We will do so by showing that their fundamental groups are not
isomorphic.Eventhisisnotcompletelystraightforward,becauseitinvolves
solvingtheisomorphismproblemforcertainfinitelypresentedgroups.But
inthiscasewecanreducetheproblemtoamuchsimplerprobleminvolving
abelian groups.
GivenagroupG,thecommutatorsubgroupofG,denotedby[G,G],isthe
normalclosureofthesetofallelementsoftheformαβα−1β−1forα,β ∈G.
Clearly,thequotientgroupG/[G,G]isalwaysabelian,andthecommutator
subgroup is trivial if and only if G itself is abelian. This quotient group
is denoted by Ab(G) and called the abelianization of G. It is clear that
isomorphic groups have isomorphic abelianizations. Ab(G) is the “largest”
abelian quotient of G, or equivalently the largest abelian homomorphic
image of G, in the sense that any other homomorphism into an abelian
group factors through the abelianization, as the following characteristic
property shows.
Theorem 10.11 (Characteristic Property of Abelianizations).
For any abelian group H and any homomorphism ϕ: G → H, there exists
a unique homomorphism ϕ(cid:7): Ab(G) → H such that the following diagram
commutes:
ϕ(cid:2)
G H
(cid:3)(cid:4)
π (cid:3)ϕ(cid:7)
(cid:5)(cid:3)
Ab(G).
Exercise 10.1. Prove Theorem 10.11.
Itisrelativelyeasytocomputetheabelianizationsofoursurfacegroups.

---

228 10. The Seifert–Van Kampen Theorem
Theorem 10.12. The fundamental groups of compact surfaces have the
following abelianizations:
Ab(π1(S2))={1};
Ab(π1(
(cid:31)
T2#· ·
!
·#T
"
2)) ∼ =Z2n;
n
Ab(π1(
(cid:31)
P2#· ·
!
·#P
"
2)) ∼ =Zn−1×Z/(cid:22)2(cid:23).
n
Proof. The case of the sphere is obvious, so consider first an orientable
surface of genus n, and let
G=(cid:22)β1,γ1,…,β
n
,γ
n
|β1γ1β
1
−1 γ
1
−1···β
n
γ
n
β
n
−1γ
n
−1(cid:23)
be the fundamental group. Define a map ϕ: Ab(G)→Z2n as follows. Let
e =(0,…,1,…,0)∈Z2n (1 in the ith place), and set
i
ϕ(β i )=e i , ϕ(γ i )=e i+n .
Thought of as a map from the free group (cid:22){β ,γ }(cid:23) into Z2n, this sends
i i
the element β1γ1β
1
−1 γ
1
−1···β
n
γ
n
β
n
−1γ
n
−1 to (0,…,0), so it descends to
a homomorphism from G to Z2n. By the characteristic property of the
abelianization, it also descends to a homomorphism (still denoted by ϕ)
from Ab(G) to Z2n.
To go back the other way, define ψ: Z2n →Ab(G) by
(cid:16)
[β ], 1≤i≤n,
ψ(e )= i
i [γ i−n ], n+1≤i≤2n,
where the brackets on the right-hand side denote the equivalence class in
Ab(G), and extend it to be a homomorphism. It is easy to check that ϕ
and ψ are inverses of each other.
Next consider the connected sum of projective planes, and let H =
(cid:22)β1,…,β
n
| β
1
2···β
n
2(cid:23). Write f for the nontrivial element of Z/(cid:22)2(cid:23), and
define ϕ: Ab(H)→Zn−1×Z/(cid:22)2(cid:23) by
(cid:16)
e , 1≤i≤n−1;
ϕ(β )= i
i f −e n−1 −···−e1, i=n.
As before, ϕ(β2···β2) = (0,…,0) by direct computation (noting that
1 n
f+f =0),soϕdescendstoAb(H).Thehomomorphismψ: Zn−1×Z/(cid:22)2(cid:23)→
Ab(H) defined by
ψ(e
i
)=[β
i
], ψ(f)=[β1 ···β
n
]
is easily verified to be an inverse for ϕ.

---

Distinguishing Manifolds 229
Corollary 10.13. Anycompact,connectedsurfaceishomeomorphictoex-
actly one of the surfaces S2, T2#···#T2, or P2#···#P2.
Proof. First note that the sphere cannot be homeomorphic to a connected
sumoftoriorprojectiveplanes,becauseonehastrivialfundamentalgroup
andtheotherdoesnot.Next,ifM isaconnectedsumofprojectiveplanes,
thenAb(π1(M))containsanontrivialtorsionelement,whereastheabelian-
ized fundamental groups of connected sums of tori are torsion free. There-
fore, no connected sum of projective planes can be homeomorphic to a
connected sum of tori. If M is a connected sum of n tori, then its abelian-
ized fundamental group has rank 2n. Thus the genus (i.e., the number of
tori in the connected sum) can be recovered from the fundamental group,
so the genus of an orientable surface is a topological invariant. Similarly,
a connected sum of n projective planes has abelianized fundamental group
of rank n−1, so once again the genus is a topological invariant.
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
|P| ≈ |Q|. Each of these presentations can be transformed into one of the
standard ones by elementary transformations, and since the surfaces rep-
resented by different standard presentations are not homeomorphic, both
presentations must reduce to the same standard one. Since the Euler char-
acteristic of a presentation is unchanged by elementary transformations,
the two presentations must have had the same Euler characteristic to be-
gin with.
Because of this corollary, we can define the Euler characteristic of a
compact surface M, denoted by χ(M), to be the Euler characteristic of
any presentation of that surface.

---

230 10. The Seifert–Van Kampen Theorem
Problems
10-1. Compute the fundamental group of each of the following spaces. (To
“compute” a fundamental group means to give a presentation of the
group together with a specific loop representing each generator.)
(a) A closed disk with two points removed.
(b) The projective plane with two points removed.
(c) The connected sum of n tori with one point removed.
(d) The connected sum of n tori with two points removed.
10-2. Give a purely algebraic proof that the groups (cid:22)α,β | αβαβ−1(cid:23) and
(cid:22)ρ,γ |ρ2γ2(cid:23)areisomorphic.[Hint:LookattheKleinbottleforinspi-
ration.]
10-3. Letnbeanintegergreaterthan2.Constructapolygonalpresentation
whosegeometricrealizationhasafundamentalgroupthatiscyclicof
order n.
10-4. SupposeM and N arecompact2-manifolds.Showthatanytwocon-
nected sums of M and N are homeomorphic.
10-5. Compute the fundamental group of the complement of the three co-
ordinate axes in R3. [Hint: This space is homotopy equivalent to the
2-sphere with six points removed.]
10-6. If M is a connected manifold of dimension at least 3 and q ∈ M,
show that π1(M (cid:3){q}) ∼ =π1(M).
10-7. Let M and N be connected n-manifolds, n ≥ 3. Prove that the fun-
damental group of M #N is isomorphic to π1(M)∗π1(N).
10-8. LetP bethepolyhedronofafinitesimplicialcomplexK,andassume
that P is connected. Show that the fundamental group of P has a
presentation with the same number of generators as π1(K(1)) and
one relation for each 2-simplex in K. [Hint: First treat the case of
a 2-dimensional complex by induction on the number of 2-simplices.
Then use a similar argument to show that inclusion K(j) (cid:9)→ K(j+1)
induces a fundamental group isomorphism for j ≥2.]
10-9. Let Γ be a finite connected graph. The Euler characteristic of Γ is
χ(Γ)=V−E,whereV isthenumberofverticesandE isthenumber
of edges. Show that the fundamental group of Γ is a free group on
1−χ(Γ)generators.Concludethatχ(Γ)isahomotopyinvariant,i.e.,
that homotopy equivalent graphs have the same Euler characteristic.
[Hint:FirstshowbyinductiononthenumberofedgesthattheEuler
characteristic of a finite tree is 1.]

---

Problems 231
0 2 4 … 2n−2
FIGURE 10.7. The space Xn of Problem 10-10.
10-10. Let X be the union of n circles of radius 1 centered at the points
n
{0,2,4,…,2n−2} in C, which are pairwise tangent to each other
along the x-axis (Figure 10.7). (Note that X2 is homeomorphic to
the figure eight space.) Prove that π1(X
n
,1) is a free group on n
generators, and describe explicit loops representing the generators.
10-11. Show that a connected, compact surface M is nonorientable if and
only if it contains a subset homeomorphic to the M¨obius band.
10-12. Let X ⊂R3 be the union of the unit 2-sphere with the line segment
{(0,0,z) : −1 ≤ z ≤ 1}. Compute π1(X,N), where N = (0,0,1) is
the north pole, giving explicit generator(s).
10-13. Show that abelianization defines a functor from GROUP to AB. (You
have to decide what the induced homomorphisms are.)
10-14. Given a group G, show that Ab(G) is the unique group that satisfies
the characteristic property expressed in Theorem 10.11.
10-15. IfG1 andG2 aregroups,showthatAb(G1 ∗G2) ∼ =Ab(G1)⊕Ab(G2).
Conclude as a corollary that the abelianization of a free group on n
generators is free abelian of rank n.

---

11
Covering Spaces
Sofarwehavedevelopedtwogeneraltechniquesforcomputingfundamental
groups.Thefirstishomotopyequivalence,whichcanoftenbeusedtoshow
thatonespacehasthesamefundamentalgroupasasimplerone.Thiswas
used in Chapter 7, for example, to show that every contractible space is
simply connected, and that the fundamental group of the punctured plane
is infinite cyclic. The second is the Seifert–Van Kampen theorem, which
wasusedinChapter10tocomputethefundamentalgroupsofspheresand
compact surfaces.
Theonlyotherfundamentalgroupwehavecomputedisthatofthecircle,
for which we used a technique that at first glance might seem to be rather
ad hoc. The strategy for computing π1(S1,1) in Chapter 8 was to use the
properties of the exponential quotient map ε to show that any loop based
at 1 in the circle lifts to a path in R that ends at an integer; this integer
is called the winding number of the loop, and different loops are path
homotopicifandonlyiftheyhavethesamewindingnumber.Anotherway
to express this result is that lifting provides a one-to-one correspondence
between the fiber of ε over 1 and the fundamental group of the circle.
The main ingredients in the proof were the three “lifting properties”
of the circle: the path lifting property (Lemma 8.3), the homotopy lifting
property(Lemma8.4),andtheuniqueliftingproperty(Lemma8.2).These,
in turn, followed from the basic fact that every point in the circle has an
evenly covered neighborhood.
In this chapter we introduce a far-reaching generalization of these ideas,
and show how the same techniques can be applied to a broad class of
topological spaces. This brings us to the last major subject in the course:

---

234 11. Covering Spaces
(cid:7)
X
p
q X
FIGURE 11.1. An evenly covered neighborhood of q.
covering spaces and covering maps. A covering map is a particular type
of quotient map that has many of the same properties as the exponential
quotient map. A careful study of covering maps will enable us to compute
and analyze many more fundamental groups.
Definitions and Basic Properties
Let X (cid:7) and X be topological spaces, and let p: X (cid:7) → X be a continuous
map. A subset U ⊂ X is said to be evenly covered by p if U is connected
and open, and each component of p−1(U) is an open set that is mapped
homeomorphically onto U by p (Figure 11.1). We usually visualize p−1(U)
as a “stack of pancakes” that are projected down onto U by p. It is easy
to see that any connected open subset of an evenly covered set is evenly
covered.
A covering map is a continuous surjective map p: X (cid:7) → X such that X (cid:7)
is path connected and locally path connected, and every point q ∈ X has
an evenly covered neighborhood. If p: X (cid:7) → X is a covering map, we call
(cid:7)
X a covering space of X, and X the base of the covering.
(Some authors define covering spaces more generally, omitting the re-
(cid:7)
quirement that X be locally path connected or path connected, or even
sometimes omitting any connectivity requirement at all. In that case vari-

---

Definitions and Basic Properties 235
ous connectivity hypotheses have to be added to the theorems below. We
havechosentoincludethesehypothesesinthedefinitionofcoveringmaps,
because most of the interesting results require them, such as the lifting
criterion, the covering group structure theorem, and the classification of
covering spaces, and this frees us from having to remember which connec-
tivity hypotheses are necessary for which theorems. In any case, connected
manifolds and most interesting spaces built from them will always satisfy
the hypotheses.)
Example 11.1. Theexponentialquotientmapε: R→S1 givenbyε(x)=
e2πix is a covering map; this is the content of Lemma 8.5.
Example 11.2. The nth power map p : S1 → S1 given by p (z) = zn is
n n
alsoacoveringmap.Foranyz0 ∈S1,thesetU =S1(cid:3){−z0 }haspreimage
equalto{z ∈S1 :zn (cid:14)=−z0 },whichhasncomponents,eachofwhichisan
open arc mapped homeomorphically by p onto U.
n
Example 11.3. Define E: Rn →Tn by
E(x1,…,x
n
)=(ε(x1),…,ε(x
n
)),
where ε is the exponential quotient map of Example 11.1. Since a product
of covering maps is a covering map (Problem 11-2), E is a covering map.
Example 11.4. Define a map π: Sn →Pn (n≥1) by sending each point
x in the sphere to the line through the origin and x, thought of as a point
in Pn. Then π is a covering map (Problem 11-1), and the fiber over each
point of Pn is a pair of antipodal points {x,−x}.
Exercise 11.1. Let Xn be the union of n circles in C as described in
Problem 10-10. Define a map p: X3 → X2 by letting A, B, and C denote
thecirclescenteredat0,2,and4,respectively(seeFigure11.2),anddefining
⎧
⎪⎨z, z∈A;
p(z)= 2−(z−2)2, z∈B;
⎪⎩
4−z, z∈C.
(In words, p is the identity on A, wraps B twice around itself, and reflects
C onto A). Show that p is a covering map.
Lemma 11.5 (Elementary Properties of Covering Maps). Every
coveringmapisalocalhomeomorphism,anopenmap,andaquotientmap.
A one-to-one covering map is a homeomorphism.
Exercise 11.2. Prove Lemma 11.5.
Itisimportanttorealizethatasurjectivelocalhomeomorphismmaynot
be a covering map, as the next example shows.

---

236 11. Covering Spaces
A B C
FIGURE 11.2. Two views of the map of Exercise 11.1.
Example 11.6. LetX (cid:7) betheinterval(0,2)⊂R,anddefinef: X (cid:7) →S1by
f(x) = e2πix (Figure 11.3). Then f is a local homeomorphism (because it
istherestrictionofthecoveringmapε),andisclearlysurjective.However,
f is not a covering map, as is shown in the following exercise.
Exercise 11.3. Prove that the map f in the preceding example is not
a covering map by showing that the point 1 ∈ S1 has no evenly covered
neighborhood.
Recall from Chapter 8 that a local section of a continuous map is a
continuous right inverse defined on some open subset.
Lemma 11.7 (Existence of local sections). Let p: X (cid:7) → X be a cov-
ering map. Given any evenly covered open set U ⊂ X, any q ∈ U, and
any q(cid:7) 0 in the fiber over q, there exists a local section σ: U →X (cid:7) such that
σ(q)=q(cid:7) 0.
Proof. LetU (cid:7) 0 bethecomponentofp−1(U)containingq(cid:7) 0.Sincetherestric-
tion of p to U (cid:7) 0 is a homeomorphism, we can just take σ =(p| (cid:7) )−1.
U0
Proposition 11.8. For any covering map p: X (cid:7) → X, the cardinality of
the fibers p−1(q) is the same for all fibers.
Proof. IfU isanyevenlycoveredopensetinX,eachcomponentofp−1(U)
contains exactly one point of each fiber. Thus, for any q,q(cid:5) ∈U, there are
one-to-one correspondences
p−1(q)↔{components of p−1(U)}↔p−1(q(cid:5)),
which shows that the number of components is constant on U. It follows
that the set of points q(cid:5) ∈X such that p−1(q(cid:5)) has the same cardinality as
p−1(q) is open.

---

Definitions and Basic Properties 237
(cid:7)
X
f
FIGURE 11.3. A surjective local homeomorphism that is not a covering
map.
Now choose any point q ∈X, and let A be the set of points in X whose
fibershavecardinalityequaltothatofp−1(q).ThenAisopenbytheabove
argument, and X (cid:3)A is open because it is a union of open sets (one for
each cardinality not equal to that of p−1(q)). Since X is connected and A
is not empty, A must be equal to X.
If p: X (cid:7) → X is a covering map, the cardinality of any fiber is called
the number of sheets of the covering. For example, the nth power map of
Example 11.2 is an n-sheeted covering; the map π: Sn → Pn of Example
11.4isatwo-sheetedcovering;andtheexponentialquotientmapε: R→S1
has countably many sheets.
Lifting Properties
The key technical tools for working with covering spaces are the following
three lifting properties, which are straightforward generalizations of the
ones we proved for the circle in Chapter 8. In fact, the proofs for the circle
apply almost verbatim to these more general propositions. We sketch the
proofs in streamlined form here; if you remember the arguments given in
Chapter 8, you can safely skip these proofs.
If p: X (cid:7) → X is a covering map and ϕ: B → X is any continuous map,
a lift of ϕ is a continuous map ϕ(cid:7): B →X (cid:7) such that p◦ϕ(cid:7)=ϕ:
(cid:7)
X
(cid:3)(cid:4)
ϕ(cid:7)(cid:3) p
(cid:3) (cid:5)
(cid:2)
B ϕ X.

---

238 11. Covering Spaces
Proposition 11.9 (Unique Lifting Property). Let p: X (cid:7) → X be a
covering map. Suppose B is connected, ϕ: B → X is continuous, and
ϕ(cid:7) 1,ϕ(cid:7) 2: B →X (cid:7) are lifts of ϕ that agree at some point of B. Then ϕ(cid:7) 1 ≡ϕ(cid:7) 2.
Proof. As in the proof of Lemma 8.2, it suffices to show that S={b∈B :
ϕ(cid:7) 1(b)=ϕ(cid:7) 2(b)} is open and closed in B.
For any b ∈ S, let U ⊂ X be an evenly covered neighborhood of ϕ(b),
and let U
α
be the component of p−1(U) containing ϕ(cid:7) 1(b)=ϕ(cid:7) 2(b). On the
neighborhood V =ϕ(cid:7)− 1 1 (U α )∩ϕ(cid:7)− 2 1 (U α ) of b, ϕ=p◦ϕ(cid:7) 1 =p◦ϕ(cid:7) 2. Since p is
injective on U α , this means ϕ(cid:7) 1 =ϕ(cid:7) 2 on V, so S is open.
On the other hand, for b(cid:14)∈S, if U is an evenly covered neighborhood of
ϕ(b),therearedisjointcomponentsU1,U2ofp−1(U)containingϕ(cid:7) 1(b),ϕ(cid:7) 2(b)
suchthatpisahomeomorphismfromeachU
i
toU.LettingV =ϕ(cid:7)−
1
1 (U1)∩
ϕ(cid:7)−
2
1 (U2),weconcludethatϕ(cid:7)
1
(cid:14)=ϕ(cid:7)
2
onV,whichshowsthatSisclosed.
Proposition 11.10 (Path Lifting Property). Letp: X (cid:7) →X beacov-
ering map. Suppose f: I →X is any path, and q(cid:7) 0 ∈X (cid:7) is any point in the
fiber of p over f(0). Then there exists a unique lift f (cid:7) : I → X (cid:7) of f such
that f (cid:7) (0)=q(cid:7) 0.
Proof. By the Lebesgue number lemma, n can be chosen large enough
that p maps each subinterval [k/n,(k+1)/n] into an evenly covered open
subset of X. Starting with f (cid:7) (0)=q(cid:7) 0, f (cid:7) is defined inductively by choosing
an evenly covered neighborhood U containing f[k/n,(k +1)/n], a local
k
sectionσ : U →X (cid:7) suchthatσ (f(k/n))=f (cid:7) (k/n),andsettingf (cid:7) =σ ◦f
k k k k
on [k/n,(k+1)/n]. Because p◦f (cid:7) = (p◦σ )◦f = f, this is indeed a lift,
k
and it is unique by the unique lifting property.
Proposition 11.11 (Homotopy Lifting Property). Let p: X (cid:7) → X
be a covering map. Suppose f0,f1: I → X are path homotopic, and
f (cid:7) 0,f (cid:7) 1: I →X (cid:7) are lifts of f0 and f1 such that f (cid:7) 0(0)=f (cid:7) 1(0). Then f (cid:7) 0 ∼f (cid:7) 1.
Proof. If H: f0 ∼f1 is a path homotopy, by the Lebesgue number lemma
we can choose n large enough that H maps each square of side 1/n into
an evenly covered open set. Labeling the squares S = [i/n,(i+1)/n]×
ij
(cid:7)
[j/n,(j+1)/n], we define a lift H of H square by square along the bottom
row, then along the next row, and so on by induction as in the proof of
Lemma 8.3. On each square S , set H (cid:7) = σ◦H, for an appropriate local
ij
(cid:7)
section σ chosen so that the new definition of H matches the previous one
atthecornerpoint(i/n,j/n).Onalinesegmentwheretwosuchdefinitions
overlap, both the old and new definitions are lifts of the path obtained by
restricting H to that segment, starting at the same point. Thus they are
equal by the unique lifting property.
On the left-hand and right-hand edges of I×I, where s=0 or s=1, H (cid:7)
(cid:7)
is a lift of the constant loop and therefore constant. The restriction H0 to

---

Covering Maps and the Fundamental Group 239
(cid:7)
thebottomedgewheret=0isaliftoff0 startingatf0(0),andthereforeis
(cid:7) (cid:7) (cid:7) (cid:7)
equal to f0; and similarly H1 =f1. Thus H is the required path homotopy
(cid:7) (cid:7)
between f0 and f1.
The next result is an immediate corollary of the homotopy lifting prop-
erty.
Corollary 11.12 (The Monodromy Theorem). Let p: X (cid:7) → X be a
(cid:7)
covering map. Suppose f0 and f1 are path homotopic paths in X, and f0,
(cid:7) (cid:7) (cid:7)
f1 are lifts of them starting at the same point. Then f0(1)=f1(1).
Covering Maps and the Fundamental Group
Ournexttheoremcharacterizesthefundamentalgrouphomomorphismin-
duced by a covering map.
Theorem 11.13 (Injectivity Theorem). Let p: X (cid:7) →X be a covering
map. For any point q(cid:7) ∈ X (cid:7) , the induced homomorphism p∗: π1(X (cid:7) ,q(cid:7)) →
π1(X,p(q(cid:7))) is injective.
Proof. Suppose [f] ∈ π1(X (cid:7) ,q(cid:7)) is in the kernel of p∗. This means that
p∗[f] = [c
q
], where q = p(q(cid:7)), or in other words, p ◦ f ∼ c
q
in X. By
the homotopy lifting property, therefore, any lifts of p◦f and c that start
q
at the same point must be path homotopic in X (cid:7) . Now, f is a lift of p◦f
starting at q(cid:7), and the constant loop c q(cid:7) is a lift of c q starting at the same
point; therefore, f ∼c q(cid:7) in X (cid:7) , which means that [f]=1.
This theorem shows that the fundamental group of a covering space can
be identified with a subgroup of the fundamental group of the base. We
call this the subgroup induced by the covering.
Example 11.14. Let p: X3 → X2 be the covering map of Exercise 11.1,
and choose 1 as base point in both X3 and X2. To compute the subgroup
induced by p, we need to compute the action of p on the generators of
π1(X3,1). Let a, b, c be loops that go once counterclockwise around each
circle A, B, and C, starting at 1, 1, and 3, respectively; and let b1 and b2
be the lower and upper halves of b, so b1 is a path from 1 to 3, b2 is a path
·
from 3 to 1, and b∼b1 b2. Using the result of Problem 10-10, π1(X3,1) is
· · −1
the free group on [a], [b], and [b1 c b
1
], and π1(X2,1) is the free group
on [a] and [b]. The images of these generators under p∗ are [a], [b]2, and
[b] · [a]−1· [b]−1, so the subgroup induced by p is the subgroup of (cid:22)[a],[b](cid:23)
generated by these three elements.
Asourfirstsignificantapplicationofthetheorywegiveageneralsolution
to the lifting problem for covering maps: This is the problem of deciding,
givenacontinuousmapϕ: Y →X,whetherϕadmitsaliftϕ(cid:7)toacovering

---

240 11. Covering Spaces
(cid:7)
space X of X. The following theorem reduces this topological problem to
an algebraic problem.
Theorem 11.15 (Lifting Criterion). Suppose p: X (cid:7) → X is a covering
map.LetY beaconnectedandlocallypathconnectedspace,andletϕ: Y →
X be a continuous map. Given any points y0 ∈ Y and q(cid:7) 0 ∈ X (cid:7) such that
p(q(cid:7) 0) = ϕ(y0), ϕ has a lift ϕ(cid:7): Y → X (cid:7) satisfying ϕ(cid:7)(y0) = q(cid:7) 0 if and only if
the subgroup ϕ∗π1(Y,y0) of π1(X,ϕ(y0)) is contained in p∗π1(X (cid:7) ,q(cid:7) 0).
Proof. The necessity of the algebraic condition is easy to prove (and, in
fact, does not require any connectivity assumptions about Y). If ϕ(cid:7) satis-
fies the conditions in the statement of the theorem, the following diagram
commutes:
π1(X (cid:7) ,q(cid:7) 0)
(cid:3)(cid:4)
(cid:3)
(cid:3)
ϕ(cid:7)
∗(cid:3)
p∗
(cid:3)
(cid:3) (cid:5)
(cid:2)
π1(Y,y0)
ϕ∗
π1(X,ϕ(y0)).
Therefore, ϕ∗π1(Y,y0)=p∗ϕ(cid:7) ∗π1(Y,y0)⊂p∗π1(X (cid:7) ,q(cid:7) 0).
To prove the converse, we will “lift ϕ along paths” using the path lifting
property. If ϕ(cid:7)does exist, it will have the following property: For any point
y ∈Y andanypathf fromy0 toy,ϕ(cid:7)◦f isaliftofϕ◦f startingatq(cid:7) 0,and
ϕ(cid:7)(y) is equal to the terminal point of this path. We use this observation to
define ϕ(cid:7): Namely, for any y ∈Y, choose a path f from y0 to y, let ϕ (cid:4)◦f be
the (unique) lift of the path ϕ◦f to a path in X (cid:7) starting at q(cid:7) 0, and set
ϕ(cid:7)(y)=ϕ (cid:4)◦f(1).
We need to show two things: (1) ϕ(cid:7) is well-defined, independently of the
choice of the path f; and (2) ϕ(cid:7) is continuous. Then it is immediate from
the definition that p◦ϕ(cid:7)(y) = p◦ϕ (cid:4)◦f(1) = ϕ◦f(1) = ϕ(y), so ϕ(cid:7) is a lift
of ϕ.
Claim 1: ϕ(cid:7) is well-defined. Suppose f and f(cid:5) are two paths from y0 to
y (Figure 11.4). Then f(cid:5)· f−1 is a loop based at y0, so
ϕ∗[f(cid:5)· f−1]∈ϕ∗π1(Y,y0)⊂p∗π1(X (cid:7) ,q(cid:7) 0).
This means that [ϕ◦(f(cid:5)· f−1)]=[p◦g] for some loop g in X (cid:7) based at q(cid:7) 0.
Thus we have the following path homotopy in X:
p◦g ∼ϕ◦(f(cid:5)· f−1)=(ϕ◦f(cid:5)) · (ϕ◦f)−1,

---

Covering Maps and the Fundamental Group 241
(cid:7)
X
ϕ(cid:7)(y)
ϕ
(cid:4)◦f
g
q(cid:7)
0 ϕ
(cid:5)◦f(cid:5)
ϕ(cid:7)
p
f
Y ϕ(y)
ϕ ϕ◦f X
y p◦g
y0 ϕ(y0) ϕ◦f(cid:5)
f(cid:5)
FIGURE 11.4. Proof that ϕ(cid:7)is well-defined.
which implies
(p◦g) · (ϕ◦f)∼(ϕ◦f(cid:5)).
Bythemonodromytheorem,theliftsofthesetwopathsstartingatq(cid:7) 0 have
the same terminal points. Since the lift of p◦g is g, which starts and ends
at q(cid:7) 0, this implies
ϕ
(cid:5)◦f(cid:5)(1)=g ·
ϕ
(cid:4)◦f(1)=ϕ (cid:4)◦f(1),
so ϕ(cid:7)is well-defined.
Claim 2: ϕ(cid:7) is continuous. Before proving this, we will show that ϕ(cid:7) has
one important property of a continuous map: It takes path connected sets
to path connected sets. Let V ⊂ Y be path connected, and y1,y2 ∈ V be
arbitrary. There is a path f in Y from y0 to y1, and a path g in V from
·
y1 to y2 (Figure 11.5); by definition, ϕ(cid:7) maps the path f g to the lift of
·
(ϕ◦f) (ϕ◦g). In particular, the lift of ϕ◦g is a path from ϕ(cid:7)(y1) to ϕ(cid:7)(y2)
that is contained in ϕ(cid:7)(V). This proves that ϕ(cid:7)(V) is path connected.
To prove that ϕ(cid:7) is continuous, it suffices to show that each point in Y
has a neighborhood on which ϕ(cid:7) is continuous. Let y ∈ Y be arbitrary, let
(cid:7)
U beanevenlycoveredneighborhoodofϕ(y),andletU bethecomponent
of p−1(U) containing ϕ(cid:7)(y) (Figure 11.6). If V is the path component of
ϕ−1(U) containing y, the argument above shows that ϕ(cid:7)(V) is a connected

---

242 11. Covering Spaces
(cid:7)
X
ϕ(cid:7)(V)
ϕ(cid:7)(y1)
ϕ(cid:7)(y2)
Y ϕ(cid:7) q(cid:7)
0
f
y0
g
V y1 y2
FIGURE11.5.Proofthatϕ(cid:7)takespathconnectedsetstopathconnected
sets.
subset of p−1(U), and must therefore be contained in U (cid:7) . Since Y is locally
path connected, V is open and thus is a neighborhood of y. Let σ: U →U (cid:7)
be the local section of p taking ϕ(y) to ϕ(cid:7)(y), so p◦σ is the identity on U.
The following equation holds on V:
p◦ϕ(cid:7)=ϕ=p◦σ◦ϕ.
Both ϕ(cid:7) and σ ◦ϕ map V into U (cid:7) , where p is injective, so this equation
implies ϕ(cid:7)=σ◦ϕ on V, which is a composition of continuous maps.
The following corollaries are immediate.
Corollary 11.16. If p: X (cid:7) → X is a covering map and Y is a simply
connected and locally path connected space, every continuous map ϕ: Y →
X has a lift to X (cid:7) . Given any point y0 ∈ Y, the lift can be chosen to take
y0 to any point in the fiber over ϕ(y0).
Corollary 11.17. Suppose p: X (cid:7) →X is a covering map and X (cid:7) is simply
connected. For any connected and locally path connected space Y, a con-
tinuous map ϕ: Y → X has a lift to X (cid:7) if and only if ϕ∗ is the trivial
homomorphism for any base point y0 ∈ Y. If this is the case, then the lift
can be chosen to take y0 to any point in the fiber over ϕ(y0).
Example 11.18. Consider the n-sheeted covering of the circle given by
the nth power map p : S1 → S1. It is easy to check that the subgroup of
n
π1(S1,1) induced by p
n
is the cyclic subgroup generated by [α]n. Thus, for

---

Covering Maps and the Fundamental Group 243
(cid:7)
X
ϕ(cid:7)(y) U (cid:7)
ϕ(cid:7)
σ p
Y
ϕ X
y ϕ(y) U
V
FIGURE 11.6. Proof that ϕ(cid:7)is continuous.
any integer m, there is a continuous map f making the diagram
S1
(cid:3)(cid:4)
(cid:3)
f (cid:3) p n
(cid:3) (cid:5)
(cid:2)
S1 S1
p
m
commute if and only if m = nk for some integer k. If this is the case, the
lift sending 1 to 1 is obviously f =p .
k
Dependence on Base Points
It is important to remember that in general, the subgroup induced by a
covering depends not only on the covering but also on the choice of base
point q(cid:7)∈ X (cid:7) . As the next theorem shows, the subgroup may change when
we change base point, but it can change only in a very limited way.
Theorem 11.19 (Conjugacy Theorem). Let p: X (cid:7) →X be a covering
map. For any q ∈X, as q(cid:7)varies over the fiber p−1(q), the set of subgroups
p∗π1(X (cid:7) ,q(cid:7))⊂π1(X,q) is exactly one conjugacy class.
Proof. First we will show that given any q(cid:7),q(cid:7)(cid:5) ∈ p−1(q), the subgroups
p∗π1(X (cid:7) ,q(cid:7)) and p∗π1(X (cid:7) ,q(cid:7)(cid:5)) are conjugate. Let g(cid:7)be a path in X (cid:7) from q(cid:7)to

---

244 11. Covering Spaces
q(cid:7)(cid:5)
g(cid:7)
X
(cid:7)
q(cid:7) f
p
q
p◦f
g X
FIGURE 11.7. Proof of the conjugacy theorem.
q(cid:7)(cid:5), and let g = p◦g(cid:7), which is a loop in X based at q (Figure 11.7). We
have four maps
π1(X (cid:7) ,q(cid:7)) Φ g(cid:7)(cid:2) π1(X (cid:7) ,q(cid:7)(cid:5))
p∗ p∗
(cid:5) (cid:5)
π1(X,q) (cid:2) π1(X,q), (11.1)
Φ
g
where Φ g(cid:7)[f] = [g(cid:7)−1] · [f] · [g(cid:7)], and Φ
g
is defined similarly. This diagram
commutes, because
p∗Φ
g(cid:7)[f]=p∗[g(cid:7)−1·
f
·
g(cid:7)]
=[p◦(g(cid:7)−1·
f
·
g(cid:7))]
=[(p◦g(cid:7)−1) · (p◦f) · (p◦g(cid:7))]
=[g−1] · p∗[f] · [g]
=Φ
g
p∗[f].
This means that Φ
g
maps the subgroup p∗π1(X (cid:7) ,q(cid:7)) into p∗π1(X (cid:7) ,q(cid:7)(cid:5)), so
wecanreplacethebottomtwogroupsin(11.1)bytheimagegroupsunder

---

Covering Maps and the Fundamental Group 245
p∗ to obtain
π1(X (cid:7) ,q(cid:7)) Φ g(cid:7)(cid:2) π1(X (cid:7) ,q(cid:7)(cid:5))
p∗ p∗
(cid:5) (cid:5)
p∗π1(X (cid:7) ,q(cid:7))
Φ
(cid:2) p∗π1(X (cid:7) ,q(cid:7)(cid:5)). (11.2)
g
Now, in this diagram, both vertical maps are isomorphisms, and the top
mapisanisomorphismbyTheorem7.11.Thismeansthatthebottommap
Φ is an isomorphism as well. But Φ is exactly the map that sends any
g g
subgroup onto its conjugate by [g]−1, so this shows that p∗π1(X (cid:7) ,q(cid:7)) and
p∗π1(X (cid:7) ,q(cid:7)(cid:5)) are conjugate subgroups.
Conversely, let q(cid:7)∈ p−1(q), and suppose H is any subgroup of π1(X,q)
conjugate to p∗π1(X (cid:7) ,q(cid:7)). This means that there is some element [g] ∈
π1(X,q) such that H = Φ
g
(p∗π1(X (cid:7) ,q(cid:7))). If we let g(cid:7) be the lift of g start-
ing at q(cid:7), and q(cid:7)(cid:5) = g(cid:7)(1), the above construction shows that p∗π1(X (cid:7) ,q(cid:7)(cid:5)) =
Φ
g
(p∗π1(X (cid:7) ,q(cid:7)))=H.
Thereisanimportantspecialcaseinwhichthesubgroupp∗π1(X (cid:7) ,q(cid:7))does
notdependonthechoiceofbasepoint.Wesaythatthecoveringp: X (cid:7) →X
isnormalifp∗π1(X (cid:7) ,q(cid:7))isanormalsubgroupofπ1(X,p(q(cid:7)))foreachq(cid:7)∈X (cid:7) .
Thismeans,inparticular,thatforanyfixedq ∈X thesubgroupp∗π1(X (cid:7) ,q(cid:7))
is independent of the choice of base point q(cid:7)in the fiber over q, because the
onlysubgroupconjugatetoanormalsubgroupisitself.In fact,asthenext
lemma shows, as long as the induced subgroup is normal for one choice of
q(cid:7)∈X (cid:7) , it is normal for all of them.
Lemma 11.20. Let p: X (cid:7) → X be a covering map, and suppose the sub-
group induced by p is normal for one point q(cid:7)∈X (cid:7) . Then p is normal.
Proof. Let q(cid:7),q(cid:7)(cid:5) be two points of X (cid:7) , and let q =p(q(cid:7)), q(cid:5) =p(q(cid:7)(cid:5)). Let g(cid:7)be
a path from q(cid:7)to q(cid:7)(cid:5), and set g = p◦g(cid:7), which is a path from q to q(cid:5). If we
replace q by q(cid:5) in the bottom right corner of diagram (11.1), the diagram
still commutes, and the top and bottom rows are still isomorphisms. It
follows from the commutativity of the diagram that Φ
g
takes p∗(π1(X (cid:7) ,q(cid:7)))
to p∗(π1(X (cid:7) ,q(cid:7)(cid:5))). Since an isomorphism takes normal subgroups to normal
subgroups, the result follows.
Next we show that there is a natural right action of the fundamental
group of the base on the fiber of any covering space. Recall from Chapter
3 that given an action of a group Γ on a set F, the orbit of a point x∈F
is the set of all images of x under elements of the group (for a right action,
·
thisistheset{x γ :γ ∈Γ}),andtheactionissaidtobetransitiveifeach
orbit is all of F.

---

246 11. Covering Spaces
g(cid:7)(1)
(cid:7)
f(1)
g(cid:7)
q(cid:7)
(cid:7)
f
p
q
g
f
FIGURE 11.8. Proof that the fundamental group acts on the fiber.
Theorem 11.21 (Action of the Fundamental Group on a Fiber).
Suppose p: X (cid:7) → X is a covering map and q ∈ X. There is a transitive
right action of π1(X,q) on the fiber p−1(q), given by q(cid:7) · [f] = f (cid:7) (1), where
f (cid:7) is the lift of f starting at q(cid:7)∈p−1(q).
Proof. If q(cid:7)is any point in the fiber over q, any path f starting at q has a
lift to a path f (cid:7) starting at q(cid:7)by the path lifting property. The monodromy
(cid:7)
theorem guarantees that the endpoint f(1) depends only on the path class
·
of f; therefore, q(cid:7) [f] is well-defined.
To see that this is a group action, we need to check two things:
·
(a) q(cid:7) [c ]=q(cid:7);
q
· · · ·
(b) (q(cid:7) [f]) [g]=q(cid:7) ([f] [g]).
For(a),justobservet
·
hattheconstantloopc q(cid:7)istheuniqueliftofc
q
starting
at q(cid:7), and therefore q(cid:7) [c
q
]=c q(cid:7)(1)=q(cid:7). To prove the composition property
(cid:7)
(b),supposef andg aretwoloopsbasedatq.Letf betheliftoff starting
at q(cid:7), so that q(cid:7) · [f] = f (cid:7) (1). Now, if g(cid:7) is the lift of g starting at f (cid:7) (1), then
by definition, (q(cid:7)
·
[f])
·
[g]=g(cid:7)(1) (Figure 11.8). On the other hand, f
(cid:7)·
g(cid:7)is

---

The Covering Group 247
·
clearly the lift of f g starting at q(cid:7). This means that
· · · ·
q(cid:7) ([f] [g])=q(cid:7) [f g]
=(f
(cid:7)·
g(cid:7))(1)
=g(cid:7)(1).
Finally, to prove that the action is transitive, just note that any two
points q(cid:7),q(cid:7)(cid:5) in the fiber over q are joined by a path f (cid:7) because X (cid:7) is path
connected. Setting f =p◦f (cid:7) , it is immediate that f (cid:7) is the lift of f starting
at q(cid:7), and therefore q(cid:7) · [f]=q(cid:7)(cid:5).
Corollary 11.22. Let p: X (cid:7) → X be a covering map, and suppose X (cid:7) is
simply connected. The number of sheets of the covering is equal to the car-
dinality of the fundamental group of X.
Proof. Choose a base point q ∈ X and a point q(cid:7)in the fiber over q, and
consider the map π1(X,q)→p−1(q) given by [f](cid:10)→q(cid:7) · [f]. It is surjective
because the action of the fundamental group is transitive. To show that it
is injective, suppose that q(cid:7) · [f] = q(cid:7) · [g]. This means that the lifts f (cid:7) and
g(cid:7)starting at q(cid:7)end at the same point. Since X (cid:7) is simply connected, f (cid:7)∼g(cid:7),
and therefore [f]=p∗[f (cid:7) ]=p∗[g(cid:7)]=[g].
Example 11.23. Since π: Sn → Pn is a two-sheeted covering and Sn
is simply connected, Corollary 11.22 shows that π1(Pn) is a two-element
group, which must therefore be isomorphic to Z/(cid:22)2(cid:23).
Corollary 11.24. If X is a simply connected space, any covering map
p: X (cid:7) →X is a homeomorphism.
(cid:7)
Proof. The injectivity theorem shows that X is also simply connected.
Thus Corollary 11.22 shows that the cardinality of the fibers is 1, so p is a
one-to-one covering map and therefore a homeomorphism.
The Covering Group
In this section we introduce the group of covering transformations of a
covering space, and explore its relation to the fundamental groups of the
base and the covering space.

---

248 11. Covering Spaces
Suppose p: X (cid:7) →X is a covering map. A homeomorphism ϕ: X (cid:7) →X (cid:7) is
called a covering transformation if p◦ϕ=p:
(cid:7) ϕ (cid:2) (cid:7)
X X
p(cid:6) (cid:3)p
(cid:6)(cid:7) (cid:3)(cid:9)
X.
Coveringtransformationsarealsovariouslyknownasdeck transformations
or automorphisms of the covering.
Let C (X (cid:7) ) denote the set of all covering transformations of X (cid:7) with re-
p
specttop.Itiseasytoverifythatthecompositionoftwocoveringtransfor-
mations, the inverse of a covering transformation, and the identity map of
X (cid:7) are all covering transformations; thus C (X (cid:7) ) is a group, called the cov-
p
(cid:7)
ering group or the automorphism group of the covering. It acts on X (on
the left) in a natural way, and the definition of covering transformations
implies that each orbit is a subset of a single fiber.
Example 11.25. For the covering ε: R → S1, the integral translations
x (cid:10)→ x+k for k ∈ Z are easily seen to be covering transformations. More
generally,foranyintegers(k1,…,k
n
),thetranslation(x1,…,x
n
)(cid:10)→(x1+
k1,…,x
n
+k
n
)isacoveringtransformationofE: Rn →Tn.Wewillprove
below that these are all of them.
Example 11.26. If π: Sn → Pn is the covering map of Example 11.4,
then the antipodal map A(x) = −x is a covering transformation. We will
see shortly that C (Pn) is the two-element group {Id,A}.
π
Proposition 11.27 (Properties of the Covering Group). Let
p: X (cid:7) →X be a covering map.
(a) If two covering transformations agree at one point, they are identical.
(b) The covering group acts freely and continuously on X (cid:7) : If ϕ(q(cid:7)) = q(cid:7)
for some q(cid:7)∈X (cid:7) , then ϕ=Id(cid:7).
X
(c) For any q ∈X, each covering transformation permutes the points of
the fiber p−1(q).
(d) ForanyevenlycoveredopensetU ⊂X,eachcoveringtransformation
permutes the components of p−1(U).
Proof. Note that a covering transformation ϕ is, in particular, a lift of p:
(cid:7)
X
(cid:3)(cid:4)
(cid:3)
ϕ p
(cid:3)
(cid:3) (cid:5)
(cid:7) (cid:2)
X p X.

---

The Covering Group 249
Thus (a) follows from the unique lifting property. The covering group
acts continuously because each covering transformation is continuous by
definition; the fact that it acts freely follows from (a) by comparing ϕ
with the identity. Part (c) follows from the fact that if q(cid:7)∈ p−1(q), then
p(ϕ(q(cid:7))) = p(q(cid:7)) = p, so ϕ takes the fiber over q to itself; since the same is
trueofϕ−1,ϕactsasapermutationofthefiber.Toprove(d),letU bean
evenlycoveredopenset,andletU beacomponentofp−1(U).Sinceϕ(U )
α α
is a connected subset of p−1(U), it must be contained in a single compo-
nent; applying the same argument to ϕ−1 shows that ϕ(U ) is exactly a
α
component.
Example 11.28. Consider again the covering group of ε: R → S1. Let
ϕ∈C (R)bearbitrary.Ifwesetn=ϕ(0),thenbothϕandthetranslation
ε
x (cid:10)→ x+n are covering transformations taking 0 to n, and are therefore
equal by Proposition 11.27(a). Thus the covering group of ε: R → S1 is
equal to Z acting on R by integral translations. By a similar argument,
the covering group of E: Rn → Tn is Zn acting by translations, and the
covering group of π: Sn → Pn is equal to the cyclic group of order 2
generated by the antipodal map.
(cid:7)
Because of Proposition 11.27, the action of the covering group on X
is completely determined by the action on any fiber. However, unlike the
action of the fundamental group on a fiber that we defined in Theorem
11.21,theactionofthecoveringgrouponfibersisnottransitiveingeneral.
It is often useful to have a criterion for deciding when two points in a fiber
are in the same orbit.
Proposition 11.29 (Orbit Criterion). Let p: X (cid:7) → X be a covering
map.
(a) If q(cid:7), q(cid:7)(cid:5) ∈ X (cid:7) are two points in the same fiber p−1(q), there exists
a covering transformation taking q(cid:7) to q(cid:7)(cid:5) if and only if the induced
subgroups p∗π1(X (cid:7) ,q(cid:7)) and p∗π1(X (cid:7) ,q(cid:7)(cid:5)) are equal.
(b) C (X (cid:7) ) acts transitively on each fiber if and only if p is a normal
p
covering.
Proof. Ifthereexistsϕsuchthatϕ(q(cid:7))=q(cid:7)(cid:5),thenϕ∗: π1(X (cid:7) ,q(cid:7))→π1(X (cid:7) ,q(cid:7)(cid:5))
is an isomorphism, so p∗π1(X (cid:7) ,q(cid:7)) = p∗ϕ∗π1(X (cid:7) ,q(cid:7)) = p∗π1(X (cid:7) ,q(cid:7)(cid:5)). Con-
versely, if the two subgroups are equal, then the lifting criterion yields a
lift p(cid:7): X (cid:7) → X (cid:7) satisfying p◦p(cid:7)= p and p(cid:7)(q(cid:7)) = q(cid:7)(cid:5). Reversing the roles of
q(cid:7) and q(cid:7)(cid:5), we get a lift p(cid:7)(cid:5) satisfying p(cid:7)(cid:5)(q(cid:7)(cid:5)) = q(cid:7). To show that p(cid:7) and p(cid:7)(cid:5)
are inverses of each other, note that p(cid:7)(cid:5)◦p(cid:7)and Id(cid:7) are lifts of p taking q(cid:7)
X
to itself, and thus are equal by the unique lifting property, and similarly
p(cid:7)◦p(cid:7)(cid:5) =Id(cid:7). Therefore, p(cid:7)is the required covering transformation.
X
Nowsupposepisnormal.Thismeansthatforanyq(cid:7),q(cid:7)(cid:5) inthesamefiber,
p∗π1(X (cid:7) ,q(cid:7))=p∗π1(X (cid:7) ,q(cid:7)(cid:5)),sobypart(a)thereisacoveringtransformation

---

250 11. Covering Spaces
taking q(cid:7)to q(cid:7)(cid:5). Conversely, if C (X (cid:7) ) acts transitively on the fiber p−1(q),
p
the groups p∗π1(X (cid:7) ,q(cid:7)) coincide for all q(cid:7)∈p−1(q), which is to say that p is
normal.
The next theorem is the central result concerning the relationship be-
tweencoveringspacesandfundamentalgroups.Itgivesanexplicitformula
for the covering group in terms of the fundamental groups of the covering
space and the base, and can be used to compute the fundamental groups
of certain spaces from properties of their coverings. For normal coverings,
the theorem simply says that the covering group is isomorphic to the quo-
tientofthefundamentalgroupofthebasebythesubgroupinducedbythe
covering.Thestatementforgeneralgroupsissomewhatmorecomplicated,
and involves the following algebraic notion: If G is a group and H ⊂ G
is a subgroup, the normalizer of H in G, denoted by N(H), is the set of
all elements γ ∈G such that γ−1Hγ =H. The normalizer N(H) is easily
seen to be a subgroup of G; it is in fact the largest subgroup in which H is
normal.
Theorem 11.30 (Covering Group Structure Theorem). Suppose
p: X (cid:7) → X is a covering map and q(cid:7) ∈ X (cid:7) . The covering group C (X (cid:7) ) is
p
isomorphic to the quotient
N(p∗π1(X (cid:7) ,q(cid:7)))
.
p∗π1(X (cid:7) ,q(cid:7))
The isomorphism is induced by the map α: N(p∗π1(X (cid:7) ,q(cid:7))) → C
p
(X (cid:7) ) that
·
sends [f] to the unique covering transformation ϕ taking q(cid:7)to q(cid:7) [f].
Beforewegivetheproofofthisimportanttheorem,whichisrathertech-
nical, let us derive some immediate consequences to illustrate its utility.
Corollary 11.31 (Normal Case). If p: X (cid:7) → X is a normal covering,
q(cid:7)∈X (cid:7) , and q =p(q(cid:7)), then C
p
(X (cid:7) ) ∼ =π1(X,q)/p∗π1(X (cid:7) ,q(cid:7)).
Corollary 11.32 (Simply Connected Case). If p: X (cid:7) → X is a cov-
ering map and X (cid:7) is simply connected, then for any q(cid:7)∈ X (cid:7) the map α of
Theorem 11.30 is an isomorphism from π1(X,q) to C
p
(X (cid:7) ), where q =p(q(cid:7)).
Example 11.33. Since the covering group of ε: R → S1 is infinite cyclic
and R is simply connected, Corollary 11.32 yields another proof that the
fundamental group of the circle is infinite cyclic. In fact, if you look back
carefullyattheproofinChapter8,youwillseethatthisisreallythesame
proof we gave there, decorated with some fancier terminology.
Example 11.34. Because the covering group of π: Sn → Pn is the two-
element group {Id,A}, Corollary 11.32 gives another proof that π1(Pn) ∼ =
Z/(cid:22)2(cid:23).

---

The Covering Group 251
Proof of the covering group structure theorem. Write H = p∗π1(X (cid:7) ,q(cid:7)) ⊂
π1(X,q). We will show that α: N(H) → C
p
(X (cid:7) ) is a surjective homomor-
phismwhosekernelisH;bythefirstisomorphismtheorem,thisprovesthe
result.
Let [g] ∈ N(H) be arbitrary, and let q(cid:7)(cid:5) = q(cid:7) · [g] as defined in Theorem
11.21. Recall that q(cid:7)(cid:5) is the terminal point of the lift g(cid:7) of g starting at q(cid:7).
The key claim is that there exists a covering transformation ϕ ∈ C (X (cid:7) )
p
such that ϕ(q(cid:7))=q(cid:7)(cid:5).
By the orbit criterion, to prove the claim it suffices to show that
p∗π1(X (cid:7) ,q(cid:7)(cid:5)) = p∗π1(X (cid:7) ,q(cid:7)). Let Φ g(cid:7): π1(X (cid:7) ,q(cid:7)) → π1(X (cid:7) ,q(cid:7)(cid:5)) be the isomor-
phism determined by the path g(cid:7) as in Theorem 7.11. From the commu-
tative diagram (11.2) in the proof of the conjugacy theorem, we conclude
that
p∗π1(X (cid:7) ,q(cid:7)(cid:5))=p∗Φ g(cid:7)π1(X (cid:7) ,q(cid:7))
=Φ
g
p∗π1(X (cid:7) ,q(cid:7))
=[g]−1·
H
·
[g]=H
=p∗π1(X (cid:7) ,q(cid:7)).
Thus there exists a covering transformation ϕ such that ϕ(q(cid:7)) = q(cid:7)(cid:5); it is
necessarily unique by Proposition 11.27(a). Define α[g]=ϕ.
To show that α is a homomorphism, let [g1],[g2] ∈ N(H), and write
α[g ]=ϕ , so that ϕ is a covering transformation satisfying ϕ (q(cid:7))=g(cid:7)(1).
i i i i i
· ·
Let ϕ12 = α[g1 g2], so ϕ12(q(cid:7)) = g(cid:5) 1 g2(1). We need to show that ϕ12 =
ϕ1 ◦ϕ2. It suffices to show that these two covering transformations agree
at one point, so let us show that ϕ12(q(cid:7)) = ϕ1 ◦ ϕ2(q(cid:7)), or equivalently
·
g(cid:5) 1 g2(1)=ϕ1(g(cid:7) 2(1)).
Now, the lift g(cid:7) 2 of g2 is a path in X (cid:7) starting at q(cid:7). Because p◦ϕ1 = p,
the image ϕ1 ◦g(cid:7) 2 of g(cid:7) 2 under ϕ1 is also a lift of g2, but this one starts at
·
ϕ1(q(cid:7)) = g(cid:7) 1(1) (Figure 11.9). Thus the path product g(cid:7) 1 (ϕ1 ◦g(cid:7) 2) makes
·
sense, and is the lift of g1 g2 starting at q(cid:7). In summary,
·
ϕ12(q(cid:7))=g(cid:5) 1 g2(1)
·
=g(cid:7) 1 (ϕ1 ◦g(cid:7) 2)(1)
=ϕ1 ◦g(cid:7) 2(1)
=ϕ1(ϕ2(q(cid:7))),
which was to be proved.
To show that α is surjective, let ϕ ∈ C (X (cid:7) ) be arbitrary, let q(cid:7)(cid:5) = ϕ(q(cid:7)),
p
andletg(cid:7)beapathinX (cid:7) fromq(cid:7)toq(cid:7)(cid:5).Theng =p◦g(cid:7)isaloopinX.Moreover,

---

252 11. Covering Spaces
ϕ1 ◦g(cid:7) 2
ϕ1
(cid:7)
X
g(cid:7) 1 q(cid:7) g(cid:7) 2
g1 q g2 X
FIGURE 11.9. Proof that α is a homomorphism.
the orbit criterion shows that p∗π1(X (cid:7) ,q(cid:7)) = p∗π1(X (cid:7) ,q(cid:7)(cid:5)) because q(cid:7) and
q(cid:7)(cid:5) are in the same orbit. On the other hand, from (11.2), p∗π1(X (cid:7) ,q(cid:7)(cid:5)) =
Φ
g
p∗π1(X (cid:7) ,q(cid:7)). Thus Φ
g
p∗π1(X (cid:7) ,q(cid:7))=p∗π1(X (cid:7) ,q(cid:7)), which is to say that [g]∈
N(H), and the construction above gives α[g]=ϕ.
Finally,weneedtoshowthatKerα=H.Let[g]∈N(H),letg(cid:7)bethelift
ofgstartingatq(cid:7),andwriteϕ=α[g].Thenϕistheidentitytransformation
if and only if ϕ(q(cid:7)) = g(cid:7)(1) = q(cid:7), which means that g(cid:7) is a loop in X (cid:7) ; so ϕ is
the identity if and only if [g]=[p◦g(cid:7)]=p∗[g(cid:7)] for some [g(cid:7)]∈π1(X (cid:7) ,q(cid:7)), i.e.,
[g]∈H.

---

Problems 253
Problems
11-1. Prove that for any n ≥ 1 the map π: Sn → Pn defined in Example
11.4 is a covering map.
11-2. Show that a finite product of covering maps is a covering map: If
p :X (cid:7) →X are covering maps for i=1,…,n, then so is the map
i i i
p1 ×···×p n :X (cid:7) 1 ×···×X (cid:7) n →X1 ×···×X n .
11-3. Suppose p: X (cid:7) →X is a covering map.
(cid:7)
(a) If X is an n-manifold and X is Hausdorff, show that X is an
n-manifold.
(cid:7)
(b) If X is an n-manifold, show that X is an n-manifold.
11-4. Suppose p: X (cid:7) →X is a covering map and X is a compact manifold.
(cid:7)
Show that X is compact if and only if p is a finite-sheeted covering.
11-5. Let S be the following subset of C2:
S ={(z,w):w2 =z, w (cid:14)=0}.
(It is the graph of the two-valued complex square root “function”
described in Chapter 1, with the origin removed.) Show that the
projection π1: C2 → C onto the first coordinate restricts to a two-
sheeted covering map p: S →C(cid:3){0}.
11-6. Show that there is a two-sheeted covering of the Klein bottle by the
torus.
(cid:8)
11-7. LetM,M,andN beconnectedmanifoldsofdimensionnandsuppose
p: M
(cid:8)→M
is a k-sheeted covering map. Show that there exists a k-
(cid:8)
sheetedcoveringofM#N bytheconnectedsumofM withk copies
ofN.[Hint:ChoosetheballtobecutoutofM tolieinsideanevenly
covered neighborhood.]
11-8. Showthateverynonorientablecompactsurfaceofgenusnhasatwo-
sheetedcoveringbyanorientableoneofgenusn−1.[Hint:UseProb-
lem 11-7 and induction.]
11-9. Show that a proper local homeomorphism between connected, path
connected, and locally compact Hausdorff spaces is a covering map.
11-10. A continuous map f: S1 →S1 is said to be odd if f(−z)=−f(z) for
all z ∈ S1, and even if f(z) = f(−z) for all z ∈ S1. Show that every
odd map has odd degree, as follows.

---

254 11. Covering Spaces
(a) Let p2: S1 → S1 be the two-sheeted covering map of Exam-
ple 11.2. If f is odd, show that there exists a continuous map
g: S1 → S1 such that degf = degg and the following diagram
commutes:
f(cid:2)
S1 S1
p2 p2
(cid:5) (cid:5)
(cid:2)
S1
g
S1.
(b) Ifdegf iseven,showthat g liftstoamap g(cid:7): S1 →S1 suchthat
p2 ◦g(cid:7)=g.
(c) Show that g(cid:7)◦p2 and f are both lifts of g ◦p2 that agree at
either (1,0) or (−1,0), so they are equal everywhere; derive a
contradiction.
11-11. Show that every even map f: S1 →S1 has even degree.
11-12. Provethehamsandwichtheorem:Iftwopiecesofbreadandonepiece
of ham are placed arbitrarily in space, all three pieces can be cut in
half with a single slice of the knife. (If you do not like ham, you may
wishtosubstitutetofu.)Moreprecisely,giventhreedisjoint,bounded,
connected open subsets U1,U2,U3 ⊂ R3, there exists a plane that
simultaneously bisects all three, in the sense that the plane divides
R3 into two half spaces H+ and H− such that for each i, U ∩H+
i
has the same volume as U ∩H−. [Hint: For any ω ∈ S2, show that
i
thereareuniquerealnumbers(λ1,λ2,λ3)suchthattheplanethrough
λ ω and orthogonal to ω bisects U . If there does not exist a plane
i i
bisecting all three sets, define a map F: S2 →S1 by
F(ω)= (cid:3)
(λ1 −λ2)+i(λ2 −λ3)
.
(λ1 −λ2)2+(λ2 −λ3)2
ShowthatF iscontinuous,andF◦ιS1 contradictstheresultofProb-
lem11-10,whereιS1: S1 (cid:9)→S2 istheinclusionmap.Youmayassume
thatthereisavolumefunctionVolassigninganonnegativerealnum-
ber to each open set in R3 and satisfying the following properties:
The volume of a set is unchanged by translations or rotations; the
volumes of balls, cylinders, and rectangular solids are given by the
usual formulas; and if U ⊂V then Vol(U)≤Vol(V).]
11-13. Let p: X3 →X2 be the covering map of Exercise 11.1.
(a) Determine the covering group C
p
(X3).
(b) Determine whether p is a normal covering.

---

Problems 255
FIGURE 11.10. The covering map of Problem 11-14.
(c) For each of the following maps f: S1 →X2, determine whether
f has a lift to X3 taking 1 to 1.
i. f(z)=z.
ii. f(z)=z2.
iii. f(z)=2−z.
iv. f(z)=2−z2.
11-14. LetX4betheunionoffourcirclesdescribedinProblem10-10,andlet
p: X4 → X2 be the covering map indicated schematically in Figure
11.10. Answer the questions of Problem 11-13 for this covering.
11-15. Let E be the figure eight space of Example 7.21, and let X be the
unionofthex-axiswithinfinitelymanyunitcirclescenteredat{2πk+
i:k ∈Z}.Letp: X →EbethemapthatsendseachcircleinX onto
the upper circle in E by translating in the x-direction and sends the
x-axis onto the lower circle by x(cid:10)→ieix−i. You may accept without
proof that p is a covering map.
(a) Identifythesubgroupp∗π1(X,0)ofπ1(E,0)intermsofthegen-
erators for π1(E,0).
(b) Compute the covering group C (X).
p
(c) Determine whether p is a normal covering.
11-16. This problem shows that the hypothesis that Y is locally path con-
nected is necessary for the lifting criterion (Theorem 11.15) to hold.
Let X be the topologist’s sine curve (Example 4.10), and let Y be
the union of X with a path in the plane from (1,sin1) to (0,1) that
intersects X only at those two points.
(a) Show that Y is simply connected.

---

256 11. Covering Spaces
(b) Show that there is a map f: Y →S1 that has no lift to R.
11-17. Suppose X is a compact polyhedron and p: X (cid:7) → X is a covering
map.
(cid:7)
(a) ShowthatX andX admittriangulationssuchthatpisinduced
by a simplicial map. [Hint: Use barycentric subdivision.]
(b)
SupposeK,K(cid:7) arefinitecomplexessuchthat|K|=X,|K(cid:7)|=X (cid:7)
,
and p is induced by a simplicial map from K(cid:7) to K. If p is an
n-sheeted covering, show that χ(K(cid:7) )=nχ(K).

---

12
Classification of Coverings
The main thrust of the preceding chapter was to learn about fundamental
groups by studying covering maps. In this chapter we reverse the process
andexplorewhatthereistobelearnedfromthefundamentalgroupabout
the existence and uniqueness of covering spaces. The key idea is provided
bytheconjugacytheoremoftheprecedingchapter:Eachcoveringspaceof
X determines a conjugacy class of subgroups in the fundamental group of
X.
Webeginwiththeuniquenessquestion.Inthefirstsectionofthechapter
we define isomorphisms of covering spaces, and show that two covering
spaces are isomorphic if and only if they induce the same conjugacy class
of subgroups.
Thenweaddresstheexistencequestion.Theultimategoalistoshowthat
forasufficientlynicespaceX (anyconnectedmanifold,forexample),every
conjugacyclassofsubgroupsofπ1(X,q)correspondstosomecovering.This
isaccomplishedinseveralstages.FirstweshowthatX hasauniquesimply
connected covering space, called its “universal covering space.” Then we
show how to construct coverings as quotients of a given space by certain
group actions. The d´enouement is the last theorem of the chapter, which
putstogetheralltheprecedingresultstogiveacompleteclassificationofall
coverings of X up to isomorphism: They are in one-to-one correspondence
with conjugacy classes of subgroups of the fundamental group of X. We
illustratethetheorybydeterminingtheuniversalcoveringspacesofallthe
compact surfaces and classifying all the coverings of the torus.

---

258 12. Classification of Coverings
(cid:7) (cid:7)
X1
f
(cid:7)
(1)
X2
ϕ q(cid:7)
(cid:7)
f g(cid:7)
q(cid:7)
1
q(cid:7)
2
p1 p2
q X
f
FIGURE 12.1. Proof that a covering homomorphism is surjective.
Covering Homomorphisms
In this section we examine the question of how to tell when two covering
spacesare“thesame.”Asusual,weconsidertwocoveringsthesameifthey
are related by a suitable isomorphism. We begin by defining some terms.
Let X be a space, and let p1: X (cid:7) 1 →X, p2: X (cid:7) 2 →X be two coverings of
X. A covering homomorphism from p1 to p2 is a continuous map ϕ: X (cid:7) 1 →
X (cid:7) 2 such that p2 ◦ϕ=p1:
(cid:7) ϕ (cid:2) (cid:7)
X1 X2
p1 (cid:6)
(cid:6)(cid:7) (cid:3)(cid:9)
(cid:3)p2
X.
A covering homomorphism that is also a homeomorphism is said to be an
isomorphismofcoverings.Itiseasytoseethatinthiscasetheinversemap
is also a covering homomorphism. We say two coverings are isomorphic if
there is an isomorphism between them; this is an equivalence relation on
the set of coverings of X. Note that an isomorphism from a covering to
itself is just a covering transformation.
Aninterestingfeatureofcoveringhomomorphismsisthattheyarethem-
selves covering maps, as the following lemma shows.
Lemma 12.1. Let p1: X (cid:7) 1 → X and p2: X (cid:7) 2 → X be coverings of X, and
let ϕ be a covering homomorphism from p1 to p2. Then ϕ is a covering
map.
Proof. First we show that ϕ is surjective. Let q(cid:7)∈X (cid:7) 2 be arbitrary. Choose
some q(cid:7) 1 ∈ X (cid:7) 1, and let q(cid:7) 2 = ϕ(q(cid:7) 1) ∈ X (cid:7) 2, q = p1(q(cid:7) 1) = p2(q(cid:7) 2) ∈ X (Figure
12.1). There is a path g(cid:7) in X (cid:7) 2 from q(cid:7) 2 to q(cid:7). Let f = p2 ◦g(cid:7), which is a

---

Covering Homomorphisms 259
−1
p (V)
1
ϕ−1(U)
ϕ
U
α
−1
p (V)
2
p1
q(cid:7)
U
p2
q V
FIGURE 12.2. An evenly covered neighborhood of q(cid:7).
(cid:7)
path in X starting at q, and let f be the unique lift of f to a path in
X (cid:7) 1 starting at q(cid:7) 1. Consider now the path ϕ◦f (cid:7) in X (cid:7) 2. Its initial point is
ϕ◦f (cid:7) (0) = ϕ(q(cid:7) 1) = q(cid:7) 2, and it satisfies p2 ◦ϕ◦f (cid:7) = p1 ◦f (cid:7) = f, so ϕ◦f (cid:7) is
theliftoff toX (cid:7) 2 startingatq(cid:7) 2.Bytheuniqueliftingproperty,thismeans
that ϕ◦f (cid:7) =g(cid:7), so
ϕ(f (cid:7) (1))=g(cid:7)(1)=q(cid:7),
which shows that ϕ is surjective.
Toshowthatϕisacoveringmap,letq(cid:7)∈X (cid:7) 2 bearbitrary;letq =p2(q(cid:7))∈
X; let U1, U2 ⊂ X be neighborhoods of q that are evenly covered by p1
and p2, respectively; and let V be the component of U1 ∩U2 containing q.
Thus V is a neighborhood of q that is evenly covered by both p1 and p2.
Let U be the component of p −1 (V) containing q(cid:7). We need to show that
2
the components of ϕ−1(U) are mapped homeomorphically onto U by ϕ.
−1
Consider the restrictions of p1 and ϕ to the “stack of pancakes” p
1
(V)
−1
(Figure 12.2). Since U is both open and closed in p (V), it follows that
2
ϕ−1(U) is both open and closed in p −1 (V), and is thus a union of compo-
1
nents. On any such component U , the following diagram commutes:
α
U
α
(cid:6) ϕ
(cid:6)(cid:7)
p1 U
(cid:5)(cid:3)(cid:9)
(cid:3)p2
V.

---

260 12. Classification of Coverings
Since p1 and p2 are homeomorphisms in this diagram, so is ϕ.
Thekeytodeterminingwhentwocoveringspacesareisomorphicistode-
cidewhentherearecoveringhomomorphismsbetweenthem.Thisquestion
is answered by the following theorem.
Theorem 12.2 (Covering Homomorphism Criterion). Suppose
p1: X (cid:7) 1 → X and p2: X (cid:7) 2 → X are two coverings of X, and q(cid:7) 1 ∈ X (cid:7) 1,
q(cid:7) 2 ∈ X (cid:7) 2 are base points such that p1(q(cid:7) 1) = p2(q(cid:7) 2) = q ∈ X. There exists
a covering homomorphism from p1 to p2 taking q(cid:7) 1 to q(cid:7) 2 if and only if
p1∗ π1(X (cid:7) 1,q(cid:7) 1)⊂p2∗ π1(X (cid:7) 2,q(cid:7) 2).
Proof. A covering homomorphism from p1 to p2 can also be viewed as a
lift of p1:
(cid:7)
X2
(cid:3)(cid:4)
ϕ (cid:3) p2
(cid:3) (cid:5)
(cid:7) (cid:2) (12.1)
X1 p1 X.
Thusboththenecessityandthesufficiencyofthesubgroupconditionfollow
from the lifting criterion (Theorem 11.15).
Example 12.3. Let p : S1 →S1 be the nth power map defined in Exam-
n
ple 11.2. The subgroup of π1(S1,1) induced by p
n
is the cyclic subgroup
generated by [α]n (Example 11.18). By the covering homomorphism crite-
rion, there is a homomorphism from p to p if and only if m is divisible
m n
by n; the homomorphism in that case is just p .
m/n
Example 12.4. ConsiderthefollowingtwocoveringsofT2:E: R2 →T2is
thecoveringofExample11.3(theproductoftwocopiesofε: R→S1);and
p: S1×R→T2 is given by p(z,y)=(z,ε(y)). Writing π1(T2) ∼ =(cid:22)β(cid:23)×(cid:22)γ(cid:23),
we see that E∗π1(R2) is trivial, while p∗π1(S1×R)=(cid:22)β(cid:23)×{1}. Therefore,
there exists a covering homomorphism from E to p. (Why do the base
points not matter?) It is easy to check that ϕ(x,y) = (ε(x),y) is such a
homomorphism.
Thefollowingtheoremcompletelysolvestheuniquenessquestionforcov-
ering spaces up to isomorphism.
Theorem 12.5 (Covering Isomorphism Theorem). Two coverings
p1: X (cid:7) 1 → X and p2: X (cid:7) 2 → X are isomorphic if and only if for some
q ∈X and base points q(cid:7) 1 ∈p − 1 1 (q) and q(cid:7) 2 ∈p − 2 1 (q), the induced subgroups
p1∗ π1(X (cid:7) 1,q(cid:7) 1) and p2∗ π1(X (cid:7) 2,q(cid:7) 2) are conjugate in π1(X,q). If this is the
case, these subgroups are conjugate for every such q, q(cid:7) 1, and q(cid:7) 2.

---

The Universal Covering Space 261
Proof. If there exists an isomorphism ϕ: X (cid:7) 1 → X (cid:7) 2, choose q(cid:7) 1 ∈ X (cid:7) 1 ar-
bitrarily and set q(cid:7) 2 = ϕ(q(cid:7) 1). The covering homomorphism criterion ap-
plied to ϕ and ϕ−1 guarantees that the two subgroups p1∗ π1(X (cid:7) 1,q(cid:7) 1) and
p2∗ π1(X (cid:7) 2,q(cid:7) 2) are contained in each other, so they are equal. Thus by the
conjugacy theorem (Theorem 11.19), the subgroups associated with any
other choices of base points in the same fibers are conjugate.
Conversely,supposethetwosubgroupsareconjugateforsomechoiceofq,
q(cid:7) 1, and q(cid:7) 2. By the conjugacy theorem, we can change to a new base point
q(cid:7) 2 (cid:5) ∈ X (cid:7) 2 such that p2∗ π1(X (cid:7) 2,q(cid:7) 2 (cid:5)) = p1∗ π1(X (cid:7) 1,q(cid:7) 1). Then by the covering
homomorphism criterion there exist homomorphisms ϕ from p1 to p2 and
ψ from p2 to p1, with ϕ(q(cid:7) 1) = q(cid:7)
2
(cid:5) and ψ(q(cid:7)
2
(cid:5)) = q(cid:7) 1. The composite map
ψ◦ϕ is a covering transformation of p1 that fixes q(cid:7) 1, so it is the identity.
Similarly, ϕ◦ψ is the identity, so ϕ is the required isomorphism.
The Universal Covering Space
When the results of the preceding section are applied to simply connected
covering spaces, they yield some extremely useful results.
Proposition 12.6 (Properties of Simply Connected Coverings).
(a) Let p: X (cid:7) → X be a covering map with X (cid:7) simply connected. If
p1: X (cid:7) 1 →X is any covering, there exists a covering map p(cid:7): X (cid:7) →X (cid:7) 1
such that the following diagram commutes:
(cid:7)
X
(cid:6) p(cid:7)
(cid:6)(cid:7)
p X (cid:7) 1
(cid:5)(cid:3)(cid:9)
(cid:3)p1
X.
(b) Anytwosimplyconnectedcoveringsofthesamespaceareisomorphic.
Proof. Since the trivial subgroup is contained in every other subgroup,
part (a) follows from the covering homomorphism criterion and the fact
that every covering homomorphism is a covering map. Part (b) follows
immediately from the covering isomorphism theorem.
Part (a) of this proposition says that a simply connected covering space
covers every other covering space of X. Because of this, any covering of X
(cid:7)
byasimplyconnectedspaceX (whichisuniqueby(b))iscalledauniversal
(cid:7)
covering, and X is called the universal covering space of X.
Example 12.7. Theuniversalcoveringspaceofthen-torusisRn,because
weconstructedacoveringmapE: Rn →TninExample11.3.Theuniversal
covering space of Pn is Sn, by the covering map π of Example 11.4.

---

262 12. Classification of Coverings
As the next theorem shows, every “reasonable” space, including every
manifold, has a universal covering space. We say that a space X is lo-
cally simply connected if it admits a basis of simply connected open sets.
Clearly,alocallysimplyconnectedspaceislocallypathconnected,because
simply connected sets are path connected. Any manifold is locally simply
connected, because it has a basis of Euclidean balls.
Theorem 12.8 (Existence of the Universal Covering Space). Ev-
ery connected and locally simply connected topological space (in particular,
every connected manifold) has a universal covering space.
Proof. To get an idea how to proceed, suppose for a moment that X does
have a universal covering p: X (cid:7) → X. The key fact is that once we choose
base points q(cid:7) 0 ∈ X (cid:7) and q0 = p(q(cid:7) 0) ∈ X, the fiber p−1(q) over any q ∈ X
is in one-to-one correspondence with path classes from q0 to q. To see why,
define a map E from the set of such path classes to p−1(q) by sending [f]
to the terminal point of the lift of f starting at q(cid:7) 0. Since lifts of homotopic
pathshavethesameterminalpointbythemonodromytheorem,E iswell-
defined. E is surjective, because given any q(cid:7)in the fiber over q, there is a
path f (cid:7) from q(cid:7) 0 to q(cid:7), and then p◦f (cid:7) is a path from q0 to q whose lift ends
at q(cid:7). Injectivity of E follows from the fact that X (cid:7) is simply connected: If
(cid:7) (cid:7)
f1, f2 are two paths from q0 to q whose lifts f1,f2 end at the same point,
then f (cid:7) 1 and f (cid:7) 2 are path homotopic, and therefore so are f1 = p◦f (cid:7) 1 and
f2 =p◦f (cid:7) 2.
Now let X be any space satisfying the hypotheses of the theorem, and
choose any base point q0 ∈X. Guided by the observation in the preceding
(cid:7)
paragraph, we define X to be the set of path classes of paths in X starting
at q0, and define p: X (cid:7) → X by p[f] = f(1), which is well-defined because
(cid:7)
path homotopic paths have the same terminal point. We will prove thatX
has the required properties in a series of steps.
Step1:TopologizeX (cid:7) .WedefineatopologyonX (cid:7) byconstructingabasis.
Forany[f]∈X (cid:7) andanysimplyconnectedopensetU ⊂X containingf(1),
define the set [f · U]⊂X (cid:7) by
· ·
[f U]={[f a]:a is a path in U starting at f(1)}.
·
Let B denote the collection of all such sets [f U]; we will show that B is a
basis.First,sinceX islocallysimplyconnected,forany[f]∈X (cid:7) thereexists
·
a simply connected open set U containing f(1), and clearly [f] ∈ [f U].
Thus the union of all the sets in B is X (cid:7) .
Tochecktheintersectioncondition,suppose[h]∈X (cid:7) isintheintersection
· · · ·
oftwobasissets[f U],[g V]∈B.Thismeansthath∼f a∼g b,where
a is a path in U and b is a path in V (Figure 12.3). Let W be a simply
connected neighborhood of h(1) contained in U ∩V (such a neighborhood
·
existsbecauseX hasabasisofsimplyconnectedopensets).If[h c]isany
· · · · · ·
elementof[h W],then[h c]=[f a c]∈[f U]becausea cisapathin

---

The Universal Covering Space 263
V
W
b
X g c
h
a
q0
U
f
·
FIGURE 12.3. Proof that the collection of sets [f U] is a basis.
· · · · ·
U.Similarly,[h c]=[g b c]∈[g V].Thus[h W]isabasissetcontained
· ·
in [f U]∩[g V], which proves that B is a basis. From now on, we endow
X (cid:7) with the topology generated by B.
Step 2: X (cid:7) is path connected. Let [f] ∈ X (cid:7) be arbitrary. We will show
that there is a path in X (cid:7) from q(cid:7) 0 to [f], where q(cid:7) 0 =[c q0 ].
For any 0≤t≤1, define f : I →X by
t
f (s)=f(ts),
t
so f
t
is a path in X from q0 to f(t). Then define f (cid:7) : I →X (cid:7) by
(cid:7)
f(t)=[f ].
t
Clearly, f (cid:7) (0)=[f0]=q(cid:7) 0, and f (cid:7) (1)=[f1]=[f]. So we need only show that
(cid:7) (cid:7)
f is continuous; for this it suffices to show that the inverse image under f
of any basis open set [h · U] ⊂ X (cid:7) is open. Let t0 ∈ I be a point such that
f (cid:7) (t0) ∈ [h · U] (Figure 12.4). This means that f
t0
∼ h · c for some path c
lying in U, and in particular that f(t0) = f
t0
(1) ∈ U. For any 0 ≤ t ≤ 1,
define a path f by
t0t
f
t0t
(s)=f(t0+s(t−t0)).
·
This path just follows f from f(t0) to f(t), so f
t0
f
t0t
is easily seen to be
path homotopic to f .
t

---

264 12. Classification of Coverings
U
h
X c f(t)
f
f(t0)
q0
(cid:7)
FIGURE 12.4. Proof that X is path connected.
By continuity of f, there is some δ > 0 such that f(t0 −δ,t0+δ) ⊂ U.
If t∈(t0 −δ,t0+δ), then
· · ·
f ∼f f ∼h c f ,
t t0 t0t t0t
from which it follows that
f (cid:7) (t)=[f ]=[h · c · f ]∈[h · U].
t t0t
Thisshowsthatf (cid:7)−1[h · U]containstheset(t0 −δ,t0+δ),sof (cid:7) iscontinuous.
Step 3: p is a covering map. Let U ⊂X be any simply connected open
set. We will show that U is evenly covered.
Choose any point q1 ∈ U. We begin by showing that p−1(U) is the
·
disjointunionofthesets[f U]as[f]variesoverallthedistinctpathclasses
·
f(cid:2)rom q0 to q1. It is obvious from the definition of p that p[f U] ⊂ U, so
[f · U]⊂p−1(U). Conversely, if [g]∈p−1(U), then g(1)=p[g]∈U, so
[f]
there is a path b in U from(cid:2)g(1) to q1, and [g]=[g · b · b−1]∈[(g · b) · U].
This proves that p−1(U)= [f · U].
[f]
This shows, in particular, that p is continuous: X has a basis of simply
connected open sets, and the inverse image under p of any such set is a
union of basis sets and therefore open. And p is clearly surjective, because
each q ∈X is equal to p[g] for any path g from q0 to q.
·
Next we show that p is a homeomorphism from each set [f U] to U. It
is surjective because for each q ∈U there is a path a from f(1) to q in U,
soq =p[f · a]∈p[f · U].Toseethatitisinjective,let[g],[g(cid:5)]∈[f · U],and
supposep[g]=p[g(cid:5)],orinotherwords,g(1)=g(cid:5)(1)(Figure12.5).Thenby
definition of [f · U], g ∼f · a and g(cid:5) ∼f · a(cid:5) for some paths a,a(cid:5) in U from
f(1) to g(1). Since U is simply connected, a ∼ a(cid:5) and therefore [g] = [g(cid:5)].
Finally,pisanopenmapbecauseittakesbasisopensetstoopensets,and
·
therefore p: [f U]→U is a homeomorphism.

---

The Universal Covering Space 265
U
g a
X
f a(cid:5)
g(cid:5)
q0
·
FIGURE 12.5. Proof that p is injective on [f U].
·
Eachset[f U]isopenbydefinition,andeachispathconnectedbecause
(cid:7)
itishomeomorphictothepathconnectedsetU.ItfollowsthatX islocally
path connected. To complete the proof that p is a covering map, we need
to show that for any two paths f and f(cid:5) from q0 to q1, the sets [f · U] and
[f(cid:5) · U] are either equal or disjoint. If they are not disjoint, there exists
[g] ∈ [f · U]∩[f(cid:5) · U], so g ∼ f · a ∼ f(cid:5) · a(cid:5) for paths a, a(cid:5) in U from q1
to g(1). Since U is simply connected, a ∼ a(cid:5), which implies f ∼ f(cid:5) and
therefore [f
· U]=[f(cid:5)·
U].
Step 4: X (cid:7) is simply connected. Suppose F: I →X (cid:7) is any loop based at
q(cid:7) 0. Let f = p◦F, so F is a lift of f. If we write f (cid:7) (t) = [f
t
] as in Step 3,
then p◦f (cid:7) (t) = p[f
t
] = f
t
(1) = f(t), so f (cid:7) is also a lift of f starting at q(cid:7) 0.
(cid:7)
By the unique lifting property, F =f. Since F is a loop,
[c q0 ]=q(cid:7) 0 =F(1)=f (cid:7) (1)=[f1]=[f],
so f is null homotopic. By the homotopy lifting property, this means that
F is null homotopic as well.
A careful study of this proof shows that it does not really need the full
strengthofthehypothesisthatX islocallysimplyconnected.Eachtimewe
usethefactthataloopinasmallopensetU ⊂X isnullhomotopic,allwe
really need to know is that it is null homotopic in X. For this reason, it is
traditionaltomakethefollowingdefinition:AspaceX issemilocallysimply
connected if it admits a basis of open sets U with the property that every
loopinU isnullhomotopicinX.Itcanbeshownthataconnected,locally
path connected space admits a universal covering space if and only if it is
semilocallysimplyconnected(see[Mas89]or[Sie92]).Sinceourmotivation

---

266 12. Classification of Coverings
for studying the fundamental group is to understand manifolds, we have
no need for this extra generality.
Once you have understood the proof of the existence of the universal
coveringspaceofaspaceX,youshouldforgetthecomplicatedconstruction
(cid:7) (cid:7)
of X in terms of path classes, and just think of X as a simply connected
space with a covering map to X. The uniqueness theorem tells us that all
(cid:7)
the relevant properties of X can be derived from these facts.
Proper Group Actions
ThenextstepinclassifyingcoveringsistostartwithaspaceY anddevelop
atechniqueforconstructingspacescoveredbyY.Inthenextsectionwewill
apply this to the universal covering space in order to derive a classification
theorem for coverings of a given space X.
To get an idea how to construct spaces covered by Y, let us suppose
p: X (cid:7) → X is a normal covering. (The restriction to normal coverings will
notbealimitationintheend:Forreasonsthatwillsoonbecomeapparent,
the construction in this section will produce only normal coverings, but in
the next section we will be able to use them to produce all coverings of a
given space.)
As we observed in the previous chapter, the covering group C (X (cid:7) ) acts
p
(cid:7)
continuouslyandfreelyonX (ontheleft).Theorbitcriterion(Proposition
11.29) says that C (X (cid:7) ) acts transitively on each fiber when p is normal, so
p
the identifications made by p are exactly those determined by the equiva-
lence relation x ∼ y if and only if y = ϕ(x) for some ϕ ∈ C (X (cid:7) ). Since p
p
is a quotient map by Lemma 11.5, X is homeomorphic to the orbit space
determined by the left action of C (X (cid:7) ) on X (cid:7) (see Chapter 3).
p
NowletY beanyspace,andsupposewearegivenaleftactionbyagroup
Γ on Y. Our aim in this section is to describe conditions under which the
quotient map π: Y → Y/Γ onto the orbit space is a covering map whose
covering group is Γ. Note that this construction can produce only normal
coverings, because Γ acts transitively on the fibers of any orbit space by
definition.
Not every group action yields a covering map, of course. Clearly, the
actionmustbecontinuousandfree(Proposition11.27(b)).Moreover,every
pointofacoveringspaceY hasaneighborhood(oneofthe“pancakes”over
an evenly covered open set) whose images under the covering group are all
disjoint, which places a strong restriction on the actions we can consider.
A simple condition that will guarantee that a group action has the req-
uisite properties in all cases of interest to us is the following. A continuous
actionofatopologicalgroupΓonaspaceY issaidtobeproperifthemap
·
Γ×Y → Y ×Y given by (g,y) (cid:10)→ (y,g y) is a proper map, i.e., if the
inverse image of any compact set under this map is compact.

---

Proper Group Actions 267
Properactionshavethefollowingusefulalternativecharacterizations,at
least for discrete group actions on locally compact Hausdorff spaces, the
onlytypewewillbeconcernedwith.Foranyg ∈ΓandanysubsetK ⊂Y,
· ·
we let g K ={g y :y ∈K}.
Proposition 12.9. For a discrete group Γ acting on a locally compact
Hausdorff space Y, the following are equivalent:
(a) Γ acts properly.
·
(b) For any compact set K ⊂Y, K∩(g K)=∅ for all but finitely many
g ∈Γ.
(c) For every y,y(cid:5) ∈ Y, there exist neighborhoods U of y and U(cid:5) of y(cid:5)
such that U ∩(g · U(cid:5))=∅ for all but finitely many g ∈Γ.
Proof. We will show (a) =⇒ (b) =⇒ (c) =⇒ (a). Assume first that the
action of Γ is proper, and let Φ: Γ×Y → Y ×Y denote the proper map
·
Φ(g,y)=(y,g y). Given any compact set K ⊂Y, the set
Φ−1(K×K)={(g,y)∈Γ×Y :y ∈K, g · y ∈K}
iscompact.ThusitsprojectionontoΓiscompactandthereforefinite.But
·
this projection includes all g ∈Γ such that K∩(g K)(cid:14)=∅, so this proves
(a) =⇒ (b).
Now suppose (b) holds. Because Y is locally compact Hausdorff, any
pointsy,y(cid:5) ∈Y haveprecompactneighborhoodsU andU(cid:5),respectively.Let
·
K bethecompactsetU∪U(cid:5).Thenthesetofg ∈ΓsuchthatK∩(g K)=∅
is finite, which implies (c).
Finally, if (c) holds, let L be an arbitrary compact subset of Y ×Y. For
any(y,y(cid:5))∈L,chooseneighborhoodsU ofyandU(cid:5)ofy(cid:5)asin(c),soU×U(cid:5)
isaneighborhoodof(y,y(cid:5)).Thesetofsuchproductneighborhoodsas(y,y(cid:5))
ranges over L is an open cover of L, so finitely many such neighborhoods
U (g 1 − × 1· U U 1 (cid:5) i (cid:5) , ) . (cid:14)= .., ∅ U } m is × fi U ni m (cid:5) te. c L ov e e t r S L = . F S o 1 r ∪ e · a · c · h ∪ i S , m th a e n s d et K S = i = π1( { L g ) ∈ ⊂ Γ Y. : T U h i e ∩ n
it is straightforward to check that Φ−1(L) is contained in the compact set
S×K.SinceY isHausdorff,LisclosedinY×Y;andsinceΦiscontinuous,
Φ−1(L) is a closed subset of a compact set and thus compact.
Corollary 12.10. IfadiscretegroupΓactsfreelyandproperlyonalocally
compact Hausdorff space Y, every point y ∈Y has a neighborhood U such
·
that U ∩(g U)=∅ unless g =1.
Proof. Taking y = y(cid:5) in Proposition 12.9(c), we obtain neighborhoods U
and U(cid:5) of y such that U ∩(g · U(cid:5)) = ∅ except for finitely many group
elements 1,g1,…,g
m
∈Γ. Since the action is free and Y is Hausdorff, for

---

268 12. Classification of Coverings
each g there are disjoint neighborhoods W of y and W(cid:5) of g · y. Let
i i i i
U (cid:7) =U ∩U(cid:5)∩W1 ∩(g
1
−1· W
1
(cid:5))∩···∩W
m
∩(g
m
−1· W
m
(cid:5) ).
(cid:7)
We will show that U has the required properties.
First consider g = g for some i. If y ∈ U (cid:7) ⊂ g −1· W(cid:5), then g · y ∈ W(cid:5),
i i i i i
whichisdisjointfrom W andthereforefromU (cid:7) .ThusU (cid:7)∩(g · U (cid:7) )=∅.On
i i
the other hand, if g ∈ Γ is not the identity and not one of the g ’s, then
i
for any y ∈ U (cid:7) ⊂ U(cid:5), we have g · y ∈ g · U(cid:5), which is disjoint from U and
(cid:7)
therefore also from U.
Agroupactionpossessingthepropertyexpressedinthiscorollary,orthat
expressed in part (c) of Proposition 12.9, or something closely related to
these(dependingonwhomyouread)hastraditionallybeencalledproperly
discontinuous. This is a particularly unfortunate term, because the group
actionsweareinterestedinareallcontinuous,sooneisforcedtospeakofa
“continuous properly discontinuous action.” We will avoid the problem by
workingonlywithproperactions,whichhavemanyimportantapplications
intopologyandgeometry,andarequitesufficientaslongasweconfineour
attention to locally compact Hausdorff spaces.
Theorem 12.11. LetY beaconnected,locallypathconnected,locallycom-
pact Hausdorff space (for example, a connected manifold), and suppose a
discrete group Γ acts continuously, freely, and properly on Y. Then Y/Γ is
Hausdorff, the quotient map π: Y → Y/Γ is a normal covering map, and
C (Y)=Γ, considered as a group of homeomorphisms of Y.
π
Proof. Clearly, π is surjective and continuous. In fact, it is an open map,
for the following reason: If U ⊂Y is open, then π−1(π(U)) is the union of
·
all sets of the form g U as g ranges over Γ. This is a union of open sets
and therefore open, so π(U) is open.
Toshowthat π isacoveringmap,let y ∈Y,andchooseaneighborhood
U ofy asinCorollary12.10.LetV (cid:7) ⊂U bethecomponentofU containing
(cid:7)
y; clearly, V still has the property that its images under Γ are disjoint. Let
(cid:7)
V =π(V), which is open in Y/Γ because π is an open map.
Now, π−1(V) is the union of the disjoint connected open sets g · V (cid:7) for
g ∈ Γ, so to show that π is a covering it remains only to show that π is
a homeomorphism from each such set onto V. Because for each g ∈ Γ,
g: V (cid:7) →g · V (cid:7) is a homeomorphism and the diagram
(cid:7) g (cid:2) · (cid:7)
V g V
π(cid:6) (cid:3)π
(cid:6)(cid:7) (cid:3)(cid:9)
V
commutes, it suffices to show that π: V (cid:7) → V is a homeomorphism. It is
surjective,continuous,andopen;anditisinjectivebecauseπ(v)=π(v(cid:5))for

---

Proper Group Actions 269
v,v(cid:5) ∈V (cid:7) impliesv(cid:5) =g · vforsomeg ∈Γ,sov =v(cid:5) becauseV (cid:7)∩(g · V (cid:7) )=∅
when g (cid:14)=1. This proves that π is a covering map.
· ·
Ifg ∈Γ,thenx(cid:10)→g xisacoveringtransformation,sinceπ(g x)=π(x)
bydefinition;thusΓ⊂C (Y).Byconstruction,Γactstransitivelyoneach
π
fiber,soπ isanormalcovering.Ifϕisanycoveringtransformation,choose
y ∈ Y and let y(cid:5) = ϕ(y). Then there is some g ∈ Γ such that g · y = y(cid:5);
·
since ϕ and x (cid:10)→ g x are covering transformations that agree at a point,
they are equal. Thus Γ is the full covering group.
·
ToshowthatthequotientspaceisHausdorff,letΦ(g,y)=(y,g y)asin
the proof of Proposition 12.9. Since Φ is proper, it is closed by Proposition
4.32, so Φ(Γ×Y) is a closed subset of Y ×Y. Let x,x(cid:5) ∈Y/Γ be distinct
points. Choosing y,y(cid:5) ∈ Y such that π(y) = x and π(y(cid:5)) = x(cid:5), the fact
that x(cid:14)=x(cid:5) means that (y,y(cid:5))(cid:14)∈Φ(Γ×Y). Therefore, (y,y(cid:5)) has a product
neighborhood U ×U(cid:5) ⊂ Y ×Y that is disjoint from Φ(Γ×Y). Since π
is open, π(U) and π(U(cid:5)) are neighborhoods of x and x(cid:5), respectively. Any
point z ∈ π(U)∩π(U(cid:5)) would satisfy z = π(v) = π(v(cid:5)) for some v ∈ U
and v(cid:5) ∈ U(cid:5). But this would mean that v(cid:5) = g · v for some g ∈ Γ, so
(v,v(cid:5)) = (v,g · v) ∈ Φ(Γ×Y), which contradicts the fact that U ×U(cid:5) is
disjoint from the image of Φ. Thus π(U)∩π(U(cid:5)) = ∅, which shows that
Y/Γ is Hausdorff.
(cid:8)
Corollary 12.12. Let M be a connected n-manifold on which a dis-
(cid:8)
crete group Γ acts continuously, freely, and properly. Then M/Γ is an
n-manifold, and the quotient map π: M (cid:8) → M (cid:8) /Γ is a normal covering
map.
Proof. We know from Theorem 12.11 that π is a normal covering map and
(cid:8)
M/Γ is Hausdorff, and therefore it is a manifold by Problem 11-3(a).
Example 12.13 (Lens Spaces). ByidentifyingR4 withC2 intheobvi-
ous way, we can consider S3 as the following subset of C2:
S3 ={(z1,z2)∈C2 :|z1 |2+|z2 |2 =1}.
Fix a pair of relatively prime integers 1 ≤ m < n, and define an action of
Z/(cid:22)n(cid:23) on S3 by
(cid:12) (cid:13)
k · (z1,z2)= e2πik/nz1,e2πikm/nz2 .
It can easily be checked that this action is free, and it is proper because
Z/(cid:22)n(cid:23) is a finite group (Problem 12-6). The orbit space S3/(Z/(cid:22)n(cid:23)) is thus
a compact 3-manifold whose universal covering space is S3 and whose fun-
damentalgroupisisomorphictoZ/(cid:22)n(cid:23).Thismanifold,denotedbyL(n,m),
is called a lens space.

---

270 12. Classification of Coverings
A particularly important example of a free proper action arises when
we consider a topological group G and a discrete subgroup Γ (that is,
a subgroup that is a discrete subspace). Recall from Chapter 3 that left
translationdefinesaleftactionofΓonGwhosequotientisthecosetspace
G/Γ.
Proposition 12.14. Let Γ be a discrete subgroup of a connected, locally
path connected, locally compact Hausdorff topological group G. Then Γ acts
freely and properly on G by left translations, so the quotient map π: G →
G/Γ is a normal covering map.
Proof. As we observed in Example 3.35(e), G acts freely on itself, so the
restrictionofthisactiontoΓiscertainlyfree.Wewillshowthattheaction
is proper by showing that it satisfies property (b) of Proposition 12.9.
Let K ⊂ G be any compact set. If γ ∈ Γ is an element such that K ∩
γK (cid:14)= ∅, then there exist g1,g2 ∈ K such that g1 = γg2, which is to say
γ ∈ KK−1 = {g1g
2
−1 : g1,g2 ∈ K}. This set KK−1 is compact because it
is the image of K ×K under the continuous map from G×G to G given
by (g1,g2)(cid:10)→g1g
2
−1 . Because Γ is discrete, there can be only finitely many
elements of Γ in KK−1.
Corollary 12.15. SupposeGandH areconnected,locallypathconnected,
locally compact Hausdorff topological groups, and ϕ: G→H is a surjective
continuous homomorphism with discrete kernel. If ϕ is an open or closed
map, then it is a normal covering map.
Proof. Let Γ = Kerϕ. By the preceding proposition, the quotient map
π: G → G/Γ is a normal covering map. The assumption that ϕ is either
open or closed implies that it is a quotient map, and by the first isomor-
phism theorem the identifications made by ϕ are precisely those made by
π. Thus the result follows from the uniqueness of quotient spaces.
Example 12.16 (Coverings of the Torus). For any integers a,b,c,d
such that ad−bc (cid:14)= 0, consider the map p: T2 → T2 given by p(z,w) =
(zawb,zcwd). This is easily seen to be a surjective continuous homomor-
phism,anditisaclosedmapbytheclosedmaplemma.Onceweshowthat
it has discrete kernel, it will follow from the preceding corollary that it is
a normal covering map.
(cid:12) Le(cid:13)t A denote the invertible linear transformation of R2 whose matrix is
a b . Then we have a commutative diagram
c d
A(cid:2)
R2 R2
E E
(cid:5) (cid:5)
T2 (cid:2) T2 (12.2)
p

---

Proper Group Actions 271
where E(x,y) = (e2πix,e2πiy) is the universal covering map of the torus.
To identify Kerp, note that
p◦E(x,y)=(1,1) ⇐⇒ E◦A(x,y)=(1,1)
⇐⇒ A(x,y)∈Z2
⇐⇒ (x,y)∈A−1(Z2),
where A−1(Z2) denotes the additive subgroup {A−1(m,n) : (m,n) ∈ Z2}
of R2. Because E is surjective, this shows that Kerp=E◦A−1(Z2).
SinceA−1 hasrationalentries,itfollowseasilythateachelementofKerp
has finite order in T2. Moreover, since Z2 is generated (as a group) by the
two elements (1,0) and (0,1), Kerp is generated by their images under
E◦A−1. An abelian group that is generated by finitely many elements of
finite order is easily seen to be finite; in particular, it is discrete.
Application: Universal Coverings of Higher Genus Surfaces
As another application of the theory of proper group actions, we will show
that the unit disk B2 ⊂ C is the universal covering space of all the ori-
entable surfaces of genus n ≥ 2. The construction is rather involved, so
we will describe the main steps and leave some of the details for you to
work out. Some of these steps can be done a bit more straightforwardly if
you know a little about Riemannian metrics and their geodesics, but we
will not assume any such knowledge. We will, however, assume a passing
acquaintance with complex analysis, at least enough to understand what
it means for a function to be complex analytic.
We begin by describing a special metric on the disk. For z1,z2 ∈ B2,
define
(cid:20) (cid:21)
−1
2|z1 −z2 |2
d(z1,z2)=cosh 1+
(1−|z1 |2)(1−|z2 |2)
.
This is a metric, called the hyperbolic metric. (The only property of a
metricthatisnotstraightforwardtocheckisthetriangleinequality;away
to prove it is indicated in Problem 12-8.)
The disk with this metric, called the hyperbolic disk, is one model of
non-Euclideanplanegeometry.The“straightlines”inthisgeometry,called
hyperbolic geodesics,aretheintersectionswiththediskofEuclideancircles
andlinesmeetingtheunitcircleorthogonally(Figure12.6).(Alinesegment
throughtheorigincanbethoughtofasthelimitingcaseofacirculararcas
theradiusgoestoinfinity.)Itiseasytocheckthat“twopointsdeterminea
line”:Thatis,givenanytwopointsinthedisk,thereisauniquehyperbolic
geodesic passing through both points.

---

272 12. Classification of Coverings
0
FIGURE 12.6. Hyperbolic geodesics.
The most interesting feature of the hyperbolic metric is that it is pre-
served by a transitive group action. Let α and β be complex numbers with
|α|2−|β|2 >0, and define
αz+β
ϕ(z)= . (12.3)
βz+α
A straightforward calculation shows that ϕ is continuous, takes the
disk to itself, and preserves the hyperbolic metric in the sense that
d(ϕ(z1),ϕ(z2)) = d(z1,z2) for all z1,z2 ∈ B2. Any such map is called a
M¨obius transformation of the disk, and the set M of all such maps is a
group under composition, called the M¨obius group of the disk. It can be
(cid:12) (cid:13)
identified with the group of matrices of the form αβ and so is a topo-
β α
logical group acting continuously on B2.
M¨obius transformations take geodesics to geodesics, as can be seen by
substituting ϕ(z) for z in the equation defining a circle or line intersecting
theboundaryofthediskorthogonally,andnotingthatitreducestoanother
equation of one of the same types. In fact, the same computation shows
that a Mo¨bius transformation takes the intersection of the disk with any
Euclidean circle or line to another set of one of the same forms.
One special case worth noting is that any rotation of the disk z (cid:10)→ eiθz
is a Mo¨bius transformation with α = eiθ/2 and β = 0, so the hyperbolic
metricisinvariantunderrotations.In fact,anyM¨obiustransformationthat
takes the origin to itself must be of this form, because (12.3) reduces to
ϕ(z)=(α/α)z inthatcase.Observealsothatthehyperbolicdistancefrom
theorigintozdependsonlyon|z|,soanymetricballB (0)abouttheorigin
r
is actually a Euclidean disk centered at 0, and its boundary is a Euclidean
circle.SinceM¨obiustransformationspreservehyperbolicdistanceandtake
circles to circles, it follows that every metric ball is a Euclidean disk. (Its
Euclidean center may not be the same as its hyperbolic center, however).
ItalsofollowsthatthehyperbolicmetricgeneratestheEuclideantopology.

---

Proper Group Actions 273
The left action of M on the disk defined by (12.3) is transitive because
any z0 ∈B2 is carried to 0 by the M¨obius transformation
z−z0
ϕ(z)= . (12.4)
1−z0z
In fact, more is true: Given any two pairs of points z0,z1 and z
0
(cid:5),z
1
(cid:5) such
that d(z0,z1) = d(z
0
(cid:5),z
1
(cid:5)), there is a unique Mo¨bius transformation taking
z0 to z
0
(cid:5) and z1 to z
1
(cid:5) (and therefore taking the geodesic segment joining
z0,z1 to the one joining z
0
(cid:5),z
1
(cid:5)). To prove this, let ψ = ρ◦ϕ, where ϕ is
the transformation (12.4) and ρ is a rotation moving ϕ(z1) to the positive
x-axis, so that ψ takes z0 to 0 and z1 to some λ > 0. Similarly, there is
a transformation ψ(cid:5) taking z(cid:5) to 0 and z(cid:5) to λ(cid:5) > 0. Since M¨obius trans-
0 1
formations preserve distances, λ and λ(cid:5) are at the same distance from 0
along the positive x-axis and therefore must be equal, so ψ(cid:5)−1 ◦ψ is the
transformation we seek. It is unique because if γ is any M¨obius transfor-
mation taking z0 to z
0
(cid:5) and z1 to z
1
(cid:5), the composition ψ(cid:5) ◦γ ◦ψ−1 fixes 0
and therefore must be a rotation, and since it also fixes λ, it must be the
identity, which implies γ =ψ(cid:5)−1◦ψ.
Each M¨obius transformation ϕ is complex analytic with nowhere van-
ishing derivative. Multiplication by the complex derivative ϕ(cid:5)(z0) defines
a linear map from C to C, which can be interpreted geometrically as
the action of ϕ on tangent vectors to curves: For any differentiable pa-
rametrized curve f: (−ε,ε) → B2 with f(0) = z0, the chain rule gives
(ϕ◦f)(cid:5)(0) = ϕ(cid:5)(z0)f(cid:5)(0). Thus ϕ acts on tangent vectors by multiplying
them by the nonzero complex number ϕ(cid:5)(z0), and since all tangent vectors
are rotated through the same angle, every Mo¨bius transformation is con-
formal, meaning it preserves angles between tangent vectors. (We will also
be considering angles between geodesics, by which we always mean angles
between their tangent vectors.) In particular, if ϕ(z) = eiθz is rotation
through an angle θ, then ϕ(cid:5)(0) = eiθ rotates tangent vectors through the
same angle. It follows that the only M¨obius transformation that fixes the
origin and fixes the direction of a tangent vector at the origin is the iden-
tity. In fact, a Mo¨bius transformation that fixes any point and a tangent
direction at that point must be the identity, because conjugation with a
transformationtakingthefixedpointto0yieldsatransformationthatfixes
0 and a tangent direction at 0.
NowletM beacompactorientablesurfaceofgenusn≥2.Wewillshow
that there is a discrete subgroup Γ ⊂ M acting freely and properly on B2
suchthatM ishomeomorphictoB2/Γ.ItfollowsfromTheorem12.11that
the universal covering space of M is B2.
Recall from Chapter 6 the standard polygonal presentation of M as a
quotient of a polygonal region with 4n sides whose edges are identified in
pairs. We will realize M as a quotient of a compact region in B2 bounded
byageodesicpolygon,thatis,theunionoffinitelymanygeodesicsegments.
We begin by constructing a 4n-sided geodesic polygon whose edges have

---

274 12. Classification of Coverings
θ
P
θ ≈π−π/2n. θ ≈0. θ =π/2n.
FIGURE12.7.Geodesicpolygonswithinteriorangles0<θ<π−π/2n.
equal lengths and meet at equal angles (a regular geodesic polygon). Start
with 4n points (z0,z1,…,z4n = z0) equally spaced on some circle about
the origin. Because the hyperbolic metric is invariant under rotations, the
geodesic segments joining z j and z j+1 for j = 0,…,4n−1 all have the
same length and meet at equal angles, so their union is a regular geodesic
polygon. As the radius of the circle goes to zero, these geodesics approach
linesegmentsthroughtheorigin,anddefinesmallregulargeodesicpolygons
whoseinterioranglesareveryclosetowhattheywouldbeintheEuclidean
case, namely π −π/2n (see Figure 12.7). As the points get farther from
the origin, the arcs become nearly tangent to each other, defining geodesic
polygons with interior angles very near zero. By continuity, somewhere in
between there is a polygon whose interior angles are exactly θ = π/2n.
(Note that this does not work when n = 1, so we cannot construct a
covering of the torus in this manner.)
Let P be the compact subset of B2 consisting of this regular geodesic
polygon together with the bounded component of its complement. Choose
one vertex v0, and label the edges a1,b1,a −
1
1 ,b −
1
1 ,…,a
n
,b
n
,a−
n
1,b−
n
1 in
counterclockwise order starting from v0. (See Figure 12.8, but ignore the
−1
vertex labels other than v0 for now.) For each edge pair a
j
,a
j
, there is
−1
a unique Mo¨bius transformation α that takes the edge labeled a onto
j j
the one labeled a , with the initial vertex of one going to the initial vertex
j
−1
of the other. Similarly, let β be the transformation taking b to b and
j j j
respecting the initial and terminal vertices. Let Γ ⊂ M be the subgroup
generated by {α ,β : j = 1,…,4n}. We will call the generators α , β ,
j j j j
and their inverses edge pairing transformations.
One important property of the edge pairing transformations is easy to
verify: If σ is any edge pairing transformation, then P ∩σ(P) consists of
exactly one edge of P. To see why, suppose σ takes an edge e to another
edgee(cid:5).Thenclearly,P∩σ(P)containse(cid:5).Notethatthecomplementofany
geodesic in B2 has exactly two components, which we may call the sides of
thegeodesic.BecauseP isconnectedandliesononesideofeachofitsedges,
thesameistrueofσ(P).Usingconformalityandfollowingwhatσdoestoa
vector that is perpendicular toe and points into P, it is easy to check that

---

Proper Group Actions 275
v0
v3
a1
b1
v2
α1
−1
a
1
v1 β1
−1
b
1
v4
FIGURE 12.8. Edge pairing transformations.
σ(P)liesontheoppositesideofe(cid:5) fromP,andthereforeP∩σ(P)consists
of exactly the edge e(cid:5). Because P is obviously homeomorphic to a regular
Euclidean polygon, the quotient of P by the identifications determined by
the edge pairing transformations is homeomorphic to M. Let p: P → M
denote the quotient map.
Theorem 12.17. The group Γ is discrete and acts freely and properly on
B2, and the quotient B2/Γ is homeomorphic to M. The restriction of this
quotient map to P is p.
Proof. Thefirstthingwewillproveisthattheedgepairingtransformations
satisfythesamerelationasthegeneratorsofthefundamentalgroupof M:
α1 ◦β1 ◦α
1
−1◦β
1
−1◦···◦α
n
◦β
n
◦α
n
−1◦β
n
−1 =Id. (12.5)
Actually, it will be more convenient to prove the equivalent identity ob-
tained by inversion:
β
n
◦α
n
◦β
n
−1◦α
n
−1◦···◦β1 ◦α1 ◦β
1
−1◦α
1
−1 =Id. (12.6)
To simplify the notation, let us write the sequence of transformations on
the left-hand side of (12.6) as σ4n ◦···◦σ2 ◦σ1.
−1
By definition, σ1 = α
1
takes v0, the initial vertex of the edge labeled
−1
a1, to the initial vertex of the edge labeled a
1
. If we label the vertices in

---

276 12. Classification of Coverings
V3
3θ V0
V2
2θ α α−1
β−1
V1
θ
β
4θ
V4
FIGURE12.9.ImagesofavectorV0 underedgepairingtransformations.
counterclockwiseorderstartingfromv0 asv0,v3,v2,v1,v4 asinFigure12.8,
itiseasytocheckonestepatatimethatσ
j
takesv j−1tov
j
forj =1,…,4.
Since v4 is also the initial vertex of the edge labeled a2, we can continue
by induction to number all the remaining vertices v5 through v4n = v0 in
suchawaythatσ
j
(v j−1)=v
j
.Inparticular,σ4n ◦···◦σ2 ◦σ1(v0)=v0.To
show that this composition is the identity, it suffices to show that it fixes
a tangent direction at v0.
For any vertex v , we will measure angles of vectors at v from the edge
j j
adjacent to v
j
in the counterclockwise direction (so we measure from a1 at
−1
v0,fromb
1
atv1,etc.).Positiveangleswillalwaysbeunderstoodtomean
counterclockwise rotation from that edge. Let θ =π/2n be the measure of
the interior angles of P.
Let V0 be a nonzero vector that makes an angle of 0 at v0 (see Figure
12.9), and for j = 1,…,4n let V
j
be the image of V0 under σ
j
◦···◦σ1,
so that σ j takes V j−1 to V j . We will prove the following claim: For each j,
the angle of V at v is jθ. For j =0 this is immediate from the definition
j j
−1 −1
of V0. For j = 1, note that σ1 = α
1
takes a1 to a
1
, and therefore takes
−1
V0 toavectorV1 thatpointsinthedirectionofa
1
,whichmakesanangle
−1
θ with b . Next, since M¨obius transformations preserve angles, the image
1
−1
V2 of V1 under σ2 = β
1
makes an angle θ with b1, which is the same as
−1
an angle 2θ with a
1
. A similar analysis shows that the angles of V3 and
V4 are 3θ and 4θ, respectively, and the claim is then proved for all j by

---

Proper Group Actions 277
induction. In particular, the angle of V4n is 4nθ =2π, so V4n points in the
same direction as V0. This completes the proof of (12.5).
Now we have to prove that Γ is discrete and acts freely and properly
on B2. It seems to be impossible to prove this by directly analyzing the
action of Γ, so instead we resort to a rather circuitous trick due originally
toPoincar´e.Wewillconstruct“byhand”acoveringspaceofM thatought
to be its universal covering space, as a union of infinitely many copies of
P—one for each element of π1(M)—with “adjacent” copies glued together
bytheidentificationsdeterminedbytheedgepairingtransformations.Only
later will we show that this space is homeomorphic to B2, and therefore is
simply connected and so is in fact the universal covering space.
Let G be the abstract group with presentation (cid:22)α1,β1,…,α
n
,β
n
|
α1β1α
1
−1 β
1
−1···α
n
β
n
α
n
−1β
n
−1(cid:23), which is isomorphic to π1(M). Let ∼ be
the equivalence relation on G×P generated by all relations of the form
(g,σ(z)) ∼ (gσ,z), where σ is an edge pairing transformation and both z
(cid:8)
and σ(z) are points in∂P. Give G the discrete topology, and letM denote
the quotient space G×P/∼. We will denote the equivalence class of (g,z)
in M (cid:8) by [g,z], and the quotient map by π: G×P →M (cid:8) .
Left translation in the G factor defines a natural continuous action of G
on G×P. This respects the identifications made by π, so it descends to a
continuous action of G on M (cid:8) , satisfying g(cid:5)· [g,z] = [g(cid:5)g,z]. This action is
free, because (g(cid:5)g,z)∼(g,z) only when g(cid:5) =1.
The subset P (cid:7) = π({1}×P) = {[1,z] : z ∈ P} of M (cid:8) is homeomorphic
to P (why?), and M (cid:8) is the union of the sets g · P (cid:7) = {[g,z] : z ∈ P} as g
(cid:8)
ranges over G. Each of these sets is a homeomorphic copy of P in M, and
thecopiesg · P (cid:7) andg(cid:5)· P (cid:7) intersectinanedgepreciselywheng andg(cid:5) differ
by a single edge pairing transformation. Since there are only finitely many
· (cid:7)
suchtransformations,thismeansinparticularthateachsetg P intersects
only finitely many others.
Because ∼ identifies only points (g,z) with z ∈ ∂P, the fiber of π over
any point [g0,z0] for z0 ∈ IntP consists of exactly one point (g0,z0) ∈
G×P. If z0 is in ∂P but is not a vertex, then z0 lies on one edge, and
there is exactly one edge pairing transformation σ that identifies that edge
with another edge; thus the fiber over [g0,z0] is exactly two points (g0,z0)
and (gσ−1,σ(z0)). If z0 is a vertex of P, then by the argument at the
beginning of the proof there is a sequence of edge pairing transformations
σ1,…,σ4n (possibly a cyclic permutation of the sequence we considered
earlier) such that the points z
j
=σ
j
◦···◦σ1(z0) are the vertices of P, so
−1 −1 −1
the fiber over [g0,z0] consists of the 4n points (g0σ
1
,z1), (g0σ
1
σ
2
,z2),
… , (g0σ
1
−1···σ
4
−
n
1
,z4n )=(g0,z0).

---

278 12. Classification of Coverings
There is a natural continuous map p(cid:7): M (cid:8) → M given by p(cid:7)[g,z] = p(z),
obtained from p◦π2 by passing to the quotient:
G×P
π2(cid:2)
P
π p
(cid:5) (cid:5)
(cid:8) (cid:2)
M p(cid:7) M.
Clearly, p(cid:7) is surjective, because p(cid:7)(P (cid:7) ) = M. It is a quotient map for the
following reason: If U ⊂M (cid:8) is an open set that is saturated with respect to
p(cid:7),thenπ−1(U)⊂G×P isopenandsaturatedwithrespecttop(cid:7)◦π =p◦π2,
and since p◦π2 is a quotient map, it follows that p(cid:7)(U)=p(cid:7)◦π(π−1(U))=
p◦π2(π−1(U)) is open. You can check that the fibers of p(cid:7)are precisely the
(cid:8) (cid:8)
orbitsofGinM,sowecanidentifyM withtheorbitspaceM/G.Wewish
to show that p(cid:7)is actually a covering map.
To show that p(cid:7)is a covering, by Theorem 12.11 it suffices to show that
(cid:8)
M is connected, locally path connected, locally compact, and Hausdorff,
(cid:8)
and that the action of G on M is proper. Connectedness is easy: If σ is an
edge pairing transformation taking edge e to edge e(cid:5), then the connected
sets P (cid:7) and σ · P (cid:7) have the points [1,σ(z)]=[σ,z] in common for z ∈e, so
P (cid:7)∪(σ · P (cid:7) ) is connected. By induction, any set of the form P (cid:7)∪(σ1 · P (cid:7) )∪
···∪(σ
m
···σ1) · P (cid:7) is connected. Since M (cid:8) is the union of all such sets, and
(cid:7) (cid:8)
they all have points of P in common, M is connected.
(cid:8)
ToprovetheotherpropertiesofM,wefirstneedtointroducesomemore
maps. Let τ: G → Γ be the homomorphism that sends each generator α
i
orβ toitself(thoughtofasanelementofΓ),whichiswell-definedbecause
i
(12.5) holds in Γ. The map G × P → B2 defined by (g,z) (cid:10)→ τ(g)z is
continuous and respects the identifications made by ∼, so it descends to a
continuous map δ: M
(cid:8)→B2
given by δ[g,z]=τ(g)z. It takes the action of
G on M (cid:8) over to the action of Γ on B2, in the sense that
·
δ(g x)=τ(g)◦δ(x). (12.7)
ThemostimportantfeatureofM (cid:8) isthateveryx∈M (cid:8) hasaneighborhood
U with the following properties:
(i) U is mapped homeomorphically by δ onto a closed hyperbolic ball
B (δ(x))⊂B2.
ε
(ii) δ(U)=B (δ(x)).
ε
(iii) U intersects the sets g · P (cid:7) for only finitely many g ∈G.
We will call any such set U a regular hyperbolic neighborhood of x.

---

Proper Group Actions 279
Fromtheexistenceofregularhyperbolicneighborhoodsitfollowsimme-
diately that
- M (cid:8) islocallycompactandlocallypathconnected,becauseeachregular
hyperbolic neighborhood has these properties.
- M (cid:8) is Hausdorff: Let x,x(cid:5) ∈ M (cid:8) , and let U, U(cid:5) be regular hyperbolic
neighborhoodsofthem.Ifx(cid:5) (cid:14)∈U,thenshrinkingU abitifnecessary
we may assume x(cid:5) (cid:14)∈ U, so that U and U(cid:5) (cid:3)U are disjoint neigh-
borhoods of x and x(cid:5). On the other hand, if x(cid:5) ∈U, then the inverse
imagesunderδ| ofdisjointneighborhoodsofδ(x)andδ(x(cid:5))areopen
U
sets separating x and x(cid:5).
- The action of G on M (cid:8) is proper: With x, x(cid:5), U, and U(cid:5) as above,
there can be at most finitely many g ∈G such that U∩(g · U(cid:5))(cid:14)=∅,
because U and U(cid:5) intersect only finitely many of the sets g · P (cid:7) .
Thus, to complete the proof that p(cid:7)is a covering map, we need only prove
the existence of a regular hyperbolic neighborhood of each point.
(cid:8)
Let x=[g0,z0] be an arbitrary point of M. The fiber over x consists of
finitelymanypointsoftheform(g
j
,z
j
),wherez
j
=σ
j
◦···◦σ1(z0)forsome
(possibly empty) sequence of edge transformations σ1,…,σ
j
and g
j
=
g0σ
1
−1···σ
j
−1
. (The fiber contains one, two, or 4n such points depending
onwhetherz0 isaninteriorpoint,anedgepoint,oravertex.)Chooseε>0
smaller than half the distance from z0 to any edge that does not contain
z0. Let W ⊂ G×P be the union of the sets {g
j
}×(B
ε
(z
j
)∩P), and let
U = π(W). Because W is a saturated open set, U is a neighborhood of x
inM (cid:8) .Similarly,W istheunionofthesets{g }×(B (z )∩P),asaturated
j ε j
· (cid:7)
closed set, so π(W)=U. Clearly, U intersects g P for only finitely many
g.
To complete the proof that U is a regular hyperbolic neighborhood, we
need to show that δ is a homeomorphism from U to B
ε
(z0) taking U to
B
ε
(z0). Since the diagram
δ (cid:2)
U B (δ(x))
ε
g τ(g)
(cid:5) (cid:5)
· (cid:2) ·
g U B (δ(g x))
δ ε
commutes for each g ∈ G and the vertical maps are homeomorphisms, it
suffices to prove this for x=[1,z0]∈P (cid:7) . We consider three cases.
Case I: z0 ∈ IntP. In this case, U ⊂ P (cid:7) , and it is immediate from the
definitions that δ is one-to-one on U, δ(U) = B
ε
(z0), and δ(U) = B
ε
(z0).
Since U is the image under π of a compact set, it is compact, so δ: U →
B
ε
(z0) is a homeomorphism by the closed map lemma.

---

280 12. Classification of Coverings
z0
{1}×P
(cid:7)
δ
P
z1
{σ−1}×P
FIGURE 12.10. Hyperbolic neighborhood of an edge point.
Case II: z0 ∈ ∂P, but z0 is not a vertex. Let e0 denote the edge con-
taining z0. By our choice of ε, B
ε
(z0)∩P contains the entire portion of
B
ε
(z0) lying on one side of e0 (Figure 12.10). There is one edge pairing
transformation σ that takes e0 to another edge e1, and thus takes z0 to
z1 =σ(z0)∈e1. As a Mo¨bius transformation of B2, σ takes B
ε
(z0) home-
omorphically onto B
ε
(z1). Since B
ε
(z0)∩P and σ−1(B
ε
(z1)∩P) lie on
opposite sides of e0, B
ε
(z0)=(B
ε
(z0)∩P)∪σ−1(B
ε
(z1)∩P). Then
δ(U)=δ (cid:7) (W)=(B
ε
(z0)∩P)∪σ−1(B
ε
(z1)∩P)=B
ε
(z0).
The restriction of δ to U is one-to-one, takes U onto B
ε
(z0), and as before
is a homeomorphism by the closed map lemma.
Case III:z0 is a vertex of P.Thenδ(U)=δ (cid:7) (W)istheunionofthesets
δ (cid:7) ({σ −1···σ −1}×(B (z )∩P))=σ −1◦···◦σ −1 (B (z )∩P),
1 j ε j 1 j ε j
wherez1,…,z4n aretheverticesofP.Toseewhatthesesetsare,lookback
attheproofof (12.5);fromthatanalysis,itfollowsthatσ
−1◦···◦σ −1
maps
1 j
z
j
to z0 and maps B
ε
(z
j
)∩P to the sector of B
ε
(z0) lying between the
geodesics passing through z0 at angles −jθ and (−j+1)θ (Figure 12.11).
These sectors fit together to make up the entire closed ball B
ε
(z0), and
δ maps U bijectively to B
ε
(z0). As above, it is a homeomorphism by the
closed map lemma.

---

Proper Group Actions 281
δ(U)
P
FIGURE 12.11. Hyperbolic neighborhood of a vertex point.
This completes the proof of the existence of hyperbolic neighborhoods
andthustheproofthatp(cid:7): M (cid:8)→M isacoveringmap.Tofinishtheproofof
thetheorem,wewillshowthatδ: M (cid:8)→B2 isalsoacoveringmap.SinceB2
is simply connected, this implies that δ is a homeomorphism. The theorem
follows from this, as we now show.
First, τ: G→Γ is a group isomorphism: It is surjective because it takes
generators of G to generators of Γ; and it is injective because if τ(g)=Id,
then for any x ∈ M (cid:8) we have δ(g · x) = τ(g)δ(x) = δ(x), which implies
·
g x=xandthereforeg =1becauseGactsfreely.Itfollowsthattheaction
ofΓonB2isequivalenttothatofGonM (cid:8) underthehomeomorphismδ,and
thequotientmapB2 →B2/Γisequivalenttothecoveringmapp(cid:7): M (cid:8)→M.
Therefore, the action of Γ on B2 is free and proper, and the restriction of
thecoveringmaptoP isp(cid:7)◦δ−1| =p.ToseethatΓisadiscretesubgroup
P
of M, suppose γ → γ in Γ. By continuity γ z → γz for any z ∈ B2, and
i i
setting g =τ−1(γ ), g =τ−1(γ), and x=δ−1(z) we obtain g · x→g · x.
i i i
Since the g ’s are covering transformations, this can happen only if g =g
i i
(and therefore γ =γ) for all sufficiently large i.
i
Toshowthatδ isacovering,weneedthefollowingadditionalfactabout
regularhyperbolicneighborhoods:There exists some r >0 such that every
point x ∈ M (cid:8) has a regular hyperbolic neighborhood U whose closure is
x
mapped homeomorphically by δ onto B (δ(x)). To prove this, let K ⊂ M (cid:8)
r
(cid:7) · (cid:7)
denote the union of P together with its images σ P under the 4n edge
i
pairing transformations σ . Since K is compact, so is its image δ(K)⊂B2,
i
and it is easy to see that δ(K) contains a neighborhood of P. As U ranges
over regular hyperbolic neighborhoods of points in K, the sets δ(U) form
an open cover of δ(K). Let c be a Lebesgue number for this cover, and
choose r < c small enough that for each z ∈ P the hyperbolic ball B (z)
r
is contained in δ(K). This means that for every z ∈ P, there is a regular

---

282 12. Classification of Coverings
(cid:7)
P P
U δ(U)
x
δ(x)
x0
U
δ(x0)
x0
FIGURE 12.12. Finding regular hyperbolic balls of fixed radius.
hyperbolic neighborhood U of some point x∈K such that B (z)⊂δ(U).
r
For each x0 ∈ P (cid:7) , choose a regular hyperbolic neighborhood U of some
x ∈ K such that B
r
(δ(x0)) is contained in δ(U) (Figure 12.12), and let
U
x0
= (δ|
U
)−1(B
r
(δ(x0)); then δ: U
x0
→ B
r
(δ(x0)) is the restriction of a
homeomorphism and hence is itself a homeomorphism. Since δ is injective
o
o
t
n
h
P
e
(cid:7)
r
a
x
nd
∈
δ
M (cid:8)
(x
,
0)
th
∈
er
δ
e
(U
is
x0
s
)
o
,
m
U
e
x0
g
is
∈
th
G
e d
su
e
c
si
h
re
t
d
ha
n
t
ei
g
gh
·
b
x
orh
∈
oo
P (cid:7)
d
,
o
s
f
o
x
w
0
e
. F
c
o
a
r
n
a
s
n
e
y
t
U
=g−1·
U
·
.
x g x
We can now prove that δ is a covering map. First we need to show that
(cid:8)
it is surjective. If it were not, the image set δ(M) would have a boundary
point z0 ∈ B2. There is some point z ∈ δ(M (cid:8) ) whose distance from z0 is
less than r/2. But then z = δ(x) for some x ∈ M (cid:8) , and δ(U ) = B (z),
x r
which is a neighborhood of z0. This contradicts the assumption that z0 is
a boundary point of the image.
For any z0 ∈ B2, we will show that B r/2(z0) is evenly covered. Let V
beacomponentofδ−1(B r/2(z0))inM (cid:8) .SinceM (cid:8) islocallypathconnected,
V is open. We need to show that δ: V → B r/2(z0) is a homeomorphism.
Choose x∈V, set z =δ(x), and let σ =(δ| )−1: B (z)→U .
Now, σ(B r/2(z0)) is a connected subset of
U
δ
x−1(B
r/
r
2(z0)) tha
x
t contains a
point x in common with V, so it must be contained in V. This implies, for
any z(cid:5) ∈B r/2(z0), that δ(σ(z(cid:5)))=z(cid:5), so δ: V →B r/2(z0) is surjective.
On the other hand, ∂B
r
(z) is disjoint from B r/2(z0) by the triangle
inequality.Sinceδ takes∂U to∂B (z),itfollowsthat∂U ∩V =∅.Now,
x r x
V ∩U is open in M (cid:8) and therefore open in V, and V ∩U = V ∩U is
x x x
closed in V. Since V is connected, V ∩U is all of V, which means that
x
V ⊂U . Thus δ| is the restriction of a homeomorphism, so it is injective
x V
and open, and therefore δ: V →B r/2(z0) is a homeomorphism.

---

The Classification Theorem 283
Corollary 12.18. Let M be a compact surface. The universal covering
space of M is homeomorphic to
(a) S2 if M ≈S2 or P2;
(b) R2 if M ≈T2 or P2#P2;
(c) B2 if M is any other surface.
Proof. ThiswasprovedforalltheorientablesurfacesandP2inthischapter.
If M is a connected sum of n≥2 projective planes, then by Problem 11-8
M hasatwo-sheetedcoveringbytheorientablesurfaceN ofgenusn−1.If
(cid:8) (cid:8)
M istheuniversalcoveringspaceofM,thenM alsocoversN byCorollary
12.6(a), so M and N have the same universal covering space.
Note that R2 and B2 are homeomorphic, so up to topological equiva-
lence there are only two simply connected 2-manifolds that cover compact
surfaces. It is useful, however, to distinguish the two cases because of the
differentcharacteroftheircoveringtransformations.Forexample,thecov-
ering transformations for the torus are all translations of the plane that
preserve the Euclidean metric, while for the higher genus orientable sur-
faces they are M¨obius transformations.
The Classification Theorem
In this section we assemble the results of this chapter to come up with
a complete classification of coverings of a given space. The idea is that
every covering of X is itself covered by the universal covering space, and
intermediatecoveringscanbebuiltfromtheuniversalcoveringasquotients
by suitable group actions.
Theorem 12.19 (Classification of Coverings). LetX beaconnected,
locally simply connected, locally compact Hausdorff space (for example, any
connected manifold), and let q ∈ X be any base point. There is a one-to-
one correspondence between isomorphism classes of coverings of X and
conjugacy classes of subgroups of π1(X,q). The correspondence associates
each covering p(cid:5): X(cid:5) →X with the conjugacy class of its induced subgroup.
Proof. The covering isomorphism theorem shows that there is at most one
isomorphism class of coverings corresponding to any conjugacy class of
subgroups, so all we need to show is that there is at least one. Let H ⊂
π1(X,q) be any subgroup in the given conjugacy class. Let p: X (cid:7) → X be
the universal covering of X, and choose a base point q(cid:7)∈p−1(q). Then the
simply connected case of the covering group structure theorem (Corollary
11.32) shows that π1(X,q) is isomorphic to the covering group C
p
(X (cid:7) ),

---

284 12. Classification of Coverings
under the map α: π1(X,q)→C
p
(X (cid:7) ) that sends [f] to the unique covering
transformation ϕ taking q(cid:7)to q(cid:7) · [f]. Let H (cid:7) =α(H)⊂C (X (cid:7) ).
p
Since C (X (cid:7) ) acts freely and properly on X (cid:7) , it follows easily that H (cid:7) does
p
too.SoletX(cid:5) denotethequotientspaceX (cid:7) /H (cid:7) andπ: X (cid:7) →X(cid:5) thequotient
map;byTheorem12.11,π isanormalcoveringmap.Moreover,p: X (cid:7) →X
is constant on the fibers of π (since they are contained in the fibers of p),
so p descends to a continuous map p(cid:5): X(cid:5) → X such that the following
diagram commutes:
(cid:7)
X
(cid:6) π
(cid:6)(cid:7)
p X(cid:5)
(cid:3)p(cid:5)
(cid:5)(cid:3)(cid:9)
X.
We have to show that p(cid:5) is a covering map. Let q1 ∈ X be arbitrary,
let U be a neighborhood of q1 that is evenly covered by p, and let U(cid:5) be
any component of p(cid:5)−1(U). To show that p(cid:5) is a covering map, it suffices
to show that U(cid:5) is mapped homeomorphically onto U by p(cid:5).
Because X(cid:5) is locally path connected, U(cid:5) is open and closed in p(cid:5)−1(U).
Thusπ−1(U(cid:5))isopenandclosedinπ−1(p(cid:5)−1(U))=p−1(U),whichimplies
that it is a union of components of p−1(U). If U (cid:7) is any such component,
the following diagram commutes:
(cid:7)
U
(cid:6) π
(cid:6)(cid:7)
p U(cid:5)
(cid:3)p(cid:5)
(cid:5)(cid:3)(cid:9)
(12.8)
U.
In this diagram, p = p(cid:5)◦π is a homeomorphism, so π is injective on U (cid:7) . If
π(U (cid:7) )(cid:14)=U(cid:5), then
(cid:5)
π(π−1(U(cid:5)))= π(ϕ(U (cid:7) ))=π(U (cid:7) )(cid:14)=U,
ϕ∈H (cid:7)
which contradicts the fact that π: X (cid:7) →X(cid:5) is surjective. Thus π: U (cid:7) →U(cid:5)
is bijective, and because it is an open map, it is a homeomorphism. Since
p and π are homeomorphisms in (12.8), so is p(cid:5).

---

The Classification Theorem 285
ϕ(q(cid:7)) (cid:7)
X
ϕ
q(cid:7)
(cid:7)
f
π
p
X(cid:5)
q(cid:5)
f
p(cid:5)
X
q p(cid:5)◦f
FIGURE 12.13. Proof of the classification theorem.
The last step is to show that p(cid:5)
∗
π1(X(cid:5),q(cid:5)) = H for some q(cid:5) ∈ X(cid:5) such
that p(cid:5)(q(cid:5))=q. Let q(cid:5) =π(q(cid:7)) and consider the following diagram:
π1(X(cid:5),q(cid:5))
α(cid:2)(cid:5)
C
π
(X (cid:7) )
p(cid:5) ι
∗
(cid:5) (cid:5)
π1(X,q) α (cid:2) C p (X (cid:7) ),
where α(cid:5) and α represent the isomorphisms given by the covering group
structure theorem, and ι is inclusion.
If this diagram commutes, we are done, because then
p(cid:5)
∗
π1(X(cid:5),q(cid:5))=α−1◦ι◦α(cid:5)(π1(X(cid:5),q(cid:5)))
=α−1◦ι(C (X (cid:7) ))
π
=α−1(H (cid:7) )=H.
Toseethatitcommutes,let[f]∈π1(X(cid:5),q(cid:5))bearbitrary,andletϕ=α(cid:5)[f],
soϕtakesq(cid:7)toq(cid:7) · [f]=f (cid:7) (1),wheref (cid:7) istheliftoff toapathinX (cid:7) starting
at q(cid:7)(Figure 12.13). Then ι◦α(cid:5)[f]=ϕ, thought of as an element of C (X (cid:7) ).
p
On the other hand, α◦p(cid:5)[f] = α[p(cid:5)◦f] is the transformation ψ ∈ C (X (cid:7) )
∗ p
taking q(cid:7)to p (cid:4)(cid:5)◦f(1). Now, p◦f (cid:7) = p(cid:5) ◦π ◦f (cid:7) = p(cid:5) ◦f, so f (cid:7) is the lift of
p(cid:5)◦f starting at q(cid:7), which implies that p (cid:4)(cid:5)◦f(1) = f (cid:7) (1). Thus ϕ = ψ and
the diagram commutes.

---

286 12. Classification of Coverings
We end with a pair of interesting and representative examples.
Example 12.20 (Coverings of Lens Spaces). By the preceding the-
orem, the coverings of the lens space L(n,m) are in one-to-one corre-
spondence with subgroups of Z/(cid:22)n(cid:23). (Since Z/(cid:22)n(cid:23) is abelian, each con-
jugacy class contains precisely one subgroup.) Since every subgroup of a
cyclic group is cyclic (Exercise A.27), the only possibilities for subgroups
G ⊂ π1(L(n,m)) are cyclic groups of order p where p is a factor of n. In
each such case, a covering of L(n,m) is obtained by restricting the action
of Z/(cid:22)n(cid:23) on S3 to G, and mapping the resulting quotient space down to
L(n,m)bysendingeachG-equivalenceclasstoitsZ/(cid:22)n(cid:23)-equivalenceclass.
If n = pq for positive integers p and q, let G ⊂ Z/(cid:22)n(cid:23) be the cyclic sub-
group of order p generated by (the coset of) q. It is easy to check from
the definitions that S3/G = L(p,m), and we obtain a q-sheeted covering
L(p,m) → L(n,m). These are the only coverings of the lens spaces up to
isomorphism.
Our last application will be to classify all the coverings of the torus up
to isomorphism.
Proposition 12.21 (Classification of Torus Coverings). Every cov-
ering of T2 is isomorphic to precisely one of the following:
(a) the universal covering E :R2 →T2;
(b) the coverings p:S1×R→T2 by p(z,y)=(zaε(y)b,zbε(y)−a), where
(a,b) are integers with a≥0 and b>0 if a=0;
(c) the coverings p:T2 →T2 by p(z,w)=(zawb,wc), where (a,b,c) are
integers with 0≤b<a and c>0.
Proof. Note that all of these maps are coverings: the universal cover by
Example11.3;themapsinpart(b)byProblem12-7;andthoseinpart(c)
by Example 12.16.
Let us use q = (1,1) ∈ T2 as base point, and represent π1(T2,q) as the
productgroup(cid:22)β(cid:23)×(cid:22)γ(cid:23),whereβ andγ arethepathclassesofthestandard
generatorofπ1(S1,1)inthefirstandsecondfactors,respectively.Thenthe
map (m,n)(cid:10)→βmγn is an isomorphism of Z2 with π1(T2,q).
The classification theorem says that isomorphism classes of coverings of
T2 are in one-to-one correspondence with subgroups ofπ1(T2,q) under the
correspondence that matches a covering p : X → T2 with the subgroup
induced by p. So we begin by showing that each subgroup of Z2 is one and
only one of the following:
(i) the trivial subgroup;
(ii) infinite cyclic subgroups generated by (a,b) satisfying the conditions
of (b) above;

---

The Classification Theorem 287
(iii) subgroups of the form Z(cid:22)(a,0),(b,c)(cid:23), where (a,b,c) satisfy the con-
ditions of (c) above.
To prove this, let G be an arbitrary subgroup of Z2. Because Z2 is free
abelian of rank 2, G is free abelian of rank at most 2 by Proposition 9.13.
Thus there are three mutually exclusive cases, in which G has rank 0, 1,
or 2. Clearly, the trivial subgroup has rank 0; we will show that the rank 1
and 2 cases correspond to (ii) and (iii), respectively.
IfGhasrank1,itiscyclic.Inthiscasetherearetwoelements(a,b)and
(−a,−b) that generate G, and exactly one of these satisfies the conditions
of (b). Thus (i) corresponds to the rank 1 case.
It remains to show that when G has rank 2 there are unique integers
(a,b,c)satisfyingtheconditionsin(c)suchthat{(a,0),(b,c)}formsabasis
for G. The subgroup G1 = G∩(Z×{0}) is not trivial: If {(m,n),(i,j)}
is any basis for G, then j(m,n)−n(i,j) is an element of G in Z×{0},
which is not (0,0) because of the independence of (m,n) and (i,j). Since
Z×{0} is cyclic, so is G1. Let (a,0) be a generator of G1; replacing it by
its negative if necessary, we may assume a>0.
Since G has rank 2, it is not contained in G1. As in the proof of Propo-
sition 9.13, there is a basis for G of the form {(a,0),(b,c)}, where c is a
generator of the image of G under the projection π2: Z2 → Z. Replacing
(b,c) by its negative if necessary, we may assume c > 0. Subtracting a
multiple of (a,0) from (b,c) (which still yields a basis), we may assume
0≤b<a.Thuswehavefound(a,b,c)satisfyingtheconditionsin(c)such
that (a,0) and (b,c) are a basis for G.
Finally, we need to show that two such triples (a,b,c) and (a(cid:5),b(cid:5),c(cid:5))
that determine the same subgroup are identical. Since each basis can be
expressed in terms the other, there is an integer matrix M such that
(cid:20) (cid:21) (cid:20) (cid:21)
a b a(cid:5) b(cid:5)
M = .
0 c 0 c(cid:5)
ExaminingthelowerleftentryinthisequationshowsthatM isalsoupper
triangular. Since M has an inverse that also has integer entries, its deter-
minant must be ±1; and then the above equation shows that detM = 1
(recallthata,c,a(cid:5),andc(cid:5) areallpositive).SinceM isuppertriangular,its
determinant is the product of its (integer) diagonal entries, so these must
be both +1 or both −1; and then the fact that a and a(cid:5) are both positive
forces both diagonal entries to be 1, so a=a(cid:5) and c=c(cid:5). The upper right
entry of the matrix equation then becomes ak +b = b(cid:5) (where k is the
upper right entry of M). Since both b and b(cid:5) satisfy 0 ≤b<a, this forces
k =0, so M is the identity.
To complete the proof, we need to check that the subgroups of π1(T2,q)
induced by the covering maps (a), (b), (c) are exactly those corresponding
to (i), (ii), (iii), respectively.
Case (a) is obvious, since the fundamental group of R2 is trivial.

---

288 12. Classification of Coverings
For (b), note that the fundamental group of S1 ×R is infinite cyclic,
generated by the path class of the loop c(t) = (α(t),0). The image of
this loop under p is p◦c(t) = (α(t)a,α(t)b), which represents the element
βaγb ∈π1(T2,q).UnderourisomorphismwithZ2,thiscorrespondsto(a,b)
and generates the infinite cyclic group described in (ii).
For (c), it is easy to check that p carries the generators β and γ of
π1(T2,q) to βa and βbγc. Under our isomorphism with Z2, the subgroup
generated by these elements is exactly the one described in (iii).

---

Problems 289
Problems
12-1. Let E be the following subset of R3×R3:
E ={(x,y)∈R3×R3 :x(cid:14)=y}.
Define an equivalence relation in E by setting (x,y) ∼ (y,x) for all
(x,y)∈E. Compute the fundamental group of E/∼.
12-2. Let M =T2#T2.
(a) ShowthatthefundamentalgroupofM hasasubgroupofindex
2.
(cid:8)
(b) ProvethatthereexistsamanifoldM andatwo-sheetedcovering
map p: M
(cid:8)→M.
12-3. Consider the map f: S1 →T2 given by
f(z)=(z2,1).
For which coverings p: X (cid:7) →T2 can f be lifted to X (cid:7) ?
·
12-4. Consider the action of Z on Rm(cid:3){0} defined by n x=2nx.
(a) Show that Z acts continuously, freely, and properly.
(b) Show that the orbit space (Rm (cid:3){0})/Z is homeomorphic to
Sm−1×S1.
(c) If m ≥ 3, show that the universal covering space of Sm−1×S1
is homeomorphic to Rm(cid:3){0}.
12-5. Identify a group Γ of homeomorphisms of the plane, generated by
translations and reflections, such that R2/Γ is homeomorphic to the
Klein bottle.
12-6. Show that any continuous action of a finite group on a manifold is
proper.
12-7. For any integers a,b,c,d such that ad−bc (cid:14)= 0, show that the map
p : S1 ×R → T2 given by p(z,y) = (zaε(y)b,zcε(y)d) is a covering
map. [Hint: Using a commutative diagram similar to (12.2), show
thatpisanopenmapandacontinuoushomomorphismwithdiscrete
kernel.]
12-8. Prove the triangle inequality for the hyperbolic metric as follows.
Show that it suffices to assume that one of the points is the origin,

---

290 12. Classification of Coverings
and use the identity cosh 2 x−sinh 2 x=1 to show that sinhd(z,0)=
2|z|/(1−|z|2), and therefore by the Euclidean triangle inequality,
coshd(z1,z2)≤coshd(z1,0)coshd(z2,0)+sinhd(z1,0)sinhd(z2,0)
=cosh(d(z1,0)+d(0,z2)).
12-9. Let G be a connected, locally simply connected, locally compact
(cid:7)
Hausdorfftopologicalgroup,andletGbeitsuniversalcoveringspace.
(cid:7)
ShowthatGhasauniquegroupstructuresuchthatitisatopological
groupandsuchthatthecoveringmapp: G (cid:7) →Gisahomomorphism
with discrete kernel.

---

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
To see how this can lead to different results, let X = T2 #T2 be the
two-holed torus, and consider the loop f in X pictured in Figure 13.1. (It
goes once around the boundary of the disk that is removed to form the
connected sum.) In terms of our standard generators for π1(X), this loop
−1 −1 −1 −1
is path homotopic to either α1β1α
1
β
1
or β2α2β
2
α
2
, so it is not null
f
FIGURE 13.1. A loop that extends to a surface map.

---

292 13. Homology
homotopic,anditscirclerepresentativehasnoextensiontoamapfromthe
closed disk into X. However, it is easy to see that the circle representative
does extend to a map from T2 minus a disk into X—for example, the
inclusion map of the left half of X is such an extension.
It turns out that a more satisfactory theory results if instead of con-
sidering loops modulo those that extend to maps from a 2-manifold with
boundary,weconsiderinsteadformalsumsofmapsfroma1-simplexmod-
ulothosethatare“boundaries”ofsumsofmapsfroma2-simplex.Getting
the definitions correct requires some care, and it is easy to lose sight of the
geometricmeaningamongthetechnicaldetails,butitwillhelpifyoukeep
theaboveexampleinmindthroughoutthediscussion.Therewardisathe-
ory that extends easily to higher dimensions, is computationally tractable,
and will allow us to prove a number of significant facts about manifolds
that are much more difficult or even impossible to prove using homotopy
groups alone.
Webeginthechapterbydefiningasequenceofabeliangroupsattachedto
eachtopologicalspace,calleditssingularhomologygroups,whichformalize
the intuitive discussion above. It follows immediately from the definition
that these groups are topological invariants, and with a bit more work we
show they are also homotopy invariants. Next we prove that there is a
simple relationship between the first homology group H1(X) and the fun-
damentalgroup,namelythatH1(X)isnaturallyisomorphictotheabelian-
ization of π1(X). Then we introduce one of the main tools for computing
homology groups, the Mayer–Vietoris theorem, which is a homology ana-
logue of the Seifert–Van Kampen theorem. Using these tools, we compute
thehomologygroupsofmostofthespaceswehavestudiedsofar.Wethen
describe some applications of homology: to the topological invariance of
the dimension of a manifold, the existence of vector fields on spheres, and
(using a different homology theory called simplicial homology) the topo-
logical invariance of the Euler characteristic of a polyhedron. In the final
section we give a brief introduction to cohomology.
Singular Homology Groups
We begin with some definitions. For any integerp≥0, let Δ ⊂Rp denote
p
the Euclidean simplex (cid:22)e0,e1,…,e
p
(cid:23), where e0 = 0 and, for 1 ≤ i ≤ p,
e = (0,…,1,…,0) is the vector with a 1 in the ith place and zeros
i
elsewhere. We call Δ the standard p-simplex. If X is a topological space,
p
a singular p-simplex in X is a continuous map σ: Δ → X. For example,
p
a singular 0-simplex is just a map from the one-point space Δ0 into X,
which we may identify with a point in X; and a singular 1-simplex is a
map from Δ1 = [0,1] ⊂ R into X, which is just a path in X. (A map is
generally called “singular” if it fails to have some desirable property such

---

Singular Homology Groups 293
as continuity or differentiability. In this case, the term singular is meant
to reflect the fact that σ need not be an embedding, so its image may not
look at all like a simplex.)
Let C (X) denote the free abelian group generated by the set of all
p
singular p-simplices in X. An element of C (X), which can be written as a
p
formal linear combination of singular simplices with integer coefficients, is
called a singular p-chain in X, and the group C (X) is called the singular
p
chain group in dimension p.
There are some special singular simplices in Euclidean spaces that we
will use frequently. Let K ⊂ Rn be a convex subset. For any p+1 points
v0,…,v
p
∈ K (not necessarily in general position or even distinct), let
α(v0,…,v
p
): Δ
p
→ Rn denote the restriction of the unique affine map
that takes e to v for i = 0,…,p. By convexity, the image lies in K,
i i
so this is a singular p-simplex in K, called an affine singular simplex. A
singular chain in which every singular simplex that appears is affine will
be called an affine chain.
Thepointofhomologytheoryistousesingularchainstodetect“holes.”
The intuition is that any chain that closes up on itself (like a closed path)
butisnotequaltothe“boundaryvalue”ofachainofonehigherdimension
must surround a hole in X. To this end, we define a homomorphism from
p-chains to (p−1)-chains that precisely captures the notion of boundary
values.
Foreachi=0,…,p,letF i,p : Δ p−1 →Δ p betheaffinesingularsimplex
F
i,p
=α(e0,…,e(cid:18)
i
,…,e
p
),
where the hat indicates that e is to be omitted. More specifically, F is
i i,p
the affine map that sends
e0 (cid:10)→ e0
… …
e i−1 (cid:10)→ e i−1
e i (cid:10)→ e i+1
… …
e p−1 (cid:10)→ e p
and therefore maps Δ p−1 homeomorphically onto the boundary face of Δ p
opposite the vertex e . We call F the ith face map in dimension p.
i i,p
For any singular simplex σ: Δ → X, define a (p−1)-chain ∂σ called
p
the boundary of σ by
(cid:14)p
∂σ = (−1)iσ◦F .
i,p
i=0
Bythecharacteristicpropertyoffreeabeliangroups,thisextendsuniquely
to a homomorphism ∂: C
p
(X) → C p−1(X), called the boundary operator.

---

294 13. Homology
σ
+
−
+
Δ2
X
FIGURE 13.2. The boundary of a singular 2-simplex.
We sometimes indicate which chain group the boundary operator is acting
on by a subscript, as in ∂
p
: C
p
(X) → C p−1(X). The boundary of any
0-chain is defined to be zero.
A p-chain c is called a cycle if ∂c = 0, and it is called a boundary if
there exists a (p+1)-chain b such that c = ∂b. The set Z (X) of p-cycles
p
is a subgroup of C (X), because it is the kernel of the homomorphism ∂ .
p p
Similarly, the set B (X) of p-boundaries is also a subgroup (the image of
p
∂ p+1).
It might help clarify what is going on to work out some simple exam-
ples. When thinking about these examples, you should note the similarity
between the formula for ∂σ and the induced orientation on the boundary
faces of a simplex, discussed in Chapter 5.
A singular 1-simplex is just a path σ: I → X, and ∂σ is the formal
differenceσ(1)−σ(0).Therefore,a1-cycleisaformalsumofpathswiththe
property that the set of initial points counted with multiplicities is exactly
thesameastheset(cid:15)ofterminalpointswithmultiplicities.Atypicalexample
is a sum of paths k
i=1
σ
i
such that σ
i
(1) = σ i+1(0) and σ
k
(1) = σ1(0).
Apart from notation, this is pretty much the same thing as a product of
paths (in the sense in which we used the term in Chapter 7) such that the
lastpathendswherethefirstonestarts(hencetheterm“cycle”).Theonly
real difference is that chains do not keep track of the order in which the
paths appear.
Theboundaryofasingular2-simplexσ: Δ2 →X isasumofthreepaths
with signs (Figure 13.2). Think of this as a cycle in X that traverses the
boundary values of σ in the counterclockwise direction. (Intuitively, you
can think of a path with a negative sign as representing the same path
going in the opposite direction; although they are not really the same, we
will see below that they differ by a boundary, so they are equivalent from
the point of view of homology.)
The most important feature of the singular boundary map is that “the
boundary of a boundary is zero,” as the next lemma shows.
Lemma 13.1. For any singular chain c, ∂(∂c)=0.

---

Singular Homology Groups 295
Proof. Since each chain group C (X) is generated by singular simplices, it
p
suffices to show this in the case in which c=σ is a singular p-simplex.
First we note that the face maps satisfy the commutation relation
F i,p ◦F j,p−1 =F j,p ◦F i−1,p−1 when i>j, (13.1)
as can be seen immediately by observing that the vertices of Δ p−2 are
mapped according to the following chart:
F j,p−1 F i,p F i−1,p−1 F j,p
e0 (cid:10)→ e0 (cid:10)→ e0 e0 (cid:10)→ e0 (cid:10)→ e0
… … … … … …
e j−1 (cid:10)→ e j−1 (cid:10)→ e j−1 e j−1 (cid:10)→ e j−1 (cid:10)→ e j−1
e j (cid:10)→ e j+1 (cid:10)→ e j+1 e j (cid:10)→ e j (cid:10)→ e j+1
… … … … … …
e i−2 (cid:10)→ e i−1 (cid:10)→ e i−1 e i−2 (cid:10)→ e i−2 (cid:10)→ e i−1
e i−1 (cid:10)→ e i (cid:10)→ e i+1 e i−1 (cid:10)→ e i (cid:10)→ e i+1
… … … … … …
e p−2 (cid:10)→ e p−1 (cid:10)→ e p . e p−2 (cid:10)→ e p−1 (cid:10)→ e p .
In other words, both compositions are equal to the affine simplex
α(e0,…,e(cid:18)
j
,…,e(cid:18)
i
,…,e
p
). Using this, we compute
(cid:14)p−1(cid:14)p
∂(∂σ)= (−1)i+jσ◦F i,p ◦F j,p−1
j=0i=0
(cid:14)
= (−1)i+jσ◦F i,p ◦F j,p−1
0≤j<i≤p
(cid:14)
+ (−1)i+jσ◦F
i,p
◦F j,p−1.
0≤i≤j≤p−1
Making the substitutions i = j(cid:5), j = i(cid:5)−1 into the second sum and using
(13.1), we see that the sums cancel term by term.
Because of the preceding lemma, the group B (X) of p-boundaries is a
p
subgroup of the group Z (X) of p-cycles. The pth singular homology group
p
of X is defined to be the quotient group
H
p
(X)=Z
p
(X)/B
p
(X)=Ker∂
p
/Im∂ p+1.
It is zero if and only if every p-cycle is the boundary of some (p + 1)-
chain, which you should interpret intuitively as meaning that there are no
p-dimensional “holes” in X. The equivalence class of a p-cycle c in H (X)
p
isdenotedby[c],andiscalleditshomology class.Iftwop-cyclesdetermine
the same homology class (i.e., if they differ by a boundary), they are said
to be homologous.

---

296 13. Homology
The significance of the homology groups derives from the fact that they
are topological invariants. The proof is a very easy consequence of the
fact that continuous maps induce homology homomorphisms. We begin by
defining homomorphisms on the chain groups.
Given a continuous map f: X → Y, let f#: C
p
(X) → C
p
(Y) be the
homomorphism defined by setting f#σ =f ◦σ for each singular p-simplex
σ. The key fact is that f# commutes with the boundary operators:
(cid:14)p
f#(∂σ)= (−1)if ◦σ◦F
i,p
=∂(f#σ).
i=0
Becauseofthis,f# mapsZ
p
(X)toZ
p
(Y)andB
p
(X)toB
p
(Y),andthere-
forepassestothequotienttodefineahomomorphismf∗: H
p
(X)→H
p
(Y),
called the homomorphism induced by f.
Proposition 13.2 (Functorial Properties of Homology). LetX,Y,
and Z be topological spaces.
(a) Thehomomorphism(Id
X
)∗: H
p
(X)→H
p
(X)inducedbytheidentity
map of X is the identity of H (X).
p
(b) If f: X → Y and g: Y → Z are continuous maps, then (g◦f)∗ =
g∗ ◦f∗: H
p
(X)→H
p
(Z).
Thus the pth singular homology group defines a covariant functor from the
category of topological spaces to the category of abelian groups.
Proof. It is trivial to check that both properties hold already for f#.
Corollary 13.3 (Topological Invariance of Singular Homology).
If f: X → Y is a homeomorphism, then f∗: H
p
(X) → H
p
(Y) is an
isomorphism.
Exact Sequences and Chain Complexes
It is useful to look at the construction we just did in a somewhat more
algebraic way. A sequence of abelian groups and homomorphisms
···→G p+1 −α−p−+→1 G p −α→p G p−1 →···
is said to be exact if Imα p+1 = Kerα p for all p. For example, a 5-term
exact sequence of the form
0→A−→α B −→β C →0
is called a short exact sequence. (The maps on the ends are the zero homo-
morphisms.)Becausetheimageofthezerohomomorphismis{0},exactness

---

Singular Homology Groups 297
at A means that α is injective, and similarly exactness at C means that β
is surjective. Exactness at B means that Kerβ = α(A), and the first iso-
∼
morphismtheoremthentellsusthat C =B/α(A).Ashortexactsequence
is thus a graphic summary of the first isomorphism theorem.
More generally, a sequence of abelian groups and homomorphisms
···→C p+1 −∂−p−+→1 C p −∂→p C p−1 →···
is called a chain complex if the composition of any two consecutive ho-
momorphisms is the zero map: ∂ p ◦∂ p+1 =0. This is equivalent to the re-
quirementthatIm∂ p+1 ⊂Ker∂ p .(Thehomomorphisms∂ p areoftencalled
“boundary operators” by analogy with the case of singular homology.) We
will denote such a chain complex by C∗, with the boundary maps being
understood from the context. In many applications (such as the singular
chain groups), C is defined only for p ≥ 0, but it is sometimes conve-
p
nient to extend this to all p by defining C to be the trivial group and the
p
associated homomorphisms to be zero for p<0.
The pth homology group of the chain complex C∗ is
H
p
(C∗)=Ker∂
p
/Im∂ p+1.
Clearly,thechaincomplexisexactifandonlyif H
p
(C∗)=0forallp;thus
the homology groups provide a precise quantitative measurement of how
the complex fails to be exact.
NowsupposeC∗ andD∗ arechaincomplexes.Achain mapF: C∗ →D∗
is a collection of homomorphisms F: C →D (we could distinguish them
p p
with subscripts, but there is no need) such that ∂ ◦F =F ◦∂ for all p:
p p
∂
··· (cid:2) C p p (cid:2) C p−1 (cid:2) ···
F F
(cid:5) (cid:5)
··· (cid:2) D p ∂ (cid:2) D p−1 (cid:2) ··· .
p
For example, the homomorphisms f#: C
p
(X)→C
p
(Y) constructed above
from a continuous map f define a chain map from the singular chain com-
plex of X to that of Y. Any chain map takes Ker∂ to Ker∂ and Im∂
to Im∂, and therefore induces a homology homomorphism F∗: H
p
(C∗)→
H
p
(D∗) for each p.
The study of exact sequences, chain complexes, and homology is part of
thesubjectknownashomological algebra.Itbeganasabranchoftopology,
but has acquired a life of its own as a branch of algebra. We will return to
these ideas briefly later in this chapter.

---

298 13. Homology
Elementary Computations
Although the definition of the singular homology groups may seem less
intuitive than that of the fundamental group and the higher homotopy
groups, the homology groups offer a number of advantages. For example,
they are all abelian, which circumvents some of the thorny computational
problemsthatbesetthefundamentalgroup.Also,thereisnoneedtochoose
a base point, so unlike the homotopy groups, homology groups give us
information about all the path components of a space, as the following
lemma shows.
Lemma 13.4. Let X be a space, let {X α } α∈A be the set of path compo-
nents of X, and let ι : X (cid:9)→ X be inclusion. Then for each p ≥ 0 the
α α
maps (ι
α
)∗: H
p
(X
α
)→H
p
(X) induce an isomorphism
#
H (X )→H (X).
p α p
α∈A
Proof. Since the image of any singular simplex must lie entirely in one
path component, it is clear that the chain maps (ι
α
)#: C
p
(X
α
) → C
p
(X)
already induce isomorphisms
#
C (X )→C (X).
p α p
α∈A
The result for homology follows easily from this.
As in the case of the fundamental group, the definition of the homology
groupsdoesnotgiveusmuchinsightintohowtocomputethemingeneral,
because it involves taking quotients of huge groups by huge subgroups.
There are, however, two simple cases that we can compute directly right
now:thezero-dimensionalhomologygroupsofallspacesandallthehomol-
ogy groups of a one-point space. In the rest of this chapter we will develop
some powerful tools for computing the rest of the homology groups.
Proposition 13.5 (Zero-Dimensional Homology). For any topolog-
ical space X, H0(X) is a free abelian group with basis consisting of an
arbitrary point in each path component.
Proof. It suffices to show that H0(X) is the infinite cyclic group generated
bytheclassofanypointwhenX ispathconnected,fortheninthegeneral
caseLemma13.4guaranteesthatH0(X)isthedirectsumofinfinitecyclic
groups, one for each path component.
A singular 0-chain is (cid:15)a formal linear combination of points in X with
integer coefficients: c = m n x . Because the boundary operator is the
i=1 i i
zero map in dimension 0, every 0-chain is a cycle.

---

Singular Homology Groups 299
Assume that X is path connected, and define a map ε: C0(X)→Z by
(cid:20) (cid:21)
(cid:14)m (cid:14)m
ε n x = n .
i i i
i=1 i=1
It is clear that ε is a surjective homomorphism. We will show that
Kerε = B0(X), from which it follows by the first isomorphism theorem
that ε induces an isomorphism H0(X)→Z. Since ε takes any single point
to 1, the result follows.
Ifσ isasingular1-simplex,then∂σ =σ(1)−σ(0),soε(∂σ)=1−1=0.
Therefore, B0(X)⊂Kerε.
To show that Kerε ⊂ B0(X), choose any point x0 ∈ X, and for each
x∈X let α(x) be a path from x0 to x. This is a singular 1-simplex(cid:15)whose
boundary is the 0-chain x−x0. Thus, for an arbitrary 0-chain c=
i
n
i
x
i
we compute
(cid:26) (cid:27)
(cid:14) (cid:14) (cid:14)
∂ n
i
α(x
i
) = n
i
x
i
− n
i
x0 =c−ε(c)x0.
i i i
In particular, if ε(c)=0, then c∈B0(X).
Proposition 13.6 (Homology of a One-Point Space). Let ∗ be a
one-point space. The singular homology groups of ∗ are
(cid:16)
H (∗) ∼ = Z if p=0, (13.2)
p
0 if p>0.
Proof. The case p = 0 follows from the preceding proposition, so we con-
centrateonp>0.Thereisexactlyonesingularsimplexineachdimension,
namely the constant map σ : Δ → ∗, so each chain group C (∗) is the
p p p
infinite cyclic group generated by σ . For p>0, the boundary of σ is the
p p
alternating sum
(cid:16)
(cid:14)p (cid:14)p
0 if p is odd,
∂σ p = (−1)iσ p ◦F i,p = (−1)iσ p−1 =
i=0 i=0 σ p−1 if p is even.
Thus ∂: C
p
(∗)→C p−1(∗) is an isomorphism when p is even and positive,
and the zero map when p is odd:
···−→ ∼= C3(∗)−→0 C2(∗)−→ ∼= C1(∗)−→0 C0(∗)→0.
It follows that for p>0,
(cid:16)
C (∗) if p is odd,
Z (∗)= p
p
0 if p is even;
(cid:16)
C (∗) if p is odd,
B (∗)= p
p
0 if p is even.

---

300 13. Homology
f1
ι1
H
X×I Y
ι0
X
f0
FIGURE 13.3. The setup for Theorem 13.7.
Taking quotients, we find that H (∗)=0.
p
Homotopy Invariance
Just like the fundamental group, the singular homology groups are also
homotopy invariant. The proof, as in the case of the fundamental group,
depends on the fact that homotopic maps induce the same homology ho-
momorphism.
Theorem 13.7. If f0,f1: X →Y are homotopic maps, then for each p≥
0 the induced homomorphisms (f0)∗,(f1)∗: H
p
(X)→H
p
(Y) are equal.
Before proving this theorem, we state its most important corollary.
Corollary 13.8 (Homotopy Invariance of Singular Homology). If
f: X → Y is a homotopy equivalence, then for each p ≥ 0, f∗: H
p
(X) →
H (Y) is an isomorphism.
p
Exercise 13.1. Prove Corollary 13.8.
Proof of Theorem 13.7. Webeginbyconsideringthespecialcaseinwhich
Y =X×I and f
i
=ι
i
, where ι0,ι1: X →X×I are the maps
ι0(x)=(x,0), ι1(x)=(x,1).
(SeeFigure13.3.)Clearly,ι0 (cid:25)ι1.Wewillshowbelowthat(ι0)∗ =(ι1)∗.As
it turns out, this immediately implies the general case as follows. Suppose
f0,f1: X → Y are continuous maps and H: X ×I → Y is a homotopy
from f0 to f1 (Figure 13.3). Then since H ◦ι
i
=f
i
, we have
(f0)∗ =(H ◦ι0)∗ =H∗ ◦(ι0)∗ =H∗ ◦(ι1)∗ =(H ◦ι1)∗ =(f1)∗.

---

Homotopy Invariance 301
To prove (ι0)∗ = (ι1)∗, it would suffice to show that (ι0)#c and (ι1)#c
differ by a boundary for each chain c. In fact, a little experimentation will
probably convince you that this is usually false. But in fact all we need is
that they differ by a boundary when c is a cycle. So we might try to define
a map h: Z
p
(X)→C p+1(X×I) such that
∂h(c)=(ι1)#c−(ι0)#c. (13.3)
It turns out to be hard to define such a thing for cycles only. Instead, we
will define h(c) for all p-chains c, and show that it satisfies a formula that
implies (13.3) when c is a cycle.
Foreachp≥0,wewilldefineahomomorphismh: C
p
(X)→C p+1(X×I)
that satisfies the following identity:
h◦∂+∂◦h=(ι1)# −(ι0)#. (13.4)
From (13.4) it follows immediately that (ι1)#c−(ι0)#c=∂h(c) whenever
∂c=0, and therefore (ι1)∗[c]=(ι0)∗[c].
Theconstructionofhisbasicallya“triangulated”versionoftheobvious
homotopy from ι0 to ι1. Consider the convex set Δ
p
×I ⊂Rp+1 =Rp×R.
Note that Δ ×{0} and Δ ×{1} are Euclidean p-simplices in Rp+1. Let
p p
usdenotetheverticesofΔ ×{0}byE =(e ,0)andthoseofΔ ×{1}by
p i i p
E(cid:5) = (e ,1). For 0 ≤ i ≤ p, let G : Δ → Δ ×I be the following affine
i i i,p p p
singular (p+1)-simplex in Rp+1:
G
i,p
=α(E0,…,E
i
,E
i
(cid:5),…,E
p
(cid:5)).
Then define h: C
p
(X)→C p+1(X×I) by
(cid:14)p
h(σ)= (−1)i(σ×Id)◦G .
i,p
i=0
Note that G takes its values in Δ×I and σ×Id is a map from Δ×I to
i,p
X×I, so this does indeed define a (p+1)-chain in X×I.
Togetanideaofwhatthismeansgeometrically,considerthecasep=2.
The three simplices (cid:22)E0,E
0
(cid:5),E
1
(cid:5),E
2
(cid:5)(cid:23), (cid:22)E0,E1,E
1
(cid:5),E
2
(cid:5)(cid:23), and (cid:22)E0,E1,E2,E
2
(cid:5)(cid:23)
give a triangulation of Δ2 × I (see Figure 13.4). In the special case in
whichσ istheidentitymapofΔ2,h(σ)isasumofaffinesingularsimplices
mapping Δ3 homeomorphically onto each one of these 3-simplices, with
signs chosen to correspond to the natural orientation on each simplex. In
the general case, h(σ) is this singular chain followed by the map σ ×Id,
and thus is a chain in X×I whose image is the product set σ(Δ2)×I.
Now we need to prove that h satisfies (13.4). For this purpose, we will
need some relations between the affine simplices G and the face maps
i,p
F j,p . First, if 1≤j ≤p, note that G j,p and G j−1,p agree on all the vertices

---

302 13. Homology
E(cid:5) E(cid:5)
0 2
G i,2 σ×Id
E(cid:5)
1
E2
E0
Δ3
E1
Δ2 ×I X×I
FIGURE 13.4. The operator h in dimension 2.
of Δ p except e j . Because F j,p+1 skips e j , the compositions G j,p ◦F j,p+1
and G j−1,p ◦F j,p+1 are equal. In fact, it is straightforward to check that
G j,p ◦F j,p+1 =G j−1,p ◦F j,p+1 =α(E0,…,E j−1,E j (cid:5),…,E p (cid:5)). (13.5)
Similarly, by following what each map does to basis elements as we did in
the proof of Lemma 13.1, one can compute that
(cid:16)
(F j,p ×Id)◦G i,p−1 = G G i i + ,p 1 ◦ ,p F ◦ j F +1 j, , p p + + 1 1 i i f f i i ≥ < j j , . (13.6)
Letσ beanarbitrarysingularp-simplexinX.Using (13.6),wecompute
(cid:14)p
h(∂σ)=h (−1)jσ◦F
j,p
j=0
(cid:14)p−1(cid:14)p (cid:12) (cid:13)
= (−1)i+j (σ◦F j,p )×Id ◦G i,p−1
i=0j=0
(cid:14)p−1(cid:14)p
(13.7)
= (−1)i+j(σ×Id)◦(F j,p ×Id)◦G i,p−1
i=0j=0
(cid:14)
= (−1)i+j(σ×Id)◦G i+1,p ◦F j,p+1
0≤j≤i≤p−1
(cid:14)
+ (−1)i+j(σ×Id)◦G
i,p
◦F j+1,p+1.
0≤i<j≤p

---

Homotopy Invariance 303
On the other hand,
(cid:14)p
∂h(σ)=∂ (−1)i(σ×Id)◦G
i,p
i=0
(cid:14)p+1(cid:14)p
= (−1)i+j(σ×Id)◦G
i,p
◦F j,p+1.
j=0i=0
Separating the terms where i < j −1, i = j −1, i = j, and i > j, this
becomes
(cid:14)
∂h(σ)= (−1)i+j(σ×Id)◦G i,p ◦F j,p+1
0≤i<j−1<j≤p+1
(cid:14)
− (σ×Id)◦G
j−1,p
◦F
j,p+1
1≤j≤p+1
(cid:14)
+ (σ×Id)◦G j,p ◦F j,p+1
0≤j≤p
(cid:14)
+ (−1)i+j(σ×Id)◦G
i,p
◦F j,p+1.
0≤j<i≤p
Making the index substitutions j = j(cid:5)+1 in the first sum and i = i(cid:5)+1
in the last, we see that these two sums exactly cancel those in (13.7). By
virtue of (13.5), all the terms in the middle two sums cancel except those
where j =0 and j =p+1. These two terms yield
h(∂σ)+∂h(σ)=−(σ×Id)◦α(E0,…,E
p
)+(σ×Id)◦α(E
0
(cid:5),…,E
p
(cid:5))
=−(ι0)#σ+(ι1)#σ.
This completes the proof.
As an immediate application, we can conclude that contractible spaces
have trivial homology in all dimensions greater than zero. (It is infinite
cyclic in dimension zero by Proposition 13.5.)
Corollary 13.9. Suppose X is a contractible space. Then H (X)=0 for
p
all p>0.
There is an abstract algebraic version of what we just did. Suppose
F,G: C∗ → D∗ are chain maps. A collection of homomorphisms h: C
p
→
D p+1 is called a chain homotopy from F to G if the following identity is
satisfied on each group C :
p
h◦∂+∂◦h=G−F.
If there exists such a map, F and G are said to be chain homotopic.
Exercise 13.2. If F,G: C∗ →D∗ are chain homotopic chain maps, show
that F∗ =G∗: Hp(C∗)→Hp(D∗) for all p.

---

304 13. Homology
f1
H
p q f1
X
p
f0
q
b σ f0
f1 q
p
f0
FIGURE 13.5. Path homotopic paths differ by a boundary.
Homology and the Fundamental Group
In this section we show that there is a simple relationship between the
firsthomologygroupofapathconnectedspaceanditsfundamentalgroup:
The former is just the abelianization of the latter. This will enable us to
compute the first homology groups of all the spaces whose fundamental
groups we know.
We begin by defining a map from the fundamental group to the first
homologygroup.LetX beaspaceandqanypointinX.Aloopf basedatq
isalsoasingular1-simplex.In fact,itisacycle,since∂f =f(1)−f(0)=0.
Therefore, any loop determines a 1-homology class. The following lemma
shows that the resulting class depends only on the path homotopy class of
f.
Lemma 13.10. Suppose f0 and f1 are paths in X, and f0 ∼ f1. Then,
considered as a singular chain, f0 −f1 is a boundary.
Proof. We must show there is a singular 2-chain whose boundary is the
1-chain f0 −f1. Let H: f0 ∼f1, and let b: I×I →Δ2 be the map
b(x,y)=(x−xy,xy), (13.8)
which maps the square onto the triangle by sending each horizontal line
segmentlinearlytoaradiallinesegment(Figure13.5).Thenbisaquotient
map by the closed map lemma, and identifies the left-hand edge of the
square to the origin. Since H respects the identifications made by b, it
passestothequotienttoyieldacontinuousmapσ: Δ2 →X,i.e.,asingular
2-simplex.Fromthedefinitionoftheboundaryoperator,∂σ =c
q
−f1+f0,

---

Homology and the Fundamental Group 305
σ
f
f p
q
q
p
f
FIGURE 13.6. Proof that [f−1]H =−[f]H.
where q = f0(1). Since c
q
is the boundary of the constant 2-simplex that
maps Δ2 to q, it follows that f0 −f1 is a boundary.
In this section, because we will be dealing with various equivalence re-
lations on paths, we adopt the following notation. For any path in X (not
necessarily a loop), we let [f] denote its equivalence class modulo path
π
homotopy.Inparticular,iff isaloopbasedatq,then[f] isitspathclass
π
in π1(X,q). Similarly, if c is any 1-chain we let [c]
H
denote its equivalence
class modulo B1(X), so if c is a cycle (a loop for example), then [c]
H
is an
element of H1(X). Define a map γ: π1(X,q)→H1(X), which we will call
the Poincar´e homomorphism, by
γ([f] )=[f] .
π H
By Lemma 13.10, γ is well-defined.
Theorem 13.11. Let X be a path connected space and q ∈ X. Then
γ: π1(X,q) → H1(X) is a surjective homomorphism whose kernel is the
commutator subgroup of π1(X,q). Consequently, H1(X) is isomorphic to
the abelianization of π1(X,q).
Proof. We begin by showing that [f−1] =−[f] for any path f in X. To
H H
see this, define a singular 2-simplex σ: Δ2 →X by σ(x,y)=f(x) (Figure
13.6). Then ∂σ =f−1−c +f, where q =f(0). Since c is a boundary, it
q q
follows that the 1-chains f−1 and −f differ by a boundary.
Next we show that γ is a homomorphism. Somewhat more generally, we
·
will show that [f g] = [f] + [g] for any two paths f,g such that
H H H
f(1)=g(0). When applied to loops f and g based at q, this implies that γ
is a homomorphism.
Given such paths f and g, define a singular 2-simplex σ: Δ2 →X by
(cid:16)
f(y−x+1) if y ≤x,
σ(x,y)=
g(y−x) if y ≥x.

---

306 13. Homology
σ
f
·
f g
g
g
f
FIGURE 13.7. Proof that γ is a homomorphism.
(See Figure 13.7.) This is constant on each line segment y−x=constant,
andiscontinuousbythegluinglemma.Itiseasytocheckthatitsboundary
is the 1-chain (f · g)−g+f−1, from which it follows that
[f · g] =[g] −[f−1] =[g] +[f] .
H H H H H
Thus γ is a homomorphism.
Nextweneedtoshowthatγ issurjective.Foreachpointx∈X,letα(x)
beaspecificpathfromq tox,withα(q)chosentobetheconstantpathc .
q
Since each path α(x) is in particular a 1-chain, the map x(cid:10)→α(x) extends
uniquely to a group homomorphism α: C0(X) → C1(X). For any path σ
in X, define a loop σ(cid:7) based at q by
σ(cid:7) =α(σ(0)) · σ · α(σ(1))−1.
Observe that
γ([σ(cid:7)] )=[α(σ(0)) · σ · α(σ(1))−1]
π H
=[α(σ(0))] +[σ] −[α(σ(1))] (13.9)
H H H
=[σ] −[α(∂σ)] .
H H
(cid:15)
Now suppose c= m n σ is an arbitrary 1-chain. Let f be the loop
i=1 i i
· ·
f =(σ(cid:7) 1)n1 ··· (σ(cid:7)
m
)nm.
From (13.9) and the fact that γ is a homomorphism it follows that
(cid:14)m (cid:12) (cid:13)
γ([f] )= n [σ ] −[α(∂σ )]
π i i H i H
i=1
=[c] −[α(∂c)] .
H H

---

Homology and the Fundamental Group 307
α(v2) v2 X
e2 σ
σ(1)
q
α(v0) σ(0)
v0
σ(2)
e0 e1
v1
α(v1)
FIGURE 13.8. Proof that Kerγ is the commutator subgroup.
In particular, if c is a cycle, then γ([f] ) = [c] , which shows that γ is
π H
surjective.
Because H1(X) is an abelian group, Kerγ clearly contains the commu-
tator subgroup [π1(X,q),π1(X,q)]. All that remains is to show that the
commutator subgroup is the entire kernel.
Let Π denote the abelianized fundamental group of X, and for any loop
f based at q let [f]Π denote the equivalence class of [f]
π
in Π. Because
the product in Π is induced by path multiplication, we will indicate it
with a dot and write it multiplicatively even though Π is abelian. For any
singular 1-simplex σ, let β(σ) = [σ(cid:7)]Π ∈ Π. Because Π is abelian, this
extends uniquely to a homomorphism β: C1(X) → Π. We will show that
β takes all 1-boundaries to the identity element of Π.
Let σ be an arbitrary singular 2-simplex. Write v = σ(e ) and σ(i) =
i i
σ◦F i,2,sothat∂σ =σ(0)−σ(1)+σ(2) (seeFigure13.8).Notethattheloop
σ(0)· (σ(1))−1· σ(2) is path homotopic to the constant loop c . (This can
v1
beseeneitherbyidentifyingΔ2 withthecloseddiskviaahomeomorphism
andnotingthatσ
providesanextensionofthecirclerepresentativeofσ(0)·
(σ(1))−1· σ(2) to the disk; or by applying Lemma 7.12 to the composition
σ◦b, where b: I×I →Δ2 is given by (13.8).) We compute
(cid:12) (cid:13)
β(∂σ)=[σ(cid:7)(0)]Π · [σ(cid:7)(1)]Π −1· [σ(cid:7)(2)]Π
=[σ(cid:7)(0)· (σ(cid:7)(1))−1· σ(cid:7)(2)]Π
=[α(v1) · σ(0)· α(v2)−1· α(v2) · (σ(1))−1· α(v0)−1
· α(v0) · σ(2)· α(v1)−1]Π
=[α(v1) · σ(0)· (σ(1))−1· σ(2)· α(v1)−1]Π
=[α(v1) · c
v1
· α(v1)−1]Π
=[c
q
]Π,

---

308 13. Homology
which proves that B1(X)⊂Kerβ.
Nowsuppose f isaloopsuchthat[f] ∈Kerγ.Thismeansthat[f] =
π H
0, or equivalently that the singular 1-chain f is a boundary. On the one
(cid:7)
hand, because f is a loop based at q, β(f) = [f]Π = [f]Π. On the other
hand, since β takes boundaries to the identity element of Π, it follows that
[f]Π =1, or equivalently that [f]
π
is in the commutator subgroup.
Corollary 13.12. The following spaces have the indicated first homology
groups.
H1(S1) ∼ =Z;
H1(Sn)=0 if n≥2;
H1(
(cid:31)
T2#· ·
!
·#T
"
2) ∼ =Z2n;
n
H1(
(cid:31)
P2#· ·
!
·#P
"
2) ∼ =Zn−1×Z/(cid:22)2(cid:23).
n
The Poincar´e homomorphism γ: π1(X,q) → H1(X) can be generalized
easily to a homomorphism from π (X,q) to H (X) for any k, called the
k k
Hurewicz homomorphism. The relationship between the higher homotopy
and homology groups is not so simple however, except in one important
special case: The Hurewicz theorem, proved by Witold Hurewicz in 1934,
says that if X is path connected and π (X,q) is trivial for 1≤j <k, then
j
H (X) is trivial for the same values of j and the Hurewicz homomorphism
j
is an isomorphism between π (X,q) and H (X). For a proof, see [Spa89]
k k
or [Whi78].
The Mayer–Vietoris Theorem
Our main tool for computing higher-dimensional homology groups will be
a result analogous to the Seifert–Van Kampen theorem, in that it gives a
recipe for computing the homology groups of a space that is the union of
two open sets in terms of the homology of the two open sets and that of
their intersection.
Statement of the Theorem
The setup for the theorem is similar to that of the Seifert–Van Kampen
theorem: We are given a space X and two open subsets U,V ⊂ X whose
union is X. (In this case, there is no requirement that any of the spaces be

---

The Mayer–Vietoris Theorem 309
path connected.) There are four inclusion maps
U
(cid:3)(cid:4) (cid:6)
i (cid:3) (cid:6)k
(cid:3) (cid:6)(cid:7)
U ∩V X,
(cid:6) (cid:3)(cid:4)
j (cid:6) (cid:3)l
(cid:6)(cid:7) (cid:3)
V
all of which induce homology homomorphisms.
Theorem 13.13 (Mayer–Vietoris). Let X be a topological space, and
let U,V be open subsets of X whose union is X. Then for each p there
is a homomorphism ∂∗: H
p
(X) → H p−1(U ∩V) such that the following
sequence is exact:
···−∂→∗ H (U ∩V)−i−∗⊕ −j→∗ H (U)⊕H (V)−k−∗−−−l→∗ H (X)
p p p p
−∂→∗ H p−1(U ∩V)−i−∗⊕ −j→∗ ··· . (13.10)
The sequence (13.10) is called the Mayer–Vietoris sequence of the triple
(X,U,V), and ∂∗ is called the connecting homomorphism. The other maps
are the obvious ones: (i∗ ⊕j∗)[c] = (i∗[c],j∗[c]) and (k∗ −l∗)([c],[c(cid:5)]) =
k∗[c]−l∗[c(cid:5)].
Before proving the theorem, let us apply it to an example to show how
it can be used to compute homology groups.
Proposition 13.14 (Homology Groups of Spheres). For n ≥ 1, Sn
has the following singular homology groups:
⎧
⎪⎪⎪⎨ Z if p=0,
H (Sn) ∼ = 0 if 0<p<n,
p ⎪⎪⎪⎩ Z if p=n,
0 if p>n.
Proof. WeusetheMayer–Vietorissequenceasfollows.LetN andS denote
the north and south poles, and let U = Sn (cid:3){N}, V = Sn (cid:3){S} as in
the proof that Sn is simply connected (Theorem 8.7). Part of the Mayer–
Vietoris sequence reads
H
p
(U)⊕H
p
(V)→H
p
(Sn)−∂→∗ H p−1(U ∩V)→H p−1(U)⊕H p−1(V).
Because U and V are contractible, when p>1 this sequence reduces to
0→H
p
(Sn)−∂→∗ H p−1(U ∩V)→0,

---

310 13. Homology
from which it follows that ∂∗ is an isomorphism. Thus, since U ∩ V is
homotopy equivalent to Sn−1,
H
p
(Sn) ∼ =H p−1(U ∩V) ∼ =H p−1(Sn−1) for p>1, n≥1. (13.11)
We will prove the proposition by induction on n. In the case n = 1,
H0(S1) ∼ =H1(S1) ∼ =Z by Proposition 13.5 and Corollary 13.12. For p>1,
(13.11) shows that H
p
(S1) ∼ = H p−1(S0). Since each component of S0 is
a one-point space, H p−1(S0) is the trivial group by Proposition 13.6 and
Lemma 13.4.
Now let n>1, and suppose the result is true for Sn−1. The cases p=0
and p=1 are again taken care of by Proposition 13.5 and Corollary 13.12.
For p>1, (13.11) and the inductive hypothesis give
⎧
⎪⎨0 if p<n,
H
p
(Sn) ∼ =H p−1(Sn−1) ∼ =
⎪⎩
Z if p=n,
0 if p>n.
Proof of the Theorem
To prove the Mayer–Vietoris theorem, we need to introduce a few more
basic concepts from homological algebra.
Suppose C∗, D∗, and E∗ are chain complexes. A sequence of chain maps
···→C∗ −→F D∗ −→G E∗ →···
is said to be exact if each of the sequences
···→C −→F D −→G E →···
p p p
is exact.
The following lemma is a standard result in homological algebra. The
proof, which is easier to do than it is to read, uses a technique commonly
called “diagram chasing.” The best way to understand it is probably to
read the first paragraph or two to get an idea of how the arguments go,
and then sit down with pencil and paper and carry out the rest yourself.
Lemma 13.15 (The Zigzag Lemma). Let
0→C∗ −→F D∗ −→G E∗ →0
be a short exact sequence of chain maps. Then for each p there is a con-
necting homomorphism ∂∗: H
p
(E∗) → H p−1(C∗) such that the following
sequence is exact:
···−∂→∗ H
p
(C∗)−F→∗ H
p
(D∗)−G−→∗ H
p
(E∗)−∂→∗ H p−1(C∗)−F→∗ ··· . (13.12)

---

The Mayer–Vietoris Theorem 311
The sequence (13.12) is called the long exact homology sequence associ-
ated with the given short exact sequence of chain maps.
Proof. Consider the diagram
(cid:2) F (cid:2) G(cid:2) (cid:2)
0 C p+1 D p+1 E p+1 0
∂ ∂ ∂
(cid:5) (cid:5) (cid:5)
(cid:2) F (cid:2) G (cid:2) (cid:2)
0 C D E 0
p p p
∂ ∂ ∂
(cid:5) (cid:5) (cid:5)
(cid:2) F (cid:2) G(cid:2) (cid:2)
0 C p−1 D p−1 E p−1 0
∂ ∂ ∂
(cid:5) (cid:5) (cid:5)
(cid:2) F (cid:2) G(cid:2) (cid:2)
0 C p−2 D p−2 E p−2 0.
The hypothesis is that this diagram commutes and the horizontal rows are
exact.
We will use brackets to denote the homology class of a cycle in any of
these groups, so for example if d ∈ D satisfies ∂d = 0, then [d ] ∈
p p p p
H
p
(D∗). To define the connecting homomorphism ∂∗, let [e
p
]∈H
p
(E∗) be
arbitrary. This means that e ∈E and ∂e =0. Surjectivity of G: D →
p p p p
E means that there is an element d ∈ D such that Gd = e , and
p p p p p
then commutativity of the diagram means that G∂d = ∂Gd = ∂e = 0,
p p p
so ∂d p ∈ KerG. By exactness at D p−1 there is an element c p−1 ∈ C p−1
such that Fc p−1 = ∂d p . Now, F∂c p−1 = ∂Fc p−1 = ∂∂d p = 0, and since
F is injective, ∂c p−1 = 0. Therefore, c p−1 represents a homology class in
H p−1(C∗).
We wish to set ∂∗[e
p
] = [c p−1]. To do so, we have to make sure the
homology class of c p−1 does not depend on any of the choices we made
along the way. Another set of choices will be of the form e(cid:5) ∈ E such
p p
that e p −e(cid:5) p = ∂e p+1, d(cid:5) p ∈ D p such that Gd(cid:5) p = e(cid:5) p , and c(cid:5) p−1 ∈ C p−1
such that Fc(cid:5) p−1 =∂d(cid:5) p . Because G is surjective, there exists d p+1 ∈D p+1
such that Gd p+1 = e p+1. Then G∂d p+1 = ∂Gd p+1 = ∂e p+1 = e p −e(cid:5) p , so
G(d p −d(cid:5) p ) = e p −e(cid:5) p = G∂d p+1. Since d p −d(cid:5) p −∂d p+1 ∈ KerG, there
exists c
p
∈ C
p
such that Fc
p
= d
p
−d(cid:5)
p
−∂d p+1. Now F∂c
p
= ∂Fc
p
=
∂(d p −d(cid:5) p −∂d p+1) = ∂d p −∂d(cid:5) p = Fc p−1 −Fc(cid:5) p−1 . Since F is injective,
this implies ∂c p = c p−1 −c(cid:5) p−1 , or [c p−1] = [c(cid:5) p−1 ]. To summarize, we have
defined ∂∗[e
p
]=[c p−1], provided that there exists d
p
∈D
p
such that
Gd p =e p ; Fc p−1 =∂d p .
To prove that ∂∗ is a homomorphism, just note that if ∂∗[e
p
] = [c p−1]
and ∂∗[e(cid:5)
p
]=[c(cid:5)
p−1
], there exist d
p
,d(cid:5)
p
∈D
p
such that Gd
p
=e
p
, Gd(cid:5)
p
=e(cid:5)
p
,
Fc p−1 =∂d p ,Fc(cid:5) p−1 =∂d(cid:5) p .ItfollowsimmediatelythatG(d p +d(cid:5) p )=e p +e(cid:5) p

---

312 13. Homology
and F(c p−1 +c(cid:5) p−1 ) = ∂(d p +d(cid:5) p ), and so ∂∗[e p +e(cid:5) p ] = [c p−1 +c(cid:5) p−1 ] =
∂∗[e
p
]+∂∗[e(cid:5)
p
].
Now we have to prove exactness of (13.12). Let us start at H
p
(C∗).
Suppose [c
p
] = ∂∗[e p+1]. Then looking back at the definition of ∂∗, there
is some d p+1 such that Fc p = ∂d p+1, so F∗[c p ] = [Fc p ] = [∂d p+1] = 0;
thus Im∂∗ ⊂ KerF∗. Conversely, if F∗[c
p
] = [Fc
p
] = 0, there is some
d p+1 ∈ D p+1 such that Fc p = ∂d p+1, and then ∂Gd p+1 = G∂d p+1 =
GFc p = 0. In particular, this means e p+1 = Gd p+1 represents a homology
class in H p+1(E∗), and threading through the definition of ∂∗ we find that
∂∗[e p+1]=[c
p
]. Thus KerF∗ ⊂Im∂∗.
NextweproveexactnessatH
p
(D∗).FromGF =0itfollowsimmediately
that G∗F∗ = 0, so ImF∗ ⊂ KerG∗. If G∗[d
p
] = [Gd
p
] = 0, there exists
e p+1 ∈ E p+1 such that ∂e p+1 = Gd p . By surjectivity of G, there is some
d p+1 ∈ D p+1 such that Gd p+1 = e p+1, and then G∂d p+1 = ∂Gd p+1 =
∂e p+1 = Gd p . Thus d p −∂d p+1 ∈ KerG = ImF, so there is c p ∈ C p with
Fc
p
=d
p
−∂d p+1. Moreover, F∂c
p
=∂Fc
p
=∂(d
p
−∂d p+1)=∂d
p
=0, so
∂c
p
=0byinjectivityofF.Thusc
p
representsahomologyclassinH
p
(C∗),
andF∗[c
p
]=[Fc
p
]=[d
p
−∂d p+1]=[d
p
].ThisprovesthatKerG∗ ⊂ImF∗.
Finally,weproveexactnessatH
p
(E∗).Suppose[e
p
]∈ImG∗.Thismeans
that [e
p
] = G∗[d
p
] for some d
p
∈ D
p
with ∂d
p
= 0, so e
p
= Gd
p
+∂e p+1.
Replacinge
p
withe
p
−∂e p+1,wemayassumeGd
p
=e
p
.Thenbydefinition
∂∗[e p ] = [c p−1], where c p−1 ∈ C p−1 is chosen so that Fc p−1 = ∂d p . But
in this case ∂d p = 0, so we may take c p−1 = 0 and therefore ∂∗[e p ] = 0.
Conversely, suppose ∂∗[e
p
]=0. This means that there exists d
p
∈D
p
such
that Gd p = e p and c p−1 ∈ C p−1 such that Fc p−1 = ∂d p , and c p−1 is a
boundary. Writing c p−1 =∂c p , we find that ∂Fc p =F∂c p =Fc p−1 =∂d p .
Thus d
p
−Fc
p
represents a homology class, and G∗[d
p
−Fc
p
] = [Gd
p
−
GFc
p
] = [e
p
− 0] = [e
p
]. Therefore, Ker∂∗ ⊂ ImG∗, and the proof is
complete.
The connecting homomorphism in the long exact homology sequence
satisfies an important naturality property, which we will use later in this
chapter.
Proposition 13.16 (Naturality of Connecting Homomorphisms).
Suppose
(cid:2) F (cid:2) G (cid:2) (cid:2)
0 C∗ D∗ E∗ 0
κ δ ε
(cid:5) (cid:5) (cid:5)
0 (cid:2) C(cid:5) F(cid:5) (cid:2) D(cid:5) G(cid:5) (cid:2) E(cid:5) (cid:2) 0 (13.13)
∗ ∗ ∗

---

The Mayer–Vietoris Theorem 313
is a commutative diagram of chain maps in which the horizontal rows are
exact. Then the following diagram commutes for each p:
∂(cid:2)∗
H
p
(E∗) H p−1(C∗)
ε∗ κ∗
(cid:5) (cid:5)
H
p
(E
∗
(cid:5))
∂
(cid:2)
∗
H p−1(C
∗
(cid:5)).
Proof. Let [e
p
] ∈ H
p
(E∗) be arbitrary. Then ∂∗[e
p
] = [c p−1], where
Fc p−1 = ∂d p for some d p such that Gd p = e p . Then by commutativity
of (13.13),
F(cid:5)(κc p−1)=δFc p−1 =δ∂d p =∂(δd p );
G(cid:5)(δd )=εGd =εe .
p p p
By definition, this means that
∂∗ε∗[e
p
]=∂∗[εe
p
]=[κc p−1]=κ∗[c p−1]=κ∗∂∗[e
p
],
which was to be proved.
Whileweareonthesubject,hereisanotheralgebraicresultwhoseproof
is a routine diagram chase.
Lemma 13.17 (The Five Lemma). Suppose the horizontal rows are
exact in the following commutative diagram of abelian groups and homo-
morphisms:
α1(cid:2) α2(cid:2) α3(cid:2) α4(cid:2)
A1 A2 A3 A4 A5
f1 f2 f3 f4 f5
(cid:5) (cid:5) (cid:5) (cid:5) (cid:5)
β1(cid:2) β2(cid:2) β3(cid:2) β4(cid:2)
B1 B2 B3 B4 B5.
If f1, f2, f4, and f5 are isomorphisms, then f3 is also.
Proof. Wewillprovethatf3 issurjective,andleavetheproofofinjectivity
to you. Suppose b3 ∈ B3 is arbitrary. By surjectivity of f4, there exists
a4 ∈A4 suchthatf4a4 =β3b3.Bycommutativityandexactness,f5α4a4 =
β4f4a4 =β4β3b3 =0.Sincef5isinjective,thismeansthatα4a4 =0,andby
exactnessagainthereexistsa3 ∈A3 suchthata4 =α3a3.Substituting,we
obtainβ3b3 =f4a4 =f4α3a3 =β3f3a3,whichimpliesb3 −f3a3 ∈Kerβ3 =
Imβ2. Thus there exists b2 ∈ B2 such that β2b2 = b3 − f3a3, and by
surjectivityoff2thereexistsa2 ∈A2suchthatb2 =f2a2.Summarizing,we
haveb3 −f3a3 =β2b2 =β2f2a2 =f3α2a2,whichshowsthatb3 ∈Imf3.
Exercise 13.3. Finish the proof of the five lemma by showing that f3 is
injective.

---

314 13. Homology
Proof of the Mayer–Vietoris theorem. LetX,U,andV beasinthestate-
meant of the theorem. Consider the three chain complexes C∗(U ∩ V),
C∗(U)⊕C∗(V),andC∗(X).(Theboundaryoperatorinthesecondcomplex
is∂(c,c(cid:5))=(∂c,∂c(cid:5)).)Weareinterestedinthefollowingsequenceofmaps:
0→C (U ∩V)−i−#− ⊕ −j→# C (U)⊕C (V)−k−#− − −l→# C (X).
p p p p
Because the chain maps i#,j#,k#,l# are all induced by inclusion, their
action is simply to consider a chain in one space as a chain in a bigger
space.Itiseasytocheckthati# ⊕j# andk# −l# arechainmapsandthat
this sequence is exact, as far as it goes. For example, if c and c(cid:5) are chains
in U and V, respectively, such that k#c−l#c(cid:5) = 0, this means that they
are equal when thought of as chains in X. For this to be the case, the two
chains must be identical, and the image of each singular simplex in each
chain must actually lie in U ∩V. Thus c is actually a chain in U ∩V, and
(c,c(cid:5))=(i# ⊕j#)(c). The rest of the conditions for exactness are similar.
Unfortunately, however, k# −l# is not surjective. It is not hard to see
why: The image of this map is the set of all p-chains in X that can be
written as a sum of a chain in U plus a chain in V. Any singular p-simplex
whose image is not contained in either U or V therefore defines a chain
that is not in the image. Thus we cannot apply the zigzag lemma directly
to this sequence.
Instead, we use the following subterfuge: Let U denote the open cover
of X consisting of the sets U and V, and for each p let CU(X) denote the
p
subgroup of C (X) generated by singular simplices whose images lie either
p
entirely in U or entirely in V. The boundary operator carries CU(X) into
p
CU (X), so we get a new chain complex CU(X). Clearly, the following
p−1 ∗
sequence is exact:
0→C∗(U ∩V)−i−#− ⊕ −j→# C∗(U)⊕C∗(V)−k−#− − −l→# C
∗
U(X)→0.
Thezigzaglemmathenyieldsthefollowinglongexacthomologysequence:
···−∂→∗ H (U ∩V)−i−∗⊕ −j→∗ H (U)⊕H (V)−k−∗−−−l→∗ HU(X)
p p p p
−∂→∗ H p−1(U ∩V)−i−∗⊕ −j→∗ ··· , (13.14)
where HU(X) is the pth homology group of the complex CU(X). This is
p ∗
almostwhatwearelookingfor.ThefinalstepistoinvokeProposition13.18
below, which shows that inclusion C
∗
U(X) (cid:9)→ C∗(X) induces a homology
isomorphism HU(X) ∼ = H (X). Making this substitution into (13.14), we
p p
obtain the Mayer–Vietoris sequence.
Themissingstepintheaboveproofisthefactthatthesingularhomology
of X can be detected by looking only at singular simplices that lie either
inU orinV.Moregenerally,supposeUisanyopencoverofX.Asingular

---

The Mayer–Vietoris Theorem 315
chaincissaidtobeU-smallifeverysingularsimplexthatappearsinchas
image lying entirely in one of the open sets of U. Let CU(X) denote the
p
subgroupofC (X)consistingofU-smallchains,andletHU(X)denotethe
p p
homology of the complex CU(X).
∗
Proposition 13.18. If U is any open cover of X, the inclusion map
C
∗
U(X) → C∗(X) induces a homology isomorphism H
p
U(X) ∼ = H
p
(X) for
all p.
The idea of the proof is simple, although the technical details are some-
what involved. If σ: Δ → X is any singular p-simplex, the plan is to
p
show that there is a homologous p-chain obtained by subdividing Δ and
p
restricting σ to each of the p-simplices of the subdivision. If we subdivide
sufficientlyfinely,wecanensurethateachoftheresultingsimpliceswillbe
U-small. The tricky part is to do this in a systematic way that allows us to
keep track of the boundary operators. Before the formal proof, let us lay
some groundwork.
Recall the barycentric subdivision of a Euclidean simplicial complex in-
troduced in Chapter 5. It is obtained by replacing each simplex with its
barycentertogetherwithconesonappropriatelower-dimensionalsimplices
fromthebarycenter.Todefineasubdivisionoperatorinsingularhomology,
we begin by extending the cone construction to affine singular simplices.
If σ = α(v0,…,v
p
) is an affine singular p-simplex in some convex set
K ⊂RmandvisanypointinK,wedefineanaffinesingular(p+1)-simplex
v∗σ called the cone on σ from v by
v∗σ =v∗α(v0,…,v
p
)=α(v,v0,…,v
p
).
In other words, v∗σ: Δ p+1 → K is the unique affine simplex that sends
e0 to v and whose 0th face ma(cid:15)p is equal to(cid:15)σ. We extend this operator to
affine chains by linearity: v∗( n σ ) = n (v∗σ ). (It is not defined
i i i i i i
for arbitrary singular chains.)
Lemma 13.19. If c is an affine chain, then
∂(v∗c)=c−v∗∂c. (13.15)
Proof. For an affine simplex σ =α(v0,…,v
p
), this is just a computation:
∂(v∗σ)=∂α(v,v0,…,v
p
)
(cid:14)p+1
= (−1)iα(v,v0,…,v
p
)◦F
i,p
i=0
(cid:14)p
=α(v0,…,v
p
)+ (−1)i+1α(v,v0,…,v(cid:18)
i
,…,v
p
)
i=0
=σ−v∗∂σ.
The general case follows by linearity.

---

316 13. Homology
σ
si1
e0 b1 e1
si2 σ
b2
FIGURE 13.9. Singular subdivisions in dimensions 1 and 2.
Now we define an operator s taking p-chains to p-chains, called the sin-
gular subdivision operator. We define it first for affine chains in Rn, by
induction on p. For p=0, simply set s=Id. For p>0, set
sc=b ∗s∂c,
p
where b is the barycenter of Δ . For example, if i : Δ → Δ is the
p p p p p
identity map, thought of as an affine singular p-simplex in Δ , si is a
p p
sum of affine simplices mapping homeomorphically onto the simplices of
the barycentric subdivision of Δ .
p
For a singular p-simplex σ in any space X, note that σ = σ#i
p
, where
σ#: C
p
(Δ
p
)→C
p
(X) is the chain map obtained from the continuous map
σ: Δ
p
→ X. We define sσ = σ#(si
p
), and extend by linearity to all of
C (X). Low-dimensional examples are pictured in Figure 13.9. We can
p
iterate s to obtain operators s2 =s◦s and more generally sk =s◦sk−1.
Lemma 13.20. The singular subdivision operator has the following prop-
erties.
(a) s◦f# =f# ◦s for any continuous map f.
(b) ∂◦s=s◦∂.
(c) Given an open cover U of X and any c∈C (X), there exists m such
p
that smc∈CU(X).
p
Proof. The first identity follows immediately from the definition of s:
s(f#σ)=s(f ◦σ)=(f ◦σ)#(si
p
)=f#σ#(si
p
)=f#(sσ).

---

The Mayer–Vietoris Theorem 317
The second is proved by induction on p. For p = 0 it is trivial, and for
p>0 we use part (a), (13.15), and the inductive hypothesis to compute
∂sσ =∂σ#(b
p
∗s∂i
p
)
=σ#∂(b
p
∗s∂i
p
)
=σ#(s∂i
p
−b
p
∗∂s∂i
p
)
=sσ#∂i
p
−σ#b
p
∗(s∂∂i
p
)
=s∂σ#i
p
−0
=s∂σ.
Toprove(c),definethemeshofanaffinechaincinRntobethemaximum
of the diameters of the images of the affine simplices that appear in c. By
Lemma 5.18, by choosing m large enough, we can make the mesh of smi
p
arbitrarily small.
If σ is any singular simplex in X, by the Lebesgue number lemma there
exists δ > 0 such that σ maps any subset of Δ of diameter less than δ
p
into one of the sets of U. In particular, if c is an affine chain in Δ whose
p
meshislessthanδ,thenσ#c∈C
p
U(X).Chooseδ tobetheminimumofthe
Lebesgue numbers for all the singular simplices appearing in c, and choose
m large enough that smi
p
has mesh less than δ. Then smσ = σ#(smi
p
) ∈
CU(X) as desired.
p
With the machinery we have set up, it is now an easy matter to prove
Proposition 13.18.
Proof of Proposition 13.18. The crux of the proof is the construction of a
chainhomotopybetweensandtheidentitymapofC (X).Recallthatthis
p
is a homomorphism h: C
p
(X)→C p+1(X) satisfying
∂◦h+h◦∂ =Id−s. (13.16)
We define h by induction on p. For p = 0, h is the zero homomorphism.
For p>0, if σ is a singular p-simplex in any space, define
hσ =σ#b
p
∗(i
p
−si
p
−h∂i
p
).
As with s, it is a trivial consequence of the definition that h◦f# =f# ◦h
foranycontinuousmapf.Observealsothatifσ isaU-smallsimplex,then
hσ is a U-small chain, so h also maps CU(X) to CU (X).
p p+1
The chain homotopy identity (13.16) is proved by induction on p. For
p = 0 it is immediate because h = ∂ = 0 and s = Id. Suppose it holds for
(p−1)-chains in all spaces. If σ is a singular p-simplex, then
∂hσ =∂σ#b
p
∗(i
p
−si
p
−h∂i
p
)
=σ#∂b
p
∗(i
p
−si
p
−h∂i
p
)
=σ#(i
p
−si
p
−h∂i
p
)−σ#b
p
∗(∂i
p
−∂si
p
−∂h∂i
p
).

---

318 13. Homology
Theexpressioninsidethesecondsetofparenthesesisequalto∂i −s∂i −
p p
∂h∂i −h∂∂i , which is zero by the inductive hypothesis because ∂i is a
p p p
(p−1)-chain. Therefore,
∂hσ =σ#i
p
−sσ#i
p
−h∂σ#i
p
=σ−sσ−h∂σ,
which was to be proved.
Now if c is any singular cycle in X, (13.16) shows that
c−sc=∂hc+h∂c=∂hc,
so sc differs from c by a boundary. If c ∈ CU(X), the difference is the
p
boundaryofachainin CU (X).Byinductionthesameistruefor smc for
p+1
any positive integer m. Moreover, smc is a cycle because s commutes with
∂.
The inclusion map ι: CU(X) (cid:9)→ C (X) is clearly a chain map, and so
p p
induces a homology homomorphism ι∗: H
p
U(X) → H
p
(X). It is surjective
because for any [c] ∈ H (X) we can choose m large enough that smc ∈
p
CU(X), and the argument above shows that c is homologous to smc. To
p
prove injectivity, suppose [c] ∈ H
p
U(X) satisfies ι∗[c] = 0. This means that
there is a (p+1)-chain b ∈ C p+1(X) such that c = ∂b. Choose m large
enough that smb ∈ CU (X). Then ∂smb = sm∂b = smc, which differs
p+1
from c by the boundary of a chain in CU (X). Thus c represents the zero
p+1
element of HU(X).
p
Applications
In this section we give a sampling of the numerous significant applications
ofhomologytheorytothestudyofmanifolds.Theseapplicationsarebased
on the fact that the homology groups give us a simple way to distinguish
topologically between spheres of different dimensions and between homo-
topy classes of maps of spheres, something that the fundamental group
could not do. Several more such applications are outlined in the problems.
Invariance of Dimension
The dimension of a manifold is part of its definition: An n-dimensional
manifold is one that admits local homeomorphisms to open subsets of Rn.
It seems intuitively obvious that dimension ought to be a topological in-
variant: A manifold of dimension n ought not to be homeomorphic to one
ofsomeotherdimension.Thisistrue,buttheproofisdecidedlynontrivial.
Aproofforn=1wasoutlinedinProblem4-1usingthefactthatRn(cid:3){0}
is connected when n > 1. Similarly, Problem 8-5 suggested a proof for
n = 2 using the fact that Rn(cid:3){0} is simply connected when n > 2. But

---

Applications 319
U
x
S (x)
ε
FIGURE 13.10. Proof of Lemma 13.21.
neither connectedness nor simple connectedness can distinguish Rn(cid:3){0}
from Rm(cid:3){0} when both m and n are larger than 2. Homology can.
Lemma 13.21. Let U be an open subset of Rn, n ≥ 2. If x is any point
in U, then Hn−1(U (cid:3){x})(cid:14)=0.
Proof. Choose ε>0 small enough that the sphere S (x) of radius ε about
ε
x is contained in U (Figure 13.10). Consider the following commutative
diagram of inclusion maps:
S (x)
ε
(cid:10)
(cid:10)
i (cid:10)k
(cid:5) (cid:10)(cid:11)
U (cid:3){x} (cid:2)Rn(cid:3){x}.
j
These induce homology homomorphisms
H n−1(S
ε
(x))
(cid:10)
(cid:10)
(cid:10)
i∗ (cid:10)k∗
(cid:10)
(cid:10)
(cid:5) (cid:10)(cid:11)
H n−1(U (cid:3){x})
j
(cid:2)
∗
H n−1(Rn(cid:3){x}).
Because k is a homotopy equivalence, k∗ is an isomorphism. This implies
that i∗ is injective (and j∗ is surjective). Since H n−1(S
ε
(x)) is not trivial,
neither is H n−1(U (cid:3){x}).
Theorem 13.22 (Invariance of Dimension). If m (cid:14)= n, a topological
space cannot be both an n-manifold and an m-manifold.
Proof. Thezero-dimensionalcaseiseasytodisposeof,becausea0-manifold
is a discrete space, and points in a positive-dimensional manifold are not

---

320 13. Homology
open sets. Suppose M is both an m-manifold and an n-manifold, and as-
sume that n > m ≥ 1. Any x ∈ M has a neighborhood U ⊂ M that
is homeomorphic to Rn. Because an open subset of a manifold is again a
manifold, U is also an m-manifold, so x has a neighborhood V ⊂ U that
is homeomorphic to Rm. On the one hand, because V is homeomorphic to
an open subset in Rn, Lemma 13.21 implies Hn−1(V (cid:3){x}) (cid:14)= 0. On the
other hand, V (cid:3){x}≈Rm(cid:3){0}(cid:25)Sm−1, so Hn−1(V (cid:3){x})=0.
Degree Theory for Spheres
In Problem 8-7, we defined the degree of a continuous map f: S1 → S1.
Homology theory allows us to extend this definition to higher-dimensional
spheres. Suppose n≥1. Because H (Sn) is infinite cyclic, if f: Sn →Sn is
n
any continuous map, f∗: H
n
(Sn) → H
n
(Sn) is multiplication by a unique
integer (Exercise A.28), called the degree of f and denoted by degf.
Proposition 13.23. Suppose n ≥ 1 and f,g: Sn → Sn are continuous
maps.
(a) If f (cid:25)g, then degf =degg.
(b) deg(g◦f)=(degg)(degf).
(c) The identity map has degree 1.
Proof. Part(a)followsfromthefactthathomotopicmapsinducethesame
homology homomorphism; part (b) from the fact that (g ◦ f)∗ = g∗ ◦
f∗; and part (c) from the fact that the identity map induces the identity
homomorphism on homology.
For a map f: S1 → S1 the definition of degf given in Problem 8-7 was
the unique integer k such that the homomorphism (ρ◦f)∗: π1(S1,1) →
π1(S1,1) is given by γ (cid:10)→γk, where ρ is the rotation taking f(1) to 1. For
the moment, let us call that definition the homotopic degree of f, and the
degree we have defined in this chapter its homological degree.
Lemma 13.24. Thehomologicaldegreeandthehomotopicdegreeofacon-
tinuous map f: S1 →S1 are equal.
Proof. By examining the definition of the Poincar´e homomorphism γ, it is
easy to see that the following diagram commutes:
π1(S1,1)
(ρ◦f)(cid:2)∗
π1(S1,1)
γ γ
(cid:5) (cid:5)
H1(S1)
(ρ◦f)
(cid:2)
∗
H1(S1).

---

Applications 321
Itfollowsthatthehomotopicdegreeoff isequaltothehomologicaldegree
of ρ ◦ f. Since the rotation ρ is homotopic to the identity map, it has
homological degree 1, so the homological degree of ρ◦f is equal to that of
f.
Some of the most important applications of degree theory come from
considering the antipodal map A: Sn →Sn given by A(x)=−x.
Lemma 13.25. Foreach n≥1,theantipodalmap A: Sn →Sn hasdegree
(−1)n+1.
Proof. Consider the reflection maps R : Sn →Sn given by
i
R
i
(x1,…,x
i
,…,x n+1)=(x1,…,−x
i
,…,x n+1).
We will prove by induction on n that R has degree −1; because the an-
i
tipodal map is equal to the (n+1)-fold composition R1 ◦···◦R n+1, it
follows that A has degree (−1)n+1.
Note that if degR = −1 for one value of i the same is true for all of
i
them, because R can be obtained from R by conjugating with the linear
i j
transformation that interchanges x and x .
i j
For n = 1, R2(z) = z in complex notation, which has degree −1 by
Problem 8-7. So suppose n > 1, and assume that the claim is true for
reflections in dimension n−1.
Recall that in the course of proving Proposition 13.14 we showed that
H
n
(Sn) ∼ =H n−1(Sn−1). In fact, we will refine that argument to show that
there is an isomorphism between these groups such that the following dia-
gram commutes:
H
n
(Sn) (cid:2) H n−1(Sn−1)
R1∗ R1∗
(cid:5) (cid:5)
H
n
(Sn) (cid:2) H n−1(Sn−1). (13.17)
From this it follows immediately by induction that R1 has degree −1 on
Sn.
To prove (13.17), let U = {U,V} be the covering of Sn by contractible
open sets used in the proof of Proposition 13.14 (the complements of the
north and south poles). Note that R1 preserves the sets U and V, and
therefore induces chain maps that make the following diagram commute:
0 (cid:2) C∗(U ∩V) (cid:2) C∗(U)⊕C∗(V) (cid:2) C
∗
U(Sn) (cid:2) 0
R1# R1# ⊕R1# R1#
(cid:5) (cid:5) (cid:5)
0 (cid:2) C∗(U ∩V) (cid:2) C∗(U)⊕C∗(V) (cid:2) C
∗
U(Sn) (cid:2) 0.

---

322 13. Homology
Therefore, by the naturality property of ∂∗, the following diagram also
commutes:
H
n
(Sn)
∂∗(cid:2)
H n−1(U ∩V)
(cid:12)ι∗
H n−1(Sn−1)
R1∗ R1∗ R1∗
(cid:5) (cid:5) (cid:5)
H
n
(Sn)
∂∗
(cid:2) H n−1(U ∩V) (cid:12)
ι∗
H n−1(Sn−1),
where Sn−1 = Sn ∩{x : x n+1 = 0} is the equatorial (n−1)-sphere and
ι: Sn−1 → U ∩V is inclusion. The horizontal maps are isomorphisms: ι∗
becauseιisahomotopyequivalence,and∂∗bytheargumentintheproofof
Proposition13.14.Composingthehorizontalisomorphismsandeliminating
the middle column, we obtain (13.17).
Proposition 13.26. The antipodal map A: Sn → Sn is homotopic to the
identity map if and only if n is odd.
Proof. If n=2k−1 is odd, an explicit homotopy H: Id(cid:25)A is given by
H(x,t)=((cosπt)x1+(sinπt)x2,(cosπt)x2 −(sinπt)x1,
…,(cosπt)x2k−1+(sinπt)x2k ,(cosπt)x2k −(sinπt)x2k−1).
Ifn=0,AinterchangesthetwopointsofS0,andsoisclearlynothomotopic
to the identity. When n is even and positive, A has degree −1, while the
identity map has degree 1, so they are not homotopic.
A vector field on Sn is a continuous map V : Sn → Rn+1 such that for
each x ∈ Sn, V(x) is tangent to Sn at x, or in other words the Euclidean
·
dotproductV(x) x=0.Thefollowingtheoremispopularlyknownasthe
“hairy ball theorem” because in the two-dimensional case it implies that
you cannot comb the hair on a hairy billiard ball without introducing a
discontinuity somewhere.
Theorem 13.27 (The Hairy Ball Theorem). There exists a nowhere
vanishing vector field on Sn if and only if n is odd.
Proof. Suppose there exists such a vector field V. By replacing V with
V/|V|, we can assume |V(x)| = 1 everywhere. We use V to construct a
homotopy between the identity map and the antipodal map as follows:
H(x,t)=(cosπt)x+(sinπt)V(x).
Directcomputation,usingthefactsthat|x|2 =|V(x)|2 =1andx · V(x)=
0,showsthatH takesitsvaluesinSn.SinceH(x,0)=xandH(x,1)=−x,
H is the desired homotopy. By Proposition 13.26, n must be odd.

---

The Homology of a Simplicial Complex 323
Conversely, when n=2k−1 is odd, the following explicit vector field is
easily checked to be tangent to the sphere and nowhere vanishing:
V(x1,…,x2k )=(x2,−x1,x4,−x3,…,x2k ,−x2k−1).
The Homology of a Simplicial Complex
Because both simplicial complexes and singular homology are built out of
simplices, it is reasonable to expect that the homology of a simplicial com-
plexshouldbecomputablefromthecombinatorialstructureofthecomplex.
In this section we define another kind of homology group associated with
a simplicial complex, called simplicial homology groups, and prove that
they are isomorphic to the singular homology groups. As an application,
we prove the topological invariance of the Euler characteristic.
Let K be a finite simplicial complex. We define the pth simplicial chain
group of K, denoted by CΔ(K), to be the free abelian group on the set of
p
p-simplices in K.
To define the boundary operator, we choose a total ordering of the ver-
tices (v1,…,v
N
), and for a p-simplex (cid:22)v
k0
,…,v
kp
(cid:23) we set
(cid:14)p
∂(cid:22)v
k0
,…,v
kp
(cid:23)= (−1)i(cid:22)v
k0
,…,v(cid:18)
ki
,…,v
kp
(cid:23) if k0 <···<k
p
.
i=0
This extends uniquely to a homomorphism ∂: CΔ(K)→CΔ (K).
p p−1
Lemma 13.28. For any simplicial p-chain c, ∂(∂c)=0.
Proof. It suffices to show this when c is a p-simplex σ = (cid:22)v ,…,v (cid:23), in
k0 kp
which case (assuming that the vertices appear in increasing order),
(cid:14)p
∂(∂σ)=∂ (−1)i(cid:22)v ,…,v(cid:18) ,…,v (cid:23)
k0 ki kp
i(cid:14)=0
= (−1)i+j(cid:22)v ,…,v(cid:18) ,…,v(cid:18) ,…,v (cid:23)
k0 kj ki kp
0≤j<i≤p
(cid:14)
+ (−1)i+j(cid:22)v ,…,v(cid:18) ,…,v(cid:18) ,…,v (cid:23).
k0 ki kj+1 kp
0≤i≤j≤p−1
After j = i(cid:5) −1 and i = j(cid:5) are substituted in the second sum, these two
sums cancel each other term by term.

---

324 13. Homology
We define
ZΔ(K)=Ker∂: CΔ(K)→CΔ (K),
p p p−1
BΔ(K)=Im∂: CΔ (K)→CΔ(K),
p p+1 p
the groups of simplicial cycles and simplicial boundaries, respectively. The
preceding lemma shows that BΔ(K) is a subgroup of ZΔ(K), so we may
p p
define the pth simplicial homology group of K to be the quotient
HΔ(K)=ZΔ(K)/BΔ(K).
p p p
Because the simplicial chain groups of a finite complex are all finitely
generated, simplicial homology can in principle be computed directly from
the combinatorial structure of a complex. In practice this is not usually
efficient, at least without a computer, because triangulations of even very
simplespacestypicallyhavealargenumberofsimplices.Wewillseebelow
that the simplicial homology groups are isomorphic to the singular ones.
However, there is one case in which simplicial homology is not hard to
compute directly.
Lemma 13.29. LetKbeacomplexconsistingofasinglen-simplexandits
faces. Then HΔ(K) is the infinite cyclic group generated by the homology
0
class of any vertex, and HΔ(K) is trivial for p>0.
p
Proof. We assume that an ordering (v0,…,v
p
) has been chosen for the
vertices of K. Define a homomorphism h: CΔ(K) → CΔ (K) by setting,
p p+1
for any p-simplex τ =(cid:22)v ,…,v (cid:23)∈K,
k0 kp
(cid:16)
hτ =
(cid:22)v0,v
k0
,…,v
kp
(cid:23) if k0 (cid:14)=0,
0 if k0 =0,
and extending h to a homomorphism.
Whenp>0,astraightforwardcomputationshowsthat∂◦h+h◦∂ =Id.
Thus if c is any p-cycle, c=∂hc, which shows that HΔ(K)=0.
p (cid:15)
(cid:15)For p = 0, define a homomorphism ε: C
0
Δ(K) → Z by ε(
i
n
i
(cid:22)v
i
(cid:23)) =
i
n
i
asintheproofofProposition13.5.Becauseε(cid:22)v0 (cid:23)=1,εissurjective.
Another computation shows that ∂hc = c−ε(c)(cid:22)v0 (cid:23) for any 0-chain c, so
any chain in Kerε is a boundary. Conversely, any boundary is in Kerε
because ε∂(cid:22)v ,v (cid:23) = ε((cid:22)v (cid:23)−(cid:22)v (cid:23)) = 0 (assuming i < j). This shows that
i j j i
ε descends to an isomorphism from HΔ(K) to Z, so HΔ(K) is the infinite
0 0
cyclic group generated by the class of (cid:22)v0 (cid:23).
It should be noted that there are several alternative ways of defining
simplicial homology groups. The one most commonly used is to define the
simplicial chain group as the free abelian group on the set of oriented sim-
plices, with the convention that σ(cid:5) = −σ if σ(cid:5) is the same simplex as

---

The Homology of a Simplicial Complex 325
σ with the opposite orientation. Another possible chain group is the free
abelian group on all ordered simplices, considering different vertex order-
ings of the same simplex as distinct generators. Both of these definitions
have the advantage that, unlike our definition, they do not depend on a
choice of ordering of the vertices; this is important if one wishes to define
homomorphisms induced by simplicial maps (which may not preserve the
vertex ordering) and prove functorial properties such as topological and
homotopy invariance. If our goal were to develop an entire theory of sim-
plicialhomologygroups,wewouldhavetouseoneofthesedefinitions.But
our aim is more modest: We wish only to show that simplicial homology
gives an alternative way of computing the singular homology groups, so
we use a definition that is technically somewhat simpler, and confine our
attention to the properties needed for this purpose.
The main result we need is an analogue of the Mayer–Vietoris theorem
for simplicial homology. Fortunately, its proof is much easier than in the
singular case.
The setup for this theorem is slightly different from that of its singular
cousin. In this case, instead of considering open subsets, we suppose K(cid:5)
and K(cid:5)(cid:5) are subcomplexes of K, and let L = K(cid:5) ∩ K(cid:5)(cid:5) (which is also a
subcomplex). As in the singular case, we have inclusion maps
K(cid:5)
(cid:3)(cid:4) (cid:6)
i (cid:3) (cid:6)k
(cid:3) (cid:6)(cid:7)
L K.
(cid:6) (cid:3)(cid:4)
j (cid:6) (cid:3)l
(cid:6)(cid:7) (cid:3)
K(cid:5)(cid:5)
Each of these induces an inclusion map on simplicial chains, which is a
chain map, provided that we choose the vertex orderings in K(cid:5), K(cid:5)(cid:5), and
L to be the restrictions of the ordering we chose for K. Therefore, all four
maps induce homology homomorphisms as well.
Theorem 13.30 (Simplicial Mayer–Vietoris Theorem). Let K be a
finite simplicial complex, with subcomplexes K(cid:5),K(cid:5)(cid:5) whose union is K,
and let L = K(cid:5) ∩ K(cid:5)(cid:5). For each p there is a connecting homomorphism
∂∗: H
p
Δ(K)→H
p
Δ
−1
(L) such that the following sequence is exact:
···−∂→∗ HΔ(L)−i−∗⊕ −j→∗ HΔ(K(cid:5))⊕H (K(cid:5)(cid:5))−k−∗−−−l→∗ HΔ(K)
p p p p
−∂→∗ HΔ (L)−i−∗⊕ −j→∗ ··· .
p−1
Proof. The sequence of chain maps
0→CΔ(L)−i−#− ⊕ −j→# CΔ(K(cid:5))⊕CΔ(K(cid:5)(cid:5))−k−#− − −l→# CΔ(K)→0
p p p p

---

326 13. Homology
is easily seen to be exact in this case. The existence of the connecting
homomorphism and the exactness of the Mayer–Vietoris sequence then
follow immediately from the zigzag lemma.
To analyze the relationship between simplicial and singular homology,
we define a map from the simplicial chain complex of K to the singular
chain complex of its geometric realization as follows. For any p-simplex
σ = (cid:22)v ,…,v (cid:23) ∈ K, let α(σ) denote the affine singular p-simplex
k0 kp
α(v ,…,v ) in |K| (with the vertices in increasing order). This extends
uniq k u 0 ely to k a p homomorphism α: CΔ(K) → C (|K|). To see that it is a
p p
chain map, just compute
(cid:14)p
∂α(v ,…,v )= (−1)iα(v ,…,v )◦F
k0 kp k0 kp i,p
i=0
(cid:14)p
= (−1)iα(v ,…,v(cid:18) ,…,v )
k0 ki kp
i=0
=α(∂(cid:22)v ,…,v (cid:23)).
k0 kp
Therefore, α induces a homology homomorphism α∗: H
p
Δ(K)→H
p
(|K|).
Theorem 13.31. For any finite complex K, the map α∗: H
p
Δ(K) →
H (|K|) is an isomorphism for all p.
p
Proof. We prove the theorem by induction on the dimension of K. If
dimK = 0, then K is just a finite set of vertices. In this case, CΔ(K)
0
is the free abelian group on the set of vertices, and all the other simplicial
chain groups are trivial. Therefore, all the boundary operators are zero,
and HΔ(K) ∼ = CΔ(K), which is isomorphic to the corresponding singular
p p
group. The map α∗: H
0
Δ(K) → H0(|K|) takes each generator [(cid:22)v(cid:23)] to a
generator [α(v)], so the theorem is proved in this case.
Now suppose the theorem is true for complexes of dimension n−1, and
let K have dimension n. We proceed by induction on the number of n-
simplices in K. When there are no n-simplices, K is (n−1)-dimensional,
so the theorem is true in that case.
Suppose K(cid:5) is the subcomplex of K obtained by deleting a single n-
simplex σ. (It is a subcomplex because K has no simplices of dimension
greater than n.) Let K(cid:5)(cid:5) denote the subcomplex consisting of σ and all its
faces,andL=K(cid:5)∩K(cid:5)(cid:5).Wewillprovetheinductivestepbycomparingthe
Mayer–VietorissequenceofK(insimplicialhomology)withthatof|K|(in
singular homology).
To set up the sequence in singular homology, let V be a neighborhood
of |σ| that admits a strong deformation retraction onto |σ| (such a neigh-
borhood exists by Problem 7-6), and let U = |K|(cid:3){x} for some point
x ∈ Int|σ|. Clearly, |K(cid:5)| ⊂ U, |K(cid:5)(cid:5)| ⊂ V, and |L| ⊂ U ∩V. All of these
inclusions are homotopy equivalences: Our choice of V guarantees that it

---

The Homology of a Simplicial Complex 327
admits a strong deformation retraction onto |K(cid:5)(cid:5)|, and it is easy to con-
struct a strong deformation of U onto |K(cid:5)| that deforms σ(cid:3){x} onto its
boundary while leaving |K(cid:5)| fixed. Gluing these maps together, we obtain
a strong deformation retraction of U ∩V onto L.
Restrictingα: CΔ(K)→C (|K|)tothechaingroupsofthevarioussub-
p p
complexes yields the following diagram of chain maps, which is obviously
commutative:
0 (cid:2) CΔ(L) i# ⊕j(cid:2)# CΔ(K(cid:5))⊕CΔ(K(cid:5)(cid:5)) k# −l (cid:2)# CΔ(K) (cid:2) 0
∗ ∗ ∗ ∗
α α⊕α α
0 (cid:2) C∗(U (cid:5) ∩V) i# ⊕j(cid:2)# C∗(U)⊕ (cid:5) C∗(V) k# −l#(cid:2) C
∗
U(| (cid:5) K|) (cid:2) 0.
Therefore, using Proposition 13.16 we see that the following diagram com-
mutes and has exact rows:
HΔ(L) (cid:2) HΔ(K(cid:5))⊕HΔ(K(cid:5)(cid:5)) (cid:2) HΔ(K) (cid:2)
p p p p
(cid:5) (cid:5) (cid:5)
H (U ∩V) (cid:2) H (U)⊕H (V) (cid:2) HU(|K|) (cid:2)
p p p p
HΔ (L) (cid:2) HΔ (K(cid:5))⊕HΔ (K(cid:5)(cid:5))
p−1 p−1 p−1
(cid:5) (cid:5)
H p−1(U ∩V) (cid:2) H p−1(U)⊕H p−1(V).
With U ∩V, U, and V in these groups replaced by their homotopy equiv-
alent spaces |L|, |K(cid:5)|, and |K(cid:5)(cid:5)|, the diagram still commutes because the
homotopy equivalences are all inclusion maps. Thus we finally arrive at a
diagraminwhichalltheverticalhomomorphismsexceptthecenteroneare
isomorphisms. (For K(cid:5) and L this follows from the inductive hypothesis,
and for K(cid:5)(cid:5) it follows from Lemma 13.29.) Therefore, by the five lemma,
the middle arrow is also an isomorphism. Finally, replacing HU by H , we
p p
obtain the result.
Topological Invariance of the Euler Characteristic
Our most significant application of simplicial homology is the following
theorem, which generalizes Corollary 10.15 and Problem 10-9.
Theorem 13.32. The Euler characteristic of a finite simplicial complex
K is given by the formula
(cid:14)
χ(K)= (−1)prankH (|K|).
p
p
Therefore, the Euler characteristic is a topological invariant of |K|.

---

328 13. Homology
Proof. Let n=dimK. Recall from Chapter 5 that the Euler characteristic
of K is defined as
(cid:14)n
χ(K)= (−1)pc ,
p
p=0
where c is the number of p-simplices in K. Note that c is also the rank
p p
of the simplicial chain group CΔ(K).
p
Consider the following short exact sequences:
0→BΔ(K)(cid:9)→ZΔ(K)→HΔ(K)→0,
p p p
0→ZΔ(K)(cid:9)→CΔ(K)→∂ BΔ (K)→0.
p p p−1
Let us write
b =rankBΔ(K), z =rankZΔ(K), h =rankHΔ(K).
p p p p p p
By Proposition 9.16, we have the following equalities:
z =h +b ,
p p p
c
p
=z
p
+b p−1.
Therefore,
(cid:14)n
χ(K)= (−1)pc
p
p=0
(cid:14)n
= (−1)p(z
p
+b p−1)
p=0
(cid:14)n
= (−1)p(h
p
+b
p
+b p−1).
p=0
Because b−1 = b n = 0, the b p and b p−1 terms above form a telescoping
sum adding to zero. Because h = rankH (|K|) by Theorem 13.31, this
p p
completes the proof.
For any topological space X, the integer β (X)=rankH (X) (if it is fi-
p p
nite)iscalledthepthBettinumberofX.WedefinetheEulercharacteristic
of X by
(cid:14)
χ(X)= (−1)pβ (X)
p
p
provided that each β (X) is finite and β (X) = 0 for p sufficiently large.
p p
Theprecedingtheoremthensaysthatχ(K)=χ(|K|)forafinitesimplicial
complex K.

---

Cohomology 329
Cohomology
As Proposition 13.2 shows, the singular homology groups are covariant
functors from the category of topological spaces to the category of abelian
groups.Formanyapplications,itturnsouttobemuchmoreusefultohave
contravariant functors. We will not pursue any of these applications here,
butcontentourselvestonotethatoneofthemostimportant,thedeRham
theory of differential forms, plays a central role in differential geometry.
To give you a view of what is to come, in this final section we introduce
singularcohomology,whichisessentiallyacontravariantversionofsingular
homology.Itdoesnotgiveusanynewinformationabouttopologicalspaces,
but the information is organized in a different way, which is much more
appropriate for some applications.
In Example 7.32 we observed that for any fixed abelian group G, there
is a contravariant functor from the category of abelian groups to itself
that sends each group X to the group Hom(X,G) of homomorphisms into
G, and each homomorphism f: X → Y to the induced homomorphism
f∗: Hom(Y,G) → Hom(X,G) given by f∗(ϕ) = ϕ◦f. We apply this to
the singular chain groups as follows. Given a topological space X and an
abelian group G, for any integer p ≥ 0 let Cp(X;G) denote the group
Hom(C (X),G). Elements of Cp(X;G) are called p-dimensional singular
p
cochains with coefficients in G (p-cochains for short).
Theboundaryoperator∂: C p+1(X)→C
p
(X)inducesahomomorphism
δ: Cp(X;G)→Cp+1(X;G), called the coboundary operator, characterized
by
(δϕ)(c)=ϕ(∂c).
It is immediate that δ◦δ =0, so we have a chain complex
···→Cp−1(X;G)−→δ Cp(X;G)−→δ Cp+1(X;G)→··· .
(Actually, when the arrows go in the direction of increasing indices as in
this case, it is customary to call it a cochain complex.) A p-cochain ϕ is
calledacocycleifδϕ=0,andacoboundaryifthereexistsψ ∈Cp−1(X;G)
such that δψ = ϕ. The subgroups of Cp(X;G) consisting of cocycles and
coboundaries are denoted by Zp(X;G) and Bp(X;G), respectively.
We define the pth singular cohomology group of X with coefficients in G
to be the quotient
Hp(X;G)=Zp(X;G)/Bp(X;G).
If f: X → Y is a continuous map, we obtain a map f#: Cp(Y;G) →
Cp(X;G) (note the reversal of direction) by
(f#ϕ)(c)=ϕ(f#c).

---

330 13. Homology
This map commutes with the coboundary operators because
(f#δϕ)(c)=δϕ(f#c)=ϕ(∂f#c)=ϕ(f#∂c)=(f#ϕ)(∂c)=(δf#ϕ)(c).
(Amapthatcommuteswithδiscalled,predictablyenough,acochainmap.)
Therefore, f# induces a cohomology homomorphism f∗: Hp(Y;G) →
Hp(X;G) by f∗[ϕ]=[f#ϕ].
Proposition 13.33. The induced cohomology homomorphism satisfies the
following properties.
(a) If f: X →Y and g: Y →Z are continuous, then (g◦f)∗ =f∗◦g∗.
(b) The homomorphism induced by the identity map is the identity.
Therefore, the assignment X (cid:10)→Hp(X;G), f (cid:10)→f∗ defines a contravariant
functor from the category of topological spaces to the category of abelian
groups.
Corollary 13.34 (Topological Invariance of Cohomology). If
f: X → Y is a homeomorphism, then for any abelian group G and any
integer p≥0, f∗: Hp(Y;G)→Hp(X;G) is an isomorphism.
Exercise 13.4. Prove Proposition 13.33 and Corollary 13.34.
Inaveryspecificsense,thesingularcohomologygroupsexpressthesame
information as the homology groups, but in rearranged form. The precise
statementisgivenbytheuniversalcoefficienttheorem,whichgivesanexact
sequence from which the cohomology groups with any coefficients can be
computed from the singular homology groups. The statement and proof
can be found in [Mun75] or [Spa89]. We will not go into the general case
here, but we can easily handle one special case.
Let F be a field of characteristic zero, which just means thatF is torsion
free as an abelian group under addition. (In most applications F will be
R, C, or Q.) We can form the cohomology groups Hp(X;F) as usual, just
by regarding F as an abelian group; but in this case they have a bit more
structure. The basic algebraic facts are expressed in the following lemma.
Lemma 13.35. Let F be a field of characteristic zero.
(a) ForanyabeliangroupG,thesetHom(G,F)ofgrouphomomorphisms
fromGtoFisavectorspaceoverFwithscalarmultiplicationdefined
pointwise: (aϕ)(g)=a(ϕ(g)) for a∈F.
(b) If f: G1 → G2 is a group homomorphism, then the induced homo-
morphism f∗: Hom(G2,F)→Hom(G1,F) is a linear transformation
of vector spaces.

---

Cohomology 331
(c) If G is finitely generated, the dimension of Hom(G,F) is equal to the
rank of G.
Proof. The proofs of (a) and (b) are straightforward (and hold for any
field, not just one of characteristic zero), and are left as an exercise. For
(c), we proceed as follows. First suppose G is free abelian of rank n, and
let g1,…,g
n
be a basis for G (as an abelian group). For each i, define a
homomorphism ϕ : G→F by setting
i
(cid:16)
1 if i=j,
ϕ (g )=
i j 0 if i(cid:14)=j.
(cid:15)
If a ϕ isthezerohomomorphismforsomescalarsa ∈F,applyingthis
i i i i
homomorphism to g shows that a = 0, so the ϕ ’s are linearly indepen-
j j i
dent. On the other h(cid:15)and, it is easy to see that an arbitrary ϕ∈Hom(G,F)
can be written ϕ = a ϕ with a = ϕ(g ); thus the ϕ ’s are a basis for
i i i i i i
Hom(G,F), proving the result in this case.
In the general case, let Gtor ⊂ G be the torsion subgroup of G.
The surjective homomorphism π: G → G/Gtor induces a homomorphism
π∗: Hom(G/Gtor,F) → Hom(G,F). It follows easily from the surjectivity
of π that π∗ is injective. On the other hand, let ϕ ∈ Hom(G,F) be ar-
bitrary. If g ∈ G satisfies kg = 0, then ϕ(g) = ϕ(kg)/k = 0, so Gtor ⊂
Kerϕ and ϕ descends to a homomorphism ϕ(cid:7) ∈ Hom(G/Gtor,F). Clearly,
π∗ϕ(cid:7)=ϕ,soπ∗ isanisomorphism.BecauseG/Gtor isfreeabelian,wehave
dimHom(G,F)=dimHom(G/Gtor,F)=rank(G/Gtor)=rankG.
Exercise 13.5. Prove parts (a) and (b) of Lemma 13.35.
Applying this to Cp(X;F) = Hom(C (X),F), we see that the cochain
p
groups are F-vector spaces and the coboundary operators are linear maps.
It follows that Zp(X;F) and Bp(X;F) are vector spaces as is the quo-
tient Hp(X;F) = Zp(X;F)/Bp(X;F). Moreover, for any continuous map
f: X →Y,theinducedcohomologymapf∗: Hp(Y;F)→Hp(X;F)isalso
a linear map.
Thespecialfeatureoffieldcoefficientsthatmakesthecohomologygroups
easier to calculate is expressed in the following lemma.
Lemma 13.36 (Extension Lemma). Let F be a field of characteristic
zero. If G is an abelian group, any group homomorphism from a subgroup
of G to F admits an extension to all of G.
Proof. Suppose H ⊂ G is a subgroup and f: H → F is a homomorphism.
Consider the set F of all pairs (H(cid:5),f(cid:5)), where H(cid:5) is a subgroup of G con-
taining H and f(cid:5): H(cid:5) → F is an extension of f. Define a partial ordering
on F by declaring (H(cid:5),f(cid:5)) ≤ (H(cid:5)(cid:5),f(cid:5)(cid:5)) if H(cid:5) ⊂ H(cid:5)(cid:5) and f(cid:5)(cid:5)| H(cid:3) = f(cid:5). Given
any totally ordered subset T ⊂ F, define H (cid:7) to be the union of all the

---

332 13. Homology
spaces H(cid:5) such that (H(cid:5),f(cid:5)) ∈ T. There is a uniquely defined homomor-
phism f (cid:7) : H (cid:7) →F, defined by setting f (cid:7) (h)=f(cid:5)(h) for any pair (H(cid:5),f(cid:5))∈T
such that h∈H(cid:5). The pair (H (cid:7) ,f (cid:7) ) is easily seen to be an upper bound for
T. Thus by Zorn’s lemma (Lemma A.3 in the Appendix), there exists a
maximal element in F; call it (H0,f0).
If H0 =G, we are done. If not, we will show that f0 can be extended to
a larger subgroup containing H0, which contradicts the maximality of H0.
Suppose there is some element g ∈G(cid:3)H0. Let H
g
denote the subgroup
H
g
={h+mg :h∈H0,m∈Z}.
ThequotientgroupH
g
/H0 iscyclicandgeneratedbythecosetofg.There
are two cases.
If H
g
/H0 is infinite, then no multiple of g is in H0, so every element
of H can be written uniquely in the form h+mg and we can define an
g
extensionf
0
(cid:5) off0 justbysettingf
0
(cid:5)(h+mg)=f0(h).Ontheotherhand,if
H
g
/H0 isfinite,letnbetheorderofthisgroup.Thismeansthatmg ∈H0
if and only if m is a multiple of n. Let k = f0(ng)/n ∈ F, and define an
extension f
0
(cid:5) of f0 by letting
f
0
(cid:5)(h+mg)=f0(h)+mk.
Toshowthatthisiswell-defined,supposeh+mg =h(cid:5)+m(cid:5)g forh,h(cid:5) ∈H0
andm,m(cid:5) ∈Z.Then(m−m(cid:5))g =h(cid:5)−h∈H0,whichimpliesm−m(cid:5) =jn
for some integer j. We compute
(f0(h)+mk)−(f0(h(cid:5))+m(cid:5)k)=f0(h−h(cid:5))+(m−m(cid:5))k
=f0(−jng)+jnk =0.
Therefore, f
0
(cid:5) is an extension of f0, which completes the proof.
Now we come to the main result of this section, which gives explicit
formulas for singular cohomology with coefficients in F.
Theorem 13.37. LetFbeafieldofcharacteristiczero.Foranytopological
space X, the vector spaces Hp(X;F) and Hom(H (X),F) are isomorphic;
p
hence if H (X) is finitely generated, then the dimension of Hp(X;F) is
p
equal to the rank of H (X).
p
Proof. An arbitrary cocycle ϕ ∈ Zp(X;F) defines a homomorphism
ϕ(cid:7): H (X)→F by
p
ϕ(cid:7)[c]=ϕ(c).
Since ϕ(∂b) = δϕ(b) = 0, this is well-defined independently of the choice
of representative c in its homology class. If ϕ = δη is a coboundary, then
ϕ(cid:7)[c] = ϕ(c) = δη(c) = η(∂c) = 0, so the homomorphism ϕ (cid:10)→ ϕ(cid:7) contains

---

Cohomology 333
the coboundary group Bp(X;F) in its kernel. It therefore descends to a
homomorphism β: Hp(X;F) → Hom(H (X),F), given by β[ϕ] = ϕ(cid:7). We
p
will show that β is an isomorphism.
Let f ∈ Hom(H (X),F) be arbitrary. Letting π: Z (X) → H (X)
p p p
denote the projection defining H (X), we obtain a homomorphism f ◦
p
π: Z (X)→F. By the extension lemma, this extends to a homomorphism
p
ϕ: C (X)→F, i.e., a p-cochain. In fact, ϕ is a coboundary, because
p
(δϕ)c=ϕ(∂c)=f ◦π(∂c)=f[∂c]=0.
Unwinding the definitions, we see that f =β[ϕ], so β is surjective.
To show that it is injective, suppose β[ϕ] = 0. This means that ϕ ∈
Cp(X;F) satisfies ϕ(c) = 0 for all cycles c, so Z (X) ⊂ Kerϕ. Therefore,
p
ϕ descends to a homomorphism ϕ(cid:7): C (X)/Z (X)→F.
p p
Ontheotherhand,thesurjectivehomomorphism∂: C
p
(X)→B p−1(X)
has kernel equal to Z (X), and therefore induces an isomorphism
p
∂ (cid:7) : C
p
(X)/Z
p
(X) → B p−1(X). Composition gives a homomorphism ϕ(cid:7)◦
∂ (cid:7)−1: B p−1(X)→F:
B p−1(X)−∂ (cid:7) − − → 1 C
p
(X)/Z
p
(X)−→ϕ(cid:7) F.
By the extension lemma, this extends to a homomorphism η: C p−1(X)→
F. If c∈C (X) is arbitrary,
p
η(∂c)=(ϕ(cid:7)◦∂ (cid:7)−1)(∂c)=ϕ(c),
which shows that ϕ = δη, and so [ϕ] = 0. Thus β is injective, completing
the proof.
As a consequence of this theorem, the Euler characteristic of a space
can also be computed in terms of its cohomology. The following corollary
follows immediately from the theorem.
Corollary 13.38. If X is a topological space such that H (X) is finitely
p
generated for all p and zero for p sufficiently large, then for any field F of
characteristic zero,
(cid:14)
χ(X)= (−1)pdimHp(X;F).
p

---

334 13. Homology
Problems
13-1. Let Pn be the real projective space of dimension n.
(a) Show that Pn is homeomorphic to the quotient of Bn by the
relationthatidentifiesantipodalpointsontheboundarysphere.
(b) Use (a) and the results of this chapter to compute the singular
homology groups of P2 and P3.
13-2. Let n≥1. If f: Sn →Sn is a continuous map that has a continuous
extension to a map F: Bn+1 →Sn, show that f has degree zero.
13-3. Show that Sn is not a retract of Bn+1 for any n.
13-4. ProvetheBrouwerfixedpointtheorem:Anycontinuousmapf: Bn →
Bn has a fixed point. [See Problem 8-9.]
13-5. Show that the dimension of a finite-dimensional simplicial complex
K is a topological invariant of |K|, and that any triangulation of an
n-manifold has dimension n. [Be careful: We are not assuming that
the complexes are finite.]
13-6. Prove that the singular homology groups of any compact polyhedron
are finitely generated.
13-7. If M is a triangulable compact manifold, show that H (M) = 0 if
p
p>dimM.
13-8. Ann-dimensionalpseudomanifoldisann-dimensionalsimplicialcom-
plex in which every simplex is a face of some n-simplex, every
(n−1)-simplex is a face of exactly two n-simplices, and for every
pair of n-simplices σ,σ(cid:5) there exists a finite sequence of n-simplices
σ =σ1,…,σ
k
=σ(cid:5)suchthatσ
i
andσ i+1havean(n−1)-dimensional
faceincommon.Showthatthenth(singularorsimplicial)homology
groupofann-dimensionalpseudomanifoldisinfinitecyclicifitisori-
entable and trivial if not. [It can be shown (see, e.g., [Mun75]) that
everytriangulated,connected,compactmanifoldisapseudomanifold,
and then this result characterizes the nth homology of triangulable
compactn-manifolds.Butthisrequiresmoremachinerythanwehave
developed.]
13-9. Suppose M is an n-manifold with boundary. Show that the set of
boundary points and the set of interior points of M are disjoint.
13-10. Let X1 and X2 be spaces with nondegenerate base points q1 and q2.
Show that H
p
(X1 ∨X2) ∼ =H
p
(X1)⊕H
p
(X2) for all p>0. [Hint: For
p=1, use Problem 10-15.]

---

Problems 335
13-11. A (covariant or contravariant) functor from the category of abelian
groups to itself is said to be exact if it takes exact sequences to exact
sequences. If F is a field of characteristic zero, show that the functor
G(cid:10)→Hom(G,F), f (cid:10)→f∗ is exact.
13-12. If U and V are open subsets of the topological space X, prove that
there is an exact Mayer–Vietoris sequence for cohomology with coef-
ficients in a field F of characteristic zero:
···→Hp−1(U ∩V;F)→Hp(X;F)→Hp(U;F)⊕Hp(V;F)→
Hp(U ∩V;F)→··· .
[Hint: Use Problem 13-11.]
13-13. AnabeliangroupKissaidtobedivisibleifforanyk ∈Kandnonzero
n∈Z,thereexistsk(cid:5) ∈K suchthatnk(cid:5) =k.Itissaidtobeinjective
if for every group G, any homomorphism from a subgroup of G into
K extends to all of G. Show that an abelian group K is injective if
and only if it is divisible if and only if the functor G (cid:10)→ Hom(G,K)
is exact.

---

Appendix
Review of Prerequisites
The most important prerequisite for studying this book is a thorough
grounding in advanced calculus. Since there are hundreds of books that
treat this subject well, we will simply assume familiarity with it, and re-
mind the reader of important facts when necessary. We also assume that
the reader is familiar with the terminology and rules of ordinary logic.
The other prerequisites are a solid understanding of the basic properties
of sets, metric spaces, and groups, at the level that you would find in most
undergraduate courses in real analysis and abstract algebra.
In this appendix we briefly review some fundamental aspects of these
threesubjects.Ifyouhavenotstudiedthismaterialbefore,youcannothope
to learn it from scratch here. But this appendix can serve as a reminder of
important concepts that you may have forgotten, as a way to standardize
ournotationandterminology,andasasourceofreferencestobookswhere
you can look up more of the details to refresh your memory. You can use
the exercises to test your knowledge, or to brush up on any aspects of the
subject on which you feel your knowledge is shaky.
Set Theory
In this book, as in most modern mathematics, mathematical statements
are couched in the language of set theory. We give here a brief descriptive
summary of the parts of set theory that we will use, in the form that is
commonlycalled“naivesettheory.”Thewordnaiveshouldbeunderstood

---

338 Appendix: Review of Prerequisites
in the same sense in which it is used by Paul Halmos in his classic text
Naive Set Theory [Hal74]: The axioms of set theory are to be viewed much
as Euclid viewed his geometric axioms, as intuitively clear statements of
fact from which reliable conclusions can be drawn.
One must be a bit careful with the axioms, to be sure, because it is
possible to get into trouble by trying to construct sets too freely, as is
illustrated by the famous paradox of Bertrand Russell described below. It
isprimarilyforthisreasonthatwetakethetroubletoenumeratetheaxioms
at all. For more detail on the subject, in the same spirit as the treatment
here, consult [Hal74] or [Dev93]. We leave it to the set theorists to explore
the deep consequences of the axioms and the relationships among different
axiom systems.
Basic Concepts
The word set is, mathematically, an undefined term. A set should be
thought of as an assemblage of “mathematical objects,” whatever they
may be—things such as numbers, ordered pairs, functions, or other sets.
The properties of sets, and the rules for manipulating them, are expressed
in the axioms we list below. We sometimes use the words collection and
family as synonyms for set.
The fundamental relationship involving sets, which we also leave math-
ematically undefined, is that of membership. Intuitively, if x is one of the
objects in the set S, then we say that x is a member or an element of S,
or x belongs to S, written x∈S. The essential characteristic of sets is that
theyaredeterminedbytheirmembers.Formally,wedefineS =T tomean
x∈S ⇐⇒ x∈T.
The set containing no elements is called the empty set and denoted by
∅. It is unique, because any two sets with no elements are equal by our
definition of set equality, so we are justified in calling it “the” empty set.
(Wecouldpostulateitsexistenceasaseparateaxiom,butitsexistencewill
follow from our other axioms, as you will see below.) If S and T are sets
such that every element of S is also an element of T, then S is a subset of
T, written S ⊂ T. It is a proper subset if S ⊂ T but S (cid:14)= T. The notation
T ⊃S means S ⊂T. Clearly, S =T if and only if S ⊂T and T ⊂S.
Theaxiomsforsetsdescribepreciselywhatsetscanbeassertedtoexist,
and what properties they have. Here is the first one.
- Specification axiom: Given a set S and a sentence P(x) that is
either true or false whenever x is any particular element of S, there
is a set consisting of all those x ∈ S for which P(x) is true, denoted
by {x∈S :P(x)}.
Note that one must start with a specific set before the specification
axiom can be used. This requirement rules out forming sets out of self-
contradictoryspecificationssuchastheonediscoveredbyBertrandRussell

---

Set Theory 339
and now known as “Russell’s paradox”: The sentence C = {X : X (cid:14)∈ X}
looks as if it might define a set, but it does not, because each statement
C∈CandC(cid:14)∈Cimpliesitsownnegation.Similarly,thespecificationaxiom
implies that there does not exist a “set of all sets,” for if there were such a
set S, we could use the specification axiom to define C = {S ∈ S : S (cid:14)∈ S}
and reach the same contradiction.
Still, there are times when we will need to speak of “all sets” or other
similaraggregations,primarilyinthecontextofcategorytheory(seeChap-
ter 7). For this purpose, we reserve the word class to refer to an aggregate
of mathematical objects that may or may not constitute a set.
- Power set axiom: Given any set S, there is a set P(S), called the
power set of S, whose elements are exactly the subsets of S.
- Union axiom: Given any co(cid:2)llection C of sets, there is a set (cid:2)called
their union and denoted by C, with the property that x ∈ C if
and only if x∈S for some S ∈C.
(cid:9)Given any nonempty collection C of sets, their intersection, denoted by
C, is defined as the set
(cid:4) (cid:2)
C={x∈ C:x∈S for every S ∈C}.
Other notations for unions and intersections are
(cid:5)
S; S1 ∪S2 ∪··· ;
S(cid:4) ∈C
S; S1 ∩S2 ∩··· .
S∈C
GivenanycollectionCofsets,ifA∩B =∅wheneverA,B ∈CandA(cid:14)=B,
the sets in C are said to be disjoint.
If A and B are any sets, their set difference is defined to be the set
A(cid:3)B ={x∈A:x(cid:14)∈B},
which exists by the specification axiom. If B ⊂A, the set difference A(cid:3)B
is also called the complement of B in A.
When sets are defined by specification, it is common to abbreviate the
notation in certain circumstances if it can be done unambiguously. For ex-
ample,iftheelementsofasetcanbenamedexplicitly,thesetiscommonly
specified simply by listing its elements, as in {a1,a2,…,a
k
}. As long as
each of the elements a is an element of some other set S , this is a legit-
i i
imate use of our axioms and can be interpreted as {x ∈ S1 ∪···∪S
k
:
x = a1 or x = a2 or … or x = a
k
}. Since the resulting set is the same
regardlessofwhatsetsS thea ’soriginallycamefrom,thereisnoneedto
i i
include them in the notation. A set {a} with a unique element a is called
a singleton.

---

340 Appendix: Review of Prerequisites
Cartesian Products, Relations, and Functions
Another primitive concept that we will use without a formal definition is
that of an ordered pair. Think of it as a pair of objects in a specific order,
indicated by writing them in parentheses and separated by a comma, as in
(a,b). The objects a and b are called the components of the ordered pair.
The defining characteristic is that two ordered pairs are equal if and only
if their first components are equal and their second components are equal:
(a,b)=(a(cid:5),b(cid:5)) ⇐⇒ a=a(cid:5) and b=b(cid:5).
- Cartesian product axiom: GivensetsAandB,thereexistsaset
A×B, called their Cartesian product, whose members are precisely
the ordered pairs (a,b) for every a∈A and b∈B.
With these axioms we can define the most important constructions in
mathematics: relations and functions. A relation between sets X and Y is
a subset of X ×Y. If r is a relation, it is often convenient to use some
notation such as x(cid:28)r y to mean (x,y)∈r. For example, both “equals” and
“less than” are relations in R×R.
An important special case arises when we consider relations between a
setS anditself,whichweusuallycallarelation“onS.”Let∼denotesuch
a relation. It is said to be reflexive if x ∼ x for all x ∈ S, symmetric if
x ∼ y implies y ∼ x, and transitive if x ∼ y and y ∼ z imply x ∼ z. A
relation that is reflexive, symmetric, and transitive is called an equivalence
relation. Given an equivalence relation ∼, for each x ∈ S the equivalence
class of x is defined to be the set
[x]={y ∈S :y ∼x}.
The set of equivalence classes is denoted by S/∼.
Closely related to equivalence relations is the following notion: A parti-
tion of a set S is a collection C of disjoint nonempty subsets of S whose
union is S. In this situation one also says that S is the disjoint union of
the sets in C.
Exercise A.1. Given an equivalence relation ∼ on a set S, show that
the set S/∼ of equivalence classes is a partition of S. Conversely, given a
partitionofS,showthatthereisauniqueequivalencerelationwhosesetof
equivalence classes is exactly the original partition.
If r is any relation on a set S, the next exercise shows that there is a
“smallest” equivalence relation ∼ such that x(cid:28)r y =⇒ x∼y. It is called
the equivalence relation generated by r.
Exercise A.2. Let r ⊂ X ×X be any relation, and define ∼ to be the
intersection of all equivalence relations in X×X that contain r.
(a) Show that ∼ is an equivalence relation.

---

Set Theory 341
(b) Show that x ∼ y if and only if one of the following is true: x = y,
x(cid:10)r(cid:3)y, or there is a finite sequence of elements z1,…,zn ∈ X such
thatx(cid:10)r(cid:3)z1 (cid:10)r(cid:3)···(cid:10)r(cid:3)zn (cid:10)r(cid:3)y,wherex(cid:10)r(cid:3)y means“x(cid:10)r y ory(cid:10)r x.”
(See below for the formal definition of a finite sequence.)
Anotherparticularlyimportanttypeofrelationisapartialordering:This
is a relation ≤ on a set X that is reflexive, transitive, and antisymmetric,
which means that x ≤ y and y ≤ x together imply x = y. If in addition
everypairx,y ∈X satisfyeitherx≤y ory ≤x,itiscalledatotalordering
(orsometimesalinearorsimpleordering).Thenotationx<y isdefinedto
meanx≤yandx(cid:14)=y,andthenotationsx>yandx≥yhavetheobvious
meanings. If X is a set endowed with an ordering, one often says that X
is a (totally or partially) ordered set, with the ordering being understood
from the context.
The most common examples of totally ordered sets are number systems
such as the real numbers or the integers (which we will introduce formally
below). An important example of a partially ordered set is the set P(S) of
subsetsofagivensetS,withthepartialorderrelationdefinedbyinclusion:
X ≤Y ifandonlyifX ⊂Y.Itiseasytoseethatanysubsetofapartially
ordered set is itself partially ordered with (the restriction of) the same
order relation, and if the original ordering is total, then the subset is also
totally ordered.
If X is a partially ordered set and S ⊂ X is any subset, an element
x ∈ X is said to be an upper bound for S if x ≥ s for every s ∈ S. If
S has an upper bound, it is said to be bounded above. The terms lower
bound and bounded below are defined similarly. An element s ∈ S is said
to be maximal if there is no s(cid:5) ∈ S such that s(cid:5) > s, and it is the largest
element of S if s(cid:5) ≤s for every s(cid:5) ∈S. Minimal and smallest elements are
defined similarly. Clearly, the largest element of S, if it exists, is unique
and maximal. If S is totally ordered, a maximal element is automatically
largest; but in a partially ordered set this may not be the case, because
theremaybeelementsthatareneitherlargernorsmallerthans.Atotally
orderedsetX issaidtobewell-orderedifeverynonemptysubsetS ⊂X has
asmallestelement.Forexample,thesetofnaturalnumbersiswell-ordered,
but the integers and the real numbers are not.
A function from X to Y is a relation f ⊂ X × Y with the property
that for every x ∈ X there is a unique y ∈ Y such that (x,y) ∈ f. This
unique element of Y is denoted by f(x). The sets X and Y are called the
domainandrangeoff,respectively.Thewordsmapandmappingareused
synonymously for function.
The notation f: X → Y means “f is a function from X to Y” (or,
depending on how it is used in a sentence, “f, a function from X to Y,”
or “f, from X to Y”). The equation y = f(x) is also sometimes written
f: x (cid:10)→ y or, if the name of the function is not important, x (cid:10)→ y. Note
that the type of arrow ((cid:10)→) used to denote the action of a function on an

---

342 Appendix: Review of Prerequisites
element of its domain is different from the arrow (→) used between the
domain and range.
Given two functions f: X →Y and g: Y →Z, their composition is the
function g◦f: X →Z defined by (g◦f)(x)=g(f(x)).
For every set X, there exists a natural function Id : X → X called
X
the identity map of X, defined by f(x) = x for all x ∈ X. If S ⊂ X is a
subset, there is a function ι : S →X called the inclusion map of S, given
S
by ι (x) = x for x ∈ S. We sometimes use the notation ι : S (cid:9)→ X to
S S
emphasize the fact that it is an inclusion map. If f: X → Y and S is a
subsetofX,thereisafunctionf| : S →Y calledtherestrictionoff toS,
S
obtainedbyapplyingf onlytoelementsofS.Intermsoforderedpairs,f|
S
is just the subset of S×Y consisting of ordered pairs (x,y)∈f such that
x ∈ S. It is immediate that f| = f ◦ι , and ι is just the restriction of
S S S
Id to S. If g: S →Y is a map and f: X →Y is a map whose restriction
X
to S is equal to g, we say that f is an extension of g.
Let f: X → Y be a function. If S ⊂ X, the image of S under f is the
set
f(S)={y ∈Y :y =f(x) for some x∈S}.
The set f(X) ⊂ Y, the image of the entire domain X, is just called the
image of f. (Warning: In analysis it is common to use the word “range” to
denote what we call the image of a function, and the word “codomain” to
denote what we call its range.) If B is a subset of Y, the inverse image of
B, denoted by f−1(B), is the set
f−1(B)={x∈X :f(x)∈B}.
If B ={b} is a singleton, it is common to use the notation f−1(b) in place
of the more accurate but more cumbersome f−1({b}).
Exercise A.3. Let f: X →Y be a map.
(a) If A⊂B ⊂Y, then f−1(A)⊂f−1(B).
(b) If B ⊂Y, then f−1(Y (cid:3)B)=X(cid:3)f−1(B).
(c) Giveacounterexampletoshowthatitisnotgenerallytruethatf(X(cid:3)
A)=Y (cid:3)f(A) whenever A⊂X.
Thefunctionf issaidtobeinjectiveorone-to-oneiff(x)=f(y)implies
x = y. It is said to be surjective or to map X onto Y if f(X) = Y, or in
other words if every y ∈ Y is equal to f(x) for some x ∈ X. A function
that is both injective and surjective is said to be bijective or a one-to-
one correspondence. A bijective map from a set X to itself is also called a
permutation of X.
Given f: X →Y, if there exists a map g: Y →X such that f◦g =Id
Y
and g◦f = Id , then g is said to be an inverse for f. Since inverses are
X

---

Set Theory 343
unique (see the next exercise), the inverse map is denoted unambiguously
by f−1 when it exists. More generally, if g satisfies only g◦f = Id , it is
X
called a left inverse for f, and if f ◦g =Id , g is a right inverse for f.
Y
Lemma A.1. If f: X → Y is a function and X (cid:14)= ∅, then f has a left
inverse if and only if it is injective, and a right inverse if and only if it is
surjective.
Proof. Supposeg isaleftinversefor f.Iff(x)=f(x(cid:5)),applyingg toboth
sides implies x = x(cid:5), so f is injective. Similarly, if g is a right inverse and
y ∈Y is arbitrary, then f(g(y))=y, so f is surjective.
Now suppose f is injective. Choose any x0 ∈ X, and define g: Y → X
by g(y) = x if y ∈ f(X) and y = f(x), and g(y) = x0 if y (cid:14)∈ f(X). It
is immediate that g ◦ f = Id . The proof that surjectivity implies the
X
existence of a right inverse requires the axiom of choice, so we postpone it
until the end of the section (Exercise A.8).
Exercise A.4. Let f be a function.
(a) Show that f has an inverse if and only if it is bijective.
(b) If f has an inverse, show that it is unique.
Number Systems and Cardinality
So far, all the set-theoretic axioms we have introduced describe ways of
obtaining new sets from already existing ones. Before the theory will have
muchcontent,weneedtoknowthatsomesetsexist.Wetakethesetofreal
numbers as our starting point. The properties that characterize it are that
it is an ordered field (a field in the algebraic sense, endowed with a total
orderinginwhichy <z =⇒ x+y <x+z andx>0, y >0 =⇒ xy >0)
that is complete (every nonempty subset with an upper bound has a least
upper bound).
- Existence axiom: There exists a complete ordered field R, called
the real numbers.
Because this axiom guarantees the existence of at least one set, we now
can assert the existence of the empty set, since {x∈R:x(cid:14)=x}=∅.
Exercise A.5. Show that the real numbers are unique, in the sense that
anycompleteorderedfieldadmitsanorder-preservingisomorphismwithR.
Let S ⊂R be a nonempty subset with an upper bound. The least upper
bound of S is also called the supremum of S, and is denoted by supS.
Similarly, any nonempty set T with a lower bound has a greatest lower
bound, also called its infimum and denoted by infT.
We will work extensively with the usual subsets of R:

---

344 Appendix: Review of Prerequisites
- ThesetofnaturalnumbersN(thepositivecountingnumbers),defined
asthesmallestsubsetofRcontaining1andcontainingn+1whenever
it contains n.
- The set of integers Z={n∈R:n=0 or n∈N or −n∈N}.
- ThesetofrationalnumbersQ={x∈R:x=p/q for some p,q ∈Z}.
We consider the set C of complex numbers to be simply R×R, in which
therealnumbersareidentifiedwiththesubsetR×{0}⊂Candistandsfor
the imaginary unit (0,1). Multiplication and addition of complex numbers
aredefinedbytheusualruleswithi2 =−1;thusx+iy isanothernotation
for (x,y).
For any pair of integers m ≤ n, the notation {m,…,n} means {k ∈
Z : m ≤ k ≤ n}. For subsets of the real numbers, we use the following
notation:
[a,b]={x∈R:a≤x≤b},
(a,b)={x∈R:a<x<b},
[a,b)={x∈R:a≤x<b},
(a,b]={x∈R:a<x≤b}.
We also allow a or b or both to be replaced by either of the symbols ∞ or
−∞inanyoftheabovedefinitionsinwhichitmakessense,withtheobvious
meanings. A nonempty subset J ⊂ R is called an interval if whenever
a,b∈J, every c such that a<c<b is also in J.
Exercise A.6. Showthatanintervalmustbeoneoftheninetypesofsets
[a,b], (a,b), [a,b), (a,b], (−∞,b], (−∞,b), [a,∞), (a,∞), or (−∞,∞).
The natural numbers play a special role in set theory, as a yardstick for
measuring sizes of sets. Two sets are said to have the same cardinality if
there exists a one-to-one correspondence between them. A set is finite if
it is empty or has the same cardinality as {1,…,n} for some n ∈ N (in
which case it is said to have cardinality n), and otherwise it is infinite. A
set is countably infinite if it has the same cardinality as N, countable if it is
either finite or countably infinite, and uncountable otherwise. The sets N,
Z, and Q are countable, but R and C are not.
Exercise A.7.
(a) Prove that the union of a countable collection of countable sets is
countable.
(b) Prove that any subset of a countable set is countable.

---

Set Theory 345
Indexed Collections
Using what we have introduced so far, it is easy to extend the notion of
ordered pair. Given a natural number n and a set S, an ordered n-tuple
of elements of S is a function x: {1,…,n} → S. It is customary to write
x instead of x(i) for the value of x at i, and the whole n-tuple can be
i
written (x1,…,x
n
) or {x
i
:i=1,…,n} or {x
i
}n
i=1
. Similarly, a sequence
ofelementsofS isafunctionx: N→S,written{x1,x2,…}or{x
i
:i∈N}
or {x }∞ . An ordered n-tuple is sometimes called a finite sequence.
i i=1
A subsequence of a sequence {x i } i∈N in a set S is a sequence of the
form {x f(j) } j∈N, where f: N → N is a function that is strictly increasing,
meaning that i<j implies f(i)<f(j). We usually write i for f(j).
j
We sometimes need to deal with collections of objects that are indexed,
not by the natural numbers or subsets of them, but by arbitrary sets,
potentially even uncountable ones. An indexed collection of elements of S
isjustafunctionfromasetA(calledtheindexset)toS,andinthiscontext
is denoted by {x α : α ∈ A} or {x α } α∈A . Occasionally, when the index set
is understood or is irrelevant, we will omit it from the nota(cid:2)tion and simply
write {x α }. If {X α } α∈A is an indexed collection of sets, α∈A X α is just
another notation for the union of the (unindexed) collection{X ∈S :X =
X for some α∈A}, where S is the range of the indexing function. If the
α
index set is finite, the union is usu(cid:9)ally written as X1 ∪···∪X
n
. A similar
remark applies to the intersection
α∈A
X
α
or X1 ∩···∩X
n
.
Earlier we mentioned that given a set S and a partition of it, S is said
to be the disjoint union of the sets in the partition. It sometimes happens
thatwearegivenacollectionofsets,whichmayormaynotbedisjoint,but
which we want to consider as disjoint subsets of a larger set. For example,
we might want to form a set consisting of “five copies of R,” in which
we consider the different copies to be disjoint from each other. We can
accomplish this by the following trick. Suppose {X α } α∈A is an indexed
collection of nonempty sets. If we imagine “tagging” each element of X
α
with its index α, we can make the sets X and X disjoint when α (cid:14)= β,
α β
even if they were not disjoint to begin with. Formally, an element x with
a tag α is just an ordered pair (x,α(cid:6)). Thus we define the disjoint union of
the indexed collection, denoted by X , to be the set
α∈A α
(cid:17)
X ={(x,α):α∈A and x∈X }.
α α
α∈A
Iftheindexsetisfinite,thedisjointunionisusuallywrittenasX1(cid:6) (cid:20)···(cid:20)X
n
.
For each set X , there is a natural injective map ι : X → X ,
α α α α∈A α
given by ι (x) = (x,α). The images of these maps are disjoint from each
α
other, so we can identify each set X with its image under ι . In practice,
α α
we think of each X as a subset of the disjoint union and think of the
α
injection ι as an inclusion map. With this convention, this usage of the
α
term disjoint union is consistent with our previous one.

---

346 Appendix: Review of Prerequisites
The definition of Cartesian product now extends easily from two sets
to arbitrarily many. If (X1,…,X
n
) is an ordered n-tuple of sets, their
Cartesian product X1 × ··· × X
n
is just the set of all ordered n-tuples
(x1,…,x
n
) such that x
i
∈X
i
for i=1,…,n. (To be sure we are strictly
following the axioms, we should note that this is a subset of the set of all
functions from {1,…,n} to X1 ∪···∪X
n
, which in turn is a subset of the
power set of {1,…,n}×(X1 ∪···∪X
n
).) If X1 = ··· = X
n
= X, the
n-fold Cartesian product X×···×X is often written simply as Xn.
A Cartesian product comes equipped with projection maps π
i
: X1 ×
···×X
n
→ X
i
, defined by π
i
(x1,…,x
n
) = x
i
. It is easy to see that each
of these maps is surjective. If f: S →X1 ×···×X
n
is any function into a
Cartesian product, the composite functions f =π ◦f: S →X are called
i i i
its component functions. Any such function f is completely determined by
its component functions, by the formula
f(y)=(f1(y),…,f
n
(y)).
More generally, the Cartesian product of an arbitrary indexed (cid:2)collection
{X α } α∈A of sets is defined to be the set of all(cid:28)functions x: A→ α∈A X α
suchthatx ∈X foreachα.Itisdenotedby X .Justasinthecase
α α α∈A α
of finite pr(cid:28)oducts, any Cartesian product comes equipped with projection
maps π : X →X , defined by π (x)=x .
β α∈A α β β β
Our last set-theoretic axiom asserts that it is possible to choose an ele-
meant from each set in an arbitrary indexed collection.
- Axiomofchoice:Givenanynonemptyindexedc(cid:2)ollection{X
α
}
α∈A
of nonempty sets, there exists a function c: A → X , called a
α∈A α
choice function, such that c(α)∈X for each α.
α
In other words, the Cartesian product of any nonempty indexed collection
of nonempty sets is nonempty.
Here are two immediate applications of the axiom of choice.
Exercise A.8. Complete the proof of Lemma A.1 by showing that f is
surjective if and only if it has a right inverse.
Exercise A.9. If there exists a surjective map from a countable set onto
S, prove that S is countable.
The axiom of choice has a number of interesting equivalent reformula-
tions; the relationships among them make fascinating reading, for example
in [Hal74]. The only other formulations we will make use of are the follow-
ing two (the well-ordering theorem in Problem 4-6, and Zorn’s lemma in
the proof of Lemma 13.36).
Theorem A.2 (The Well-Ordering Theorem). Every set can be
given a total ordering that is well-ordered.

---

Metric Spaces 347
Theorem A.3 (Zorn’s Lemma). Let X be a partially ordered set in
which every totally ordered subset has an upper bound. Then X has a max-
imal element.
For proofs, see [Hal74] or [Dev93].
Metric Spaces
Metric spaces play an indispensable role in real analysis, and their proper-
ties provide the underlying motivation for most of the basic definitions in
topology. In this section we summarize the important properties of metric
spaces with which you should be familiar. For a thorough treatment of the
subject, see any good undergraduate real analysis text such as [Rud76].
Euclidean Spaces
Mostoftopology,inparticularmanifoldtheory,ismodeledonthebehavior
of Euclidean spaces and their subsets, so we begin with a quick review of
their properties.
The Cartesian product Rn = R×···×R of n copies of the real line is
known as n-dimensional Euclidean space. It is the set of ordered n-tuples
of real numbers. A point in Rn is denoted by (x1,…,x
n
) or simply x.
Thenumbersx arecalleditscomponentsorcoordinates.Zero-dimensional
i
Euclidean space R0 is, by convention, the singleton {0}.
WewillusewithoutfurthercommentthefactthatRnisann-dimensional
vector space with the usual operations of scalar multiplication and vector
addition. The geometric properties of Rn are derived from the Euclidean
·
dot product x y =x1y1+···+x
n
y
n
. In particular, the norm or length of
a vector x∈Rn is given by
(cid:12) (cid:13)
|x|=(x · x)1/2 = (x1)2+···+(x
n
)2 1/2 .
The angle between two nonzero vectors x,y is defined to be cos−1(x ·
y)/(|x||y|). Given two points x,y ∈ Rn, the line segment between them
is the set {tx+(1−t)y :0≤t≤1}.
Continuity and convergence in Euclidean spaces are defined in the usual
ways. A map f: U →V between subsets of Euclidean spaces is continuous
if for any x ∈ U and any ε > 0 there exists δ > 0 such that |x−y| < δ
implies |f(x)−f(y)| < ε. A sequence {x } of points in Rn converges to
i
x∈Rn ifforanyε>0thereexistsN suchthati≥N implies|x −x|<ε.
i
Metrics, Convergence, and Continuity
MetricspacesaregeneralizationsofEuclideanspaces,inwhichnoneofthe
vectorspacepropertiesarepresentandonlythedistancefunctionremains.

---

348 Appendix: Review of Prerequisites
If M is any set, a metric on M is a function d: M ×M →R, also called a
distance function, satisfying the following three properties:
(i) Symmetry: For all x,y ∈M, d(x,y)=d(y,x).
(ii) Positivity:Forallx,y ∈M,d(x,y)≥0,and(x,y)=0ifandonly
if x=y.
(iii) Triangleinequality:Forallx,y,z ∈M,d(x,z)≤d(x,y)+d(y,z).
Thepair(M,d)iscalledametric space.(Actually,unlessitisimportantto
specify which metric is being considered, we often just say “M is a metric
space,” with the metric being understood from the context.)
Example A.4.
(a) If M is any subset of Rn, the function d(x,y) = |x−y| is a metric
on M (Exercise A.10), called the Euclidean metric. Whenever we
considerasubsetofRn asametricspace,unlesswespecifyotherwise
it will always be with the Euclidean metric.
(b) Similarly, if M is any metric space and X is a subset of M, then X
inherits a metric simply by restricting the distance function of M to
points in X.
(c) If X is any set, define a metric on X by setting d(x,y) = 1 unless
x=y, in which case d(x,y)=0. This is called the discrete metric on
X.
Exercise A.10. Prove that d(x,y)=|x−y| is a metric on any subset of
Rn.
Here are some of the standard definitions used in metric space theory.
Let M be a metric space.
- For any x∈M and r >0, the (open) ball of radius r around x is the
set
B (x)={y ∈M :d(y,x)<r},
r
and the closed ball of radius r around x is
B (x)={y ∈M :d(y,x)≤r}.
r
- Given a subset A⊂M, a point x∈M is said to be a limit point (or
accumulation point or cluster point) of A if every open ball around x
contains a point of A other than x.
- A set A ⊂ M is said to be open if it contains an open ball around
each of its points.

---

Metric Spaces 349
- A set A⊂M is said to be closed if it contains all its limit points.
- The diameter of a set A ⊂ M is sup{d(x,y) : x,y ∈ A} (which may
be infinite).
- A set A⊂M is said to be bounded if it has finite diameter.
Exercise A.11. Let M be a metric space.
(a) Show that A⊂M is open if and only if M (cid:3)A is closed.
(b) ShowthatanopenballinM isanopenset,andaclosedballinM is
a closed set.
(c) Show that the union of an arbitrary collection of open sets is open,
and the intersection of finitely many open sets is open.
(d) Show that the intersection of an arbitrary collection of closed sets is
closed, and the union of finitely many closed sets is closed.
(e) ShowthatasubsetofM isboundedifandonlyifitiscontainedinan
open ball if and only if it is contained in a closed ball.
Exercise A.12. In each part below, a subset S of a metric space M is
given. In each case, decide whether S is open, closed, both, or neither.
(a) M =R, and S =[0,1).
(b) M =R, and S =N.
(c) M =Z, and S =N.
(d) M =R2, and S is the set of points with rational coordinates.
(e) M =R2, and S is the unit disk {(x,y)∈R2 :x2+y2 <1}.
(f) M =R3,andSistheunitdisk{(x,y,z)∈R3 :z=0 and x2+y2 <1}.
(g) M ={(x,y)∈R2 :x>0 and y>0},andS ={(x,y)∈M :x2+y2 ≤
1}.
The definition of continuity in the context of metric spaces is a straight-
forwardgeneralizationoftheEuclideandefinition.If(M1,d1)and(M2,d2)
are metric spaces, a map f: M1 → M2 is said to be continuous if for ev-
ery x ∈ M1 and every ε > 0, there exists δ > 0 such that d1(x,y) < δ
implies d2(f(x),f(y)) < ε. Similarly, if {x
i
} is a sequence of points in a
metric space (M,d), it is said to converge to x ∈ M, written x → x or
i
lim i→∞x
i
= x, if for any ε > 0 there exists N such that i ≥ N implies
d(x ,x)<ε.
i
Exercise A.13. If M and N are metric spaces and f: M →N is a map,
show that f is continuous if and only if it takes convergent sequences to
convergent sequences, i.e., if and only if xi →y in M implies f(xi)→f(y)
in N.

---

350 Appendix: Review of Prerequisites
Exercise A.14. ShowthatasubsetAofametricspaceM isclosedifand
onlyif,whenever{xi }isasequenceofpointsinAthatconvergesinM,the
limit lies in A.
Asequence{x }inametricspaceissaidtobeCauchyifforeveryε>0,
i
there exists N such that i,j ≥ N implies d(x ,x ) < ε. Every convergent
i j
sequenceisCauchy(ExerciseA.15),buttheconverseisnottrueingeneral.
A metric space in which every Cauchy sequence converges is said to be
complete.
Exercise A.15. Prove that every convergent sequence in a metric space
is Cauchy.
The following criterion for continuity is frequently useful (and in fact,
as is explained in Chapter 2, is the main motivation for the definition of a
topological space).
Lemma A.5 (Open Set Criterion for Continuity). A map
f: M1 → M2 between metric spaces is continuous if and only if the
inverse image of every open set is open: Whenever U is an open subset of
M2, f−1(U) is open in M1.
Exercise A.16. Prove Lemma A.5
Compactness
Let M be a metric space and K a subset of M. An open cover of K is
a collection {U α } α∈A of open subsets of M whose union contains K. A
subcover is a subcollection that is still an open cover of K. A subset of M
is said to be compact if every open cover has a finite subcover.
Two properties of compact sets—closedness and boundedness—follow
immediately from the definition.
Proposition A.6. Any compact subset of a metric space is closed and
bounded.
Proof. LetK ⊂M becompact,andletxbeanypointinK.Thecollection
of open balls {B (x):r >0} is an open cover of K, which therefore must
r
haveafinitesubcover.LettingRbetheradiusofthelargestofthesefinitely
many balls, it follows that K ⊂B (x), which means that it is bounded.
R
ToshowthatK isclosed,wewillshowthatitscomplementisopen.Letq
beanypointofM(cid:3)K.Foreachp∈K,letδ(p)=d(p,q)/2;thentheballs
B δ(p)(q) and B δ(p)(p) are disjoint by the triangle inequality. The collection
{B δ(p)(p) : p ∈ K} is an open cover of K, and therefore has a finite sub-
cover, say {B δ(p1)(p1),…,B δ(pk )(p k )}. Now let r =min{δ(p1),…,δ(p k )}.
Since B r (q) is disjoint from each of the balls B δ(pi )(p i ) and these balls
cover K, it is disjoint from K. In other words, there is a ball around each
q ∈M(cid:3)K containedinM(cid:3)K,soM(cid:3)K isopenandthusK isclosed.

---

Metric Spaces 351
In Rn, the converse of this proposition is true. Before proving this result
(the Heine–Borel theorem below), we need a preliminary lemma.
For any point x∈Rn and any r >0, the closed cube of side r around x
is the set
C (x)={y ∈Rn :|x −y |≤r/2, i=1,…,n}.
r i i
√
It is easy to check that the diameter of C (x) is r n.
r
Lemma A.7. Suppose {C
i
}∞
i=1
is a sequence of c(cid:9)losed cubes in Rn that
are nested, in the sense that C1 ⊃C2 ⊃···. Then
k
C
k
is not empty.
Proof. First consider the case n = 1, in which case the cubes are just
closed intervals. Writing the intervals as C = [a ,b ], the fact that they
k k k
are nested means that a1 ≤ a2 ≤ ··· ≤ a k < b k ≤ b k−1 ≤ ··· ≤ b2 ≤ b1.
Let a = sup{a
k
} and b = inf{b
k
}. Then clearly, a
k
≤ a ≤ b ≤ (cid:9)b
k
for each
k, so the interval [a,b] (or the point a if a=b) is contained in C .
k k
Forgeneraln,justapplytheprecedingargumenttoeachcoordinate.
Theorem A.8 (The Heine–Borel Theorem). Every closed and
bounded subset of Rn is compact.
Proof. We begin by showing that any closed cube in Rn is compact. Let
C be a closed cube of side r, and let U be an open cover of C. Suppose
U has no finite subcover. Subdividing each of the sides of C in half yields
a decomposition of C into 2n closed cubes of side r/2 whose union is C.
If each of these 2n cubes were covered by finitely many sets of U, then
putting together these 2n finite collections of open sets would give a finite
subcover of C; thus at least one of them must not be covered by any finite
subcollection of sets from U. Call this smaller cube C1. If we subdivide C1
in the same way, one of the 2n cubes in this subdivision must not admit a
finite subcover by the same reasoning. Continuing by induction, we obtain
a nested sequence of cubes C = C0 ⊃ C1 ⊃ ··· with the property that no
C iscoveredbyanyfinitecollectionofsetsfromU.EachcubeC hasside
k k
length r/2k. (cid:9)
By Lemma A.7, there is a point x∈ C . Because U is a cover of C, x
k k
must be in one of the sets of U, say x∈U0.√Because U0 is open, there is a
ball B
ε
(x)⊂U0. Because C
k
has diameter r n/2k and x∈C
k
, as soon as
k is sufficiently large C
k
⊂B
ε
(x)⊂U0, which contradicts the fact that C
k
cannot be covered by finitely many sets of U. This proves that any cube is
compact.
Now suppose K ⊂ Rn is any closed and bounded subset. Because it is
bounded, it is contained in some cube C (0). If U is an open cover of K,
r
thecollectionU∪{Rn(cid:3)K}isanopencoverofC (0).(Hereweusethefact
r
that K is closed.) Finitely many of these sets, say {U1,…,U
m
,Rn(cid:3)K},
cover C
r
(0), and then it is clear that {U1,…,U
m
} cover K.

---

352 Appendix: Review of Prerequisites
TheHeine–BoreltheoremisnottrueifRn isreplacedbyageneralmetric
space, as the following exercise shows.
Exercise A.17.
(a) In Z with the discrete metric, show that any infinite subset is closed
and bounded, but not compact.
(b) Similarly,inthemetricspace(0,∞),showthattheset(0,1]isclosed
2
andbounded,buttheopencoverofitbyintervalsoftheform(1/n,1)
for n∈N has no finite subcover.
Most of the applications of compactness depend on the following theo-
rem.
Theorem A.9. If M and N are metric spaces, f: M →N is continuous,
and K ⊂M is compact, then f(K) is compact.
Exercise A.18. Prove Theorem A.9.
Forexample,thefollowingtheoremisoffundamentalimportanceinreal
analysis.
Theorem A.10 (Euclidean Extreme Value Theorem). Anycontin-
uous real-valued function on a closed and bounded subset of Rn attains its
maximum and minimum values.
Proof. Letf: K →Rbesuchafunction.SinceK isclosedandbounded,it
iscompactbytheHeine–Boreltheorem.Bytheprecedingtheorem,f(K)is
compact and therefore closed and bounded in R. In particular, it contains
its supremum and infimum.
Group Theory
Wewillassumeonlybasicgrouptheorysuchasoneislikelytoencounterin
mostundergraduatealgebracourses.Youcanfindmuchmoredetailabout
all of this material in, for example, [Hun90] or [Her75].
Basic Definitions
A group is a set G together with a map G×G→G, usually called multi-
plication and written (g,h)(cid:10)→gh, satisfying
(i) Associativity: For all g,h,k ∈G, (gh)k =g(hk).
(ii) Existence of identity: There is an element 1∈G such that 1g =
g1=g for all g ∈G.

---

Group Theory 353
(iii) Existence of inverses: For each g ∈G, there is an element h∈G
such that gh=hg =1.
TheorderofagroupGisitscardinalityasaset.Thetrivial groupisthe
uniquegroupoforder1;itisthegroupconsistingoftheidentityalone.One
checkseasilythattheinverseofanyelementisunique(sotheusualnotation
g−1 for inverses makes sense), and that (gh)−1 = h−1g−1. Similarly, the
identity is unique.
A group G is said to be abelian if gh = hg for all g,h ∈ G. The group
operation in an abelian group is frequently written additively, (g,h) (cid:10)→
g+h, in which case the identity element is denoted by 0 and the inverse
of g is denoted by −g.
AsubsetofGthatisitselfagroupwiththesamemultiplicationiscalled
a subgroup of G. Clearly, a subset is a subgroup if and only if it is closed
under multiplication and contains the inverse of each of its elements.
IfS isanyset,thesetofpermutationsofS isagroupundercomposition,
called the permutation group of S. In particular, if S is a finite set, any
permutation of S can be factored as a product of transpositions, which
are permutations that interchange two elements and leave all others fixed.
The factorization into transpositions is not uniquely determined, but the
parity (evenness or oddness) of the number of transpositions is the same
foreverysuchfactorization.Apermutationiscalledevenorodddepending
on whether it decomposes into an even or odd number of transpositions.
Exercise A.19. Let Sn denote the group of permutations of the set
{1,…,n}, called the symmetric group on n elements.
(a) Show that the map sgn: Sn →{±1} given by
(cid:16)
+1 if s is even,
sgn(s)=
−1 if s is odd
is a surjective homomorphism. (Here we consider {±1} as a group
under multiplication.)
(b) Show that every element of Sn can be written as a product of trans-
positions of the following type:
sk(k)=k+1;
sk(k+1)=k;
sk(i)=i if i(cid:13)=k or k+1.
If G1,…,G
n
are groups, their direct product is the set G1 ×···×G
n
with the group structure defined by the multiplication law
(g1,…,g
n
)(g
1
(cid:5),…,g
n
(cid:5))=(g1g
1
(cid:5),…,g
n
g
n
(cid:5))
and with identity element (1,…,1). More generally, the direct product of
ana(cid:28)rbitraryindexedcollectionofgroups{G α } α∈A istheCartesianproduct
set G with multiplication defined componentwise: (gg(cid:5)) =g g(cid:5) .
α∈A α α α α

---

354 Appendix: Review of Prerequisites
A map f: G → H between groups is called a homomorphism if it pre-
servesmultiplication:f(gh)=f(g)f(h).Theimageoff isf(G)⊂H,often
writtenImf,anditskernelisthesetf−1(1),denotedbyKerf.Abijective
homomorphism is called anisomorphism. An isomorphism fromG to itself
is called an automorphism.
Exercise A.20. Let f: G→H be a homomorphism.
- Show that f is injective if and only if Kerf ={1}.
- If f is bijective, show that f−1 is also a homomorphism.
- Show that the image and the kernel of f are subgroups.
- If K ⊂G is a subgroup, show that f(K) is a subgroup of H.
An element g ∈ G defines a map C : G → G by C (h) = ghg−1. This
g g
map, called conjugation by g, is easily seen to be an automorphism of G,
so the image under C of any subgroup H ⊂ G (written symbolically as
g
gHg−1) is another subgroup of G. Two subgroups H,H(cid:5) are conjugate if
H(cid:5) =gHg−1 for some g ∈G.
Exercise A.21. Showthatconjugacyisanequivalencerelationontheset
of all subgroups of G.
The set of subgroups conjugate to a given subgroup H ⊂G is called the
conjugacy class of H.
Cosets and Quotient Groups
Given a subgroup H ⊂ G and an element g ∈ G, the left coset of H
determined by g is the set
gH ={gh:h∈H}.
The right coset Hg is defined similarly. Define a relation called congruence
modulo H by declaring that g ≡g(cid:5) (mod H) if and only if g−1g(cid:5) ∈H.
Exercise A.22. Show that congruence modulo H is an equivalence rela-
tion on G, and its equivalence classes are precisely the left cosets of H.
The set of left cosets of H in G is denoted by G/H. (This is just the
partition of G defined by congruence modulo H.) The cardinality of G/H
is called the index of H in G.
A subgroup K ⊂ G is said to be normal if it is invariant under all
conjugations, that is if gKg−1 = K for all g ∈ G. Clearly, every subgroup
of an abelian group is normal.
Exercise A.23. Show that a subgroup K ⊂ G is normal if and only if
gK =Kg foreveryg∈G,sothateveryleftcosetofK isalsoarightcoset.

---

Group Theory 355
Exercise A.24. Show that the kernel of any homomorphism is a normal
subgroup.
Normal subgroups give rise to one of the most important constructions
in group theory. Given a normal subgroup K ⊂G, define a multiplication
operator on the set G/K of left cosets by
(gK)(g(cid:5)K)=(gg(cid:5))K.
Lemma A.11. This multiplication is well-defined on cosets and turns
G/K into a group.
Proof. First we need to show that the product does not depend on the
representatives chosen for the cosets: If gK = g(cid:5)K and hK = h(cid:5)K, then
(gh)K =(g(cid:5)h(cid:5))K.FromExerciseA.22,thefactthatg andg(cid:5) determinethe
same coset means that g−1g(cid:5) ∈K, which is the same as saying g(cid:5) =gk for
somek ∈K.Similarly,h(cid:5) =hk(cid:5) fork(cid:5) ∈K.BecauseK isnormal,h−1khis
an element of K. Writing this element as k(cid:5)(cid:5), we have kh=hk(cid:5)(cid:5). It follows
that
g(cid:5)h(cid:5) =gkhk(cid:5) =ghk(cid:5)(cid:5)k(cid:5),
which shows that g(cid:5)h(cid:5) and gh determine the same coset.
Now we just note that the group properties are satisfied: Associativity
of the multiplication in G/K follows from that of G; the element 1K =K
of G/K acts as an identity; and g−1K is the inverse of gK.
WhenK isanormalsubgroupofG,thegroupG/K iscalledthequotient
groupofGbyK.Thenaturalprojectionmapπ: G→G/K thatsendseach
element to its coset is a surjective homomorphism whose kernel is K.
Thefollowinglemmatellshowtodefinehomomorphismsfromaquotient
group.
Lemma A.12. Let K ⊂ G be a normal subgroup. Given a homomor-
phism f: G → H such that K ⊂ Kerf, there is a unique homomorphism
f (cid:7) : G/K →H such that the following diagram commutes:
f(cid:2)
G H
(cid:3)(cid:4)
π (cid:3)f (cid:7)
(cid:5)(cid:3)
G/K. (A.1)
(A diagram such as (A.1) is said to commute, or to be commutative, if
the maps between two spaces obtained by following arrows around either
side of the diagram are equal. So in this case commutativity means that
f
(cid:7)◦π
=f.)

---

356 Appendix: Review of Prerequisites
Proof. Since π(g) = gK, if such a map exists, it has to be given by the
(cid:7)
formula f(gK)=f(g); this proves uniqueness. To prove existence, we just
(cid:7)
define f by this formula, so it obviously makes the diagram commute. It is
well-defined,becauseifg ≡g(cid:5) (mod K),theng(cid:5) =gk forsomek ∈K,and
therefore f(g(cid:5)) = f(gk) = f(g)f(k) = f(g). It is clear from the definition
of multiplication in G/K that it is a homomorphism.
Inthesituationoftheprecedinglemma,wesaythatthehomomorphism
f passes to the quotient or descends to the quotient.
The most important fact about quotient groups is the following result,
whichsaysinessencethattheprojectionontoaquotientgroupisthemodel
for all surjective homomorphisms.
Theorem A.13 (First Isomorphism Theorem). Let G,H be groups,
and let f: G → H be a surjective homomorphism. Then K = Kerf is a
normal subgroup of G, and f induces an isomorphism f (cid:7) : G/K → H by
(cid:7)
f(gK)=f(g).
(cid:7)
Proof. Fromtheprecedinglemma,f(gK)=f(g)definesahomomorphism
f (cid:7) : G/K →H.Becausef issurjective,f (cid:7) issurjective:Foranyh∈H there
is an element g ∈ G with f(g) = h, and then f (cid:7) (gK) = h. To show that f (cid:7)
is injective, suppose 1 = f (cid:7) (gK) = f(g). This means that g ∈ Kerf = K,
so gK =K is the identity element of G/K.
Exercise A.25. Suppose f: G → H is a surjective homomorphism, and
K ⊂G is a normal subgroup. Show that f(K) is normal in H.
Cyclic Groups
Let G be a group and g ∈ G. The set (cid:22)g(cid:23) = {gn : n ∈ Z} is obviously
a subgroup of G, called the cyclic subgroup generated by g. The group G
is said to be cyclic if G = (cid:22)g(cid:23) for some element g ∈ G. In this case, the
element g is called a generator of G.
Example A.14 (Cyclic Groups).
(a) The group Z of integers (under addition) is an infinite cyclic group
generated by 1.
(b) Foranyn∈Z,thecyclicsubgroup(cid:22)n(cid:23)isnormalbecauseZisabelian.
The quotient group Z/(cid:22)n(cid:23) is called the group of integers modulo n.
It is easily seen to be a cyclic group of order n, with the coset of 1 as
a generator.
Exercise A.26. Show that any infinite cyclic group is isomorphic to Z
and any finite cyclic group is isomorphic to Z/(cid:8)n(cid:9), where n is the order of
the group.

---

Group Theory 357
Exercise A.27. Show that every subgroup of a cyclic group is cyclic.
Exercise A.28. If G is a cyclic group and f: G → G is any homomor-
phism, show there is an integer n such that f(γ)=γn for all γ ∈G. If G is
infinite, show that n is uniquely determined by f.

---

References
[Dev93] Keith Devlin. The Joy of Sets: Fundamentals of Contemporary
Set Theory. Springer-Verlag, New York, second edition, 1993.
[DH07] MaxDehnandPoulHeegaard. Analysissitus. Enzyklop¨adie der
Math. Wiss., III.1.1:153–220, 1907.
[Die89] Jean Dieudonn´e. A History of Algebraic and Differential Topol-
ogy 1900–1960. Birkh¨auser Boston, Cambridge, 1989.
[Fre82] Michael Hartley Freedman. The topology of four-dimensional
manifolds. J. Differential Geom., 17:357–453, 1982.
[Hal74] Paul R. Halmos. Naive Set Theory. Springer-Verlag, New York,
1974.
[Her75] Israel N. Herstein. Topics in Algebra. Wiley, New York, second
edition, 1975.
[Hun90] Thomas W. Hungerford. Abstract Algebra: An Introduction.
Saunders College Publishing, Philadelphia, 1990.
[Lee97] John M. Lee. Riemannian Manifolds: An Introduction to Cur-
vature. Springer-Verlag, New York, 1997.
[LMM94] Silvio Levy, Delle Maxwell, and Tamara Munzer. Outside in.
The Geometry Center (video), 1994.

---

360 References
[Mas89] William S. Massey. Algebraic Topology: An Introduction.
Springer-Verlag, New York, 1989.
[Max77] Nelson Max. Turning a sphere inside out. International Film
Bureau (video), 1977.
[Moi77] Edwin E. Moise. Geometric Topology in Dimensions 2 and 3.
Springer-Verlag, New York, 1977.
[Mun75] James R. Munkres. Topology: A First Course. Prentice–Hall,
Englewood Cliffs, New Jersey, 1975.
[Mun84] James R. Munkres. Elements of Algebraic Topology. Addison–
Wesley, Reading, Massachusetts, 1984.
[Rad25] Tibor Rado´. U¨ber den Begriff der Riemannschen Fla¨che. Acta
Litt. Sci. Szeged., 2:101–121, 1925.
[Ran96] A. A. Ranicki. On the Hauptvermutung. In A. A. Ranicki,
editor,TheHauptvermutungBook,volume1ofK-Monographsin
Mathematics, pages 3–31. Kluwer Acad. Publ., Dordrecht, 1996.
[Rud76] Walter Rudin. Principles of Mathematical Analysis. McGraw-
Hill, New York, third edition, 1976.
[Sco83] PeterScott. Thegeometriesof3-manifolds. Bull. London Math.
Soc., 15:401–487, 1983.
[SFL98] John M. Sullivan, George Francis, and Stuart Levy. The opti-
verse. NationalCenterforSupercomputingApplications(video),
1998.
[Sie92] Allan J. Sieradski. An Introduction to Topology and Homotopy.
PWS-Kent, Boston, 1992.
[Sma58] StephenSmale. Aclassificationofimmersionsofthetwo-sphere.
Trans. Amer. Math. Soc., 90:281–290, 1958.
[Sma61] Stephen Smale. Generalized Poincar´e conjecture in dimensions
greater than 4. Ann. Math., 74:391–406, 1961.
[Spa89] Edwin H. Spanier. Algebraic Topology. Springer-Verlag, New
York, 1989.
[Sti82] JohnStillwell. Thewordproblemandtheisomorphismproblem
for groups. Bull. Amer. Math. Soc. (N.S.), 6:33–56, 1982.
[Sti93] John Stillwell. Classical Topology and Combinatorial Group
Theory. Springer-Verlag, New York, second edition, 1993.

---

References 361
[Thu97] WilliamP.Thurston. Three-dimensional geometry and topology,
volume 1. Princeton University Press, Princeton, 1997.
[Whi78] George W. Whitehead. Elements of Homotopy Theory.
Springer-Verlag, New York, 1978.

---

Index
AB (category of abelian groups), proper, 266
171 right, 59
abelian transitive, 60
group, 203, 353 affine
free, 204 chain, 293
groups, category of, 171 hyperplane, 92
Lie group, 11 map, 92
abelianization, 227 singular simplex, 293
characteristic property, 227 subspace, 92
functor, 231 algebra, fundamental theorem
of fundamental groups of of, 191
surfaces, 228 algebraic geometry, 11
uniqueness, 231 algebraic topology, 6
absolute value, 20 algebraic variety, 12
abstract simplex, 96 algebraically closed, 11
abstract simplicial complex, 96 algorithm, reduction, 196
accumulation point, 26, 348 ambient Euclidean space, 17
action analysis situs, 4
continuous, 60 angle, 7, 347
free, 60 function, for a path in S1,
left, 59, 266 179, 182
of a group, 59, 266 angle-sum theorem, 7
quotient by, 61 antipodal map, 248, 321
of fundamental group on degree of, 321
fiber, 245 homotopic to identity, 322

---

Index 363
antisymmetric relation, 341 for metric topology, 29
area, 7 for product topology, 48, 50
associative, 352 for subspace topology, 42
associativity of path class for trivial topology, 29
product, 153 in a set, 27
automorphism group of covering, neighborhood, 32
248 countable, 32
automorphism of covering, 248 of Euclidean balls, 38
automorphism of group, 354 standard, for Zn, 204
axiom topology generated by, 27
Cartesian product, 340 belongs to a set, 338
existence, 343 Betti number, 328
of choice, 346 big crunch, 14
power set, 339 bijective, 342
specification, 338 body, rigid, 13
union, 339 bound
axioms for set theory, 338–347 lower, 341
upper, 341
Bn (unit ball in Rn), 22 boundary, 25, 26
Baire category theorem, 85 face, 93
ball manifold with, 34
closed, 348 of a boundary, 294
is a closed set, 349 simplicial, 323
is a manifold with of a manifold with
boundary, 62 boundary, 34, 38
Euclidean, 31 of a simplex, 93
regular, 83 of a singular simplex, 293
open, 348 operator, 297
is an open set, 349 simplicial, 323
unit, in Rn, 22 singular, 293
barycenter, 110 simplicial, 324
barycentric subdivision, 110, 315 singular, 294
base of covering, 234 topological, 35
base point, 151 bounded
change of, 154 above, 341
nondegenerate, 212 below, 341
based at a point, 151 not a topological property,
basis 22
and continuity, 29 set, 349
countable, 32 bouquet of circles, 55
criterion, 27 branch, 9
for a topology, 29 Brouwer fixed point theorem,
for discrete topology, 29 192, 334
for Euclidean topology, 29
for free abelian group, 204 C (set of complex numbers), 344

---

364 Index
CPn (complex projective space), abelianization, 227
62 disjoint union topology, 62
Calabi–Yau manifold, 15 free abelian group, 204
cardinality, 344 free group, 200
of fibers of covering, 236, free product, 198
247 product topology, 49
Cartesian coordinates, 3 quotient topology, 56
Cartesian product, 340, 346 subspace topology, 41
axiom, 340 characteristic zero, 330
finite, 346 characterization of quotient
infinite, 346 maps, 57
category, 170 chart, 31
first, 86 coordinate, 31
homotopy, 173 on a manifold with
of abelian groups, 171 boundary, 34
of commutative rings, 171 choice function, 346
of complex vector spaces, choice, axiom of, 346
171 circle, 2, 45
of groups, 171 as coset space of R, 61
of real vector spaces, 171 fundamental group, 180
of rings, 171 generating, 45
of sets, 171 homotopy lifting property,
of simplicial complexes, 171 181
of topological spaces, 171 path lifting property, 181
pointed homotopy, 173 representative, 157
second, 86 unique lifting property, 181
theorem, Baire, 85 unit, 45
Cauchy sequence, 350 class, 339
vs. convergent sequence, 350 equivalence, 340
center of a group, 208 classical mechanics, 12
center of gravity, 110 classification
chain of 1-manifolds, 118
affine, 293 of 2-manifolds, 6, 137, 229
complex, 297 of 3-manifolds, 7
homology groups of, 297 of n-manifolds, 7
group of coverings, 283
simplicial, 323 of manifolds, 6
singular, 293 of surface presentations, 137
homotopic, 303 of surfaces, 6, 137, 229
homotopy, 303, 317 of torus coverings, 286
map, 297 closed
simplicial, 323 ball, 348
singular, 293 is a closed set, 349
change of base point, 154 is a manifold with
characteristic property boundary, 62

---

Index 365
cube, 351 equivalence, 112
map, 27 group theory, 203
lemma, 79 invariant, 113, 142
product of, 62 Euler characteristic, 113,
vs. homeomorphism, 27 142
set, 24, 26 orientability, 115
and continuity, 25 commutative diagram, 355
and limit points, 26 commutative rings, category of,
in a compact space, 74 171
in a discrete space, 25 commutator subgroup, 227
in a metric space, 349 compact
in a subspace, 41 implies closed and bounded,
intersection, in a metric 350
space, 349 limit point, 76
intersection, in a locally, 81
topological space, 24 relatively, 82
union, in a metric space, sequentially, 77
349 set
union, in a topological continuous image, 73, 352
space, 24 in a Hausdorff space, 74
closure, 25, 26 in a metric space, 350
and sequences, 38 topological space, 73
normal, 201 product of, 74
cluster point, 26, 348 quotient of, 74
coboundary, 329 vs. limit point compact, 77,
operator, 329 78
cochain vs. sequentially compact, 78
complex, 329 compactification, one-point, 89
map, 330 complement, 339
singular, 329 complementary edge pair, 139
cocycle, 329 complete
codomain, 342 metric space, 350
coffee cup, 5 ordered field, 343
coherent topology, 99 complex
of finite union, 114 analysis, 8
cohomology analytic, 8
functor, 330 chain, 297
Mayer–Vietoris sequence, general linear group, 10
335 manifold, 33
singular, 329 numbers, 344
topological invariance, 330 projective space, 12, 62
with field coefficients, 331, simplicial
332 abstract, 96
collection, 338 category of, 171
combinatorial Euclidean, 93

---

366 Index
special linear group, 11 constant loop, 151
vector spaces, category of, constant map, continuity of, 21
171 continuity
component, 70, 347 and closed sets, 25
functions, 346 and convergent sequences,
is closed, 71 38, 349
of ordered pair, 340 at a point, 21
path, 72 between Euclidean spaces,
composition, 342 347
continuity of, 20, 21 between metric spaces, 349
in a category, 170 between topological spaces,
of quotient maps, 53 20
cone, 110 in terms of basis, 29
on an affine simplex, 315 local criterion, 21
conformal, 273 of composition, 20, 21
congruence modulo a subgroup, of constant map, 21
354 of identity map, 21
conjugacy class, 354 of restriction, 21
conjugacy theorem, 243 open set criterion, 350
conjugate subgroups, 354 continuous, see continuity
conjugation, 354 continuous deformation, 4
connected continuous group action, 60
edge path, 101 continuous image
interval, 68 of compact set, 73
locally, 72 of connected set, 67
locally path, 72 continuous map induced by a
product space, 67 simplicial map, 99
quotient space, 67 contractible space, 161
simply, 156 is simply connected, 162
space, 65 singular homology of, 303
subset, 66 contravariant functor, 172
of R, 68 convergent sequence
sum, 126 in a metric space, 349
covering of, 253 in a topological space, 20
is a manifold, 126 in Euclidean space, 347
polygonal presentation, is Cauchy, 350
136 vs. continuity, 38, 349
with sphere, 129 convex, 69
connecting homomorphism, 309, hull, 92
310 set, 176
naturality, 312 homeomorphic to ball, 80
connectivity relation, 70 simply connected, 156
path, 71 coordinate, 347
consistent orientations, 107 coordinate chart, 31
consolidating, 134 corners, 23

---

Index 367
correspondence, one-to-one, 342 of lens space, 286
coset of manifold, 253
left, 354 of projective space, 235, 253
multiplication of, 355 of torus, 270, 286
right, 354 space, 234
space, 61 universal, 261
countable transformation, 248
basis, 32 uniqueness, 260
dense subset, 38 universal, 261
of Rn, 27 crease, 5
first, 32 CRING (category of commutative
neighborhood basis, 32 rings), 171
second, 32 crunch, big, 14
set, 344 cube, 4
subcover, 32 closed, 351
subset, 344 nested, 351
union, 344 open, 29
countably infinite, 344 cubical surface, 23
counterclockwise, 107 cup, coffee, 5
covariant functor, 172 curvature, 7
cover, 32 curve, 2, 117
open, 32, 73 classification, 118
in a metric space, 350 plane, 2
of a subset, 73 space, 2
covering space-filling, 188
cardinality of fibers, 236, cusp, 11
247 cutting, 134
classification, 283 cycle
group, 248 in a graph, 163
structure theorem, 250 simplicial, 324
transitivity, 249 singular, 294
homomorphism, 258 cyclic group, 356
criterion, 260 homomorphism, 357
is a covering map, 258 infinite, 200
isomorphism, 258 cyclic subgroup, 356, 357
isomorphism theorem, 260 cylinder, 3
map, 234 mapping, 167
classification, 283
is a local ∂, see boundary
homeomorphism, 235 deck transformation, 248
is a quotient map, 235 deformation, 148
is open, 235 continuous, 4
product of, 253 retract, 161
of connected sum, 253 strong, 161
of Klein bottle, 253 retraction, 161

---

368 Index
and homotopy distance function, 348
equivalence, 166 divisible group, 335
strong, 161 domain, 341
degree of a map, 191, 320 dot product, 347
homological, 320 doughnut surface, 3, 5, 45
homotopic, 320 homeomorphic to torus, 51,
degrees of freedom, 2 80
Dehn, Max, 137, 203 dual
dense, 26 map, 173
nowhere, 85 space, 173
descending to the quotient, 56, dynamical system, 13
57
homomorphism, 356 ε (exponential quotient map),
diagonal, 62 61, 179, 235
diagram, commutative, 355 edge
diameter, 76, 349 of a presentation, 131
difference of sets, 339 of a simplex, 93
dimension, 1 pairing transformation, 274
of a Euclidean simplicial path, 101
complex, 94 connected, 101
of a manifold, 33 periodic, 119
of a simplex, 92 reduced, 101
of a simplicial complex, 334 point, 124
of an abstract simplex, 96 Einstein, Albert, 14
of an abstract simplicial field equations, 14
complex, 96 general relativity, 14
of an affine subspace, 92 element of a set, 338
direct product, 353 elementary particle, 14
direct sum, 177 elementary reduction, 195
disconnected, 65 elementary subdivision, 112
discontinuous, properly, 268 elementary transformation, 133
discrete ellipsoid, 3
group, 58 embedding, 40
metric, 348 empty set, 338
space, 19 existence, 343
closed sets, 25 empty word, 194
subgroup, 270 equilibrium point, 14
topology, 19 equivalence
disjoint sets, 339 class, 52, 340
disjoint union, 340, 345 combinatorial, 112
topology, 37, 177 homotopy, 161
characteristic property, 62 is an equivalence relation,
disk 161
Euclidean, 31 of words, 195
hyperbolic, 271 relation, 52, 340

---

Index 369
generated by a relation, exponential
340 function, 20
topological, 4, 22 quotient map, 61, 179, 235
Euclidean Ext, see exterior
ball, 31 extension lemma, 331
regular, 83 extension of a map, 342
disk, 31 exterior, 25, 26
dot product, 347 extreme value theorem, 73, 76,
geometry, 7 352
locally, 4, 30
metric, 348 face
neighborhood, 30 boundary, 93
polyhedron, 94 map, 293
simplex, 96 of a presentation, 131
simplicial complex, 93 of a simplex, 93
space, 2, 347 of an abstract simplex, 96
ambient, 17 point, 124
is second countable, 33 proper, 93
zero-dimensional, 31, 347 family, 338
topology, 19 fan transformation, 125
triangle, 7 fiber, 53
Euler characteristic, 113, 142, action on, by fundamental
328 group, 245
and cohomology, 333 field, 330
combinatorial invariance, characteristic zero, 330
113, 142 ordered, 343
of a graph, 230 field equations, Einstein, 14
of a topological space, 328 figure eight space, 55, 160
of compact surfaces, 143, finite
229 graph, 101
topological invariance, 229, locally, 96
327 sequence, 345
Euler’s formula, 112 set, 344
even map, 253 simplicial complex, 96
even permutation, 353 finitely presented, 202
evenly covered, 184, 234 first category, 86
exact functor, 335 first countable, 32
exact homology sequence, 311 locally Euclidean spaces, 38
exact sequence, 296 metric spaces, 38
long, 311 first isomorphism theorem, 356
of chain complexes, 310 five lemma, 313
short, 296 fixed point theorem, Brouwer,
existence 192
axiom, 343 folding, 134
of real numbers, 343 forgetful functor, 172

---

370 Index
formal linear combination, 97 abelianized, 228
free of a topological group, 191
abelian group, 204 of a wedge of spaces, 213
characteristic property, of spheres, 188, 217
204 of the circle, 180
uniqueness, 208 of the projective plane, 247
abelian subgroup, 205 of the torus, 189
group, 200 topological invariance, 159
characteristic property, fundamental theorem of algebra,
200 191
uniqueness, 201
group action, 60
Gauss–Bonnet theorem, 8
product, 195
general linear group, 10, 59, 60
characteristic property,
complex, 10
198
general position, 92
uniqueness, 199
general relativity, 14
vector space, 97
generating circle, 45
Freedman, Michael, 7
generator
freedom, degrees of, 2
of a cyclic group, 356
full subcategory, 171
of a group, 199
function, 341
of a presentation, 201
multiple-valued, 8
genus, 144
functor
geodesic
cohomology, 330
hyperbolic, 271
contravariant, 172
polygon, 273
covariant, 172
regular, 274
exact, 335
geometric realization, 97, 99
forgetful, 172
functor, 172
fundamental group, 172
of a polygonal presentation,
homology, 296
131
fundamental group, 6, 152
action on fiber, 245 geometrization conjecture, 7
and homology, 305 geometry
and surface presentation, algebraic, 11
217 Euclidean, 7
change of base point, 154 plane, 7
functor, 172 Riemannian, 8
homotopy invariance, 161 solid, 7
is a group, 154 GL(n,R) (general linear group),
of a graph, 215 10, 59, 60
of a manifold is countable, gluing lemma, 46
189 counterexample, 62
of a polyhedron, 230 graph, 100
of a product, 189 finite, 101
of a surface, 220 fundamental group, 215

---

Index 371
of a continuous function, 2, groups, category of, 171
43
is a manifold, 44 Hn (upper half space), 34
of a relation, 8 hairy ball theorem, 322
simple, 101 half space, upper, 34
gravitation, 14 ham sandwich theorem, 254
gravity, center of, 110 handedness, 106
greatest lower bound, 343 handle, 9, 129
GROUP (category of groups), Hauptvermutung, 112
171 Hausdorff
group, 352 if diagonal is closed, 62
abelian, 11, 203 product space, 50
action, 59, 266 space, 31
continuous, 60 subspace, 42
free, 60 Heegaard, Poul, 137
proper, 266 Heine–Borel theorem, 351
quotient by, 61 hole, 5, 6, 147
transitive, 60 holomorphic, 8
as a category, 173 HomC(X,Y) (set of morphisms),
automorphism, of covering, 170
248 Hom(X,Y) (set of group
complex general linear, 10 homomorphisms), 173,
complex special linear, 11 329
covering, 248 homeomorphic, 4, 22
direct product, 353 is an equivalence relation,
discrete, 58 22
divisible, 335 homeomorphism, 4, 22
free, 200 local, 24
free abelian, 204 openness, 24
fundamental, 6, 152 vs. closed map, 27
general linear, 10, 59, 60 vs. open map, 27
homotopy, 169–170 homogeneity of norm, 89
injective, 335 homogeneous
Lie, 10 space, 63
orthogonal, 11, 59, 60 spacetime, 14
permutation, 353 homological algebra, 297
presentation, 201, 202 homological degree, 320
special linear, 11 homologous, 295
special orthogonal, 11 homology
special unitary, 11 and the fundamental group,
symmetric, 353 305
theory, combinatorial, 203 class, 295
topological, 58 functor, 296
quotient, 63 groups
unitary, 11 of a chain complex, 297

---

372 Index
simplicial, 324 maps and fundamental
singular, 295 group homomorphisms,
homomorphism 164
induced by a chain map, maps and homology
297 homomorphisms, 300
induced by a continuous path, 151
map, 296 relative to a subspace, 151
homotopy invariance, 300 homotopy
of a compact polyhedron, category, 173
334 category, pointed, 173
of a contractible space, 303 chain, 303, 317
of a disconnected space, 298 equivalence, 161
and deformation
of a one-point space, 299
retraction, 166
of a pseudomanifold, 334
is an equivalence relation,
of a simplex, 324
161
of a triangulable manifold,
equivalent, 161
334
groups, 169–170
of a wedge, 334
invariance
of spheres, 309
of path product, 152
sequence, long exact, 311
of singular homology, 300
simplicial, 324
of the fundamental group,
vs. singular, 326
161
singular, 295
is an equivalence relation,
vs. simplicial, 326
148
topological invariance, 296
lifting property, 238
zero-dimensional, 298
of the circle, 181
homomorphism
of maps, 148
covering, 258
path, 151
is a covering map, 258
and composition, 158
criterion, covering, 260
is an equivalence relation,
from a quotient group, 355
151
fundamental group, induced preserved by composition,
by a continuous map, 149
159 relative, 151
homology straight-line, 150
induced by a chain map, theory, 170
297 type, 161
induced by a continuous hull, convex, 92
map, 296 Hurewicz
of cyclic group, 357 homomorphism, 308
of group, 354 theorem, 308
of topological groups, 270 Hurewicz, Witold, 308
homotopic, 148 hyperbolic
degree, 320 disk, 271

---

Index 373
geodesic, 271 homomorphism, in
metric, 271 homology, 296, 297
triangle inequality, 289 morphism, 172
neighborhood, regular, 278 orientation, 107
hyperplane, affine, 92 subgroup, 239
infimum, 343
infinite
i (imaginary unit), 344
cyclic group, 200, 356
I (unit interval), 54
dimensional simplicial
ι(cid:9)S (inclusion map), 342
complex, 96
X (intersection), 345
α α product, 49
ideal point, 12
set, 344
identification space, 52
initial point of a path, 150
identity
initial vertex, 131
in a category, 171
injection
in a group, 352
in a category, 175
uniqueness, 353
into direct sum, 177
map, 342
into disjoint union, 345
continuity, 21
into free group, 200
path class, 153
into free product, 197
Imf (image of f), 354
injective, 342
image
group, 335
inverse, 342
injectivity theorem, 239
is a subgroup, 354
inside out sphere, 5
of a function, 342
Int, see interior
of a homomorphism, 354
integers, 344
of a normal subgroup, 356
modulo n, 356
set, 342
interior, 25, 26
imaginary unit, 344
of a manifold with
inclusion map, 342
boundary, 34, 38
continuity, 41 of a simplex, 93
increasing function, 345 intermediate value theorem, 65,
independent, linearly, 204 68
index intersection
of a subgroup, 354 of an indexed collection, 345
of a vector field, 192 of closed sets
index set, 345 in a metric space, 349
indexed collection, 345 in a topological space, 24
intersection, 345 of open sets
union, 345 in a metric space, 349
induced in a topological space, 18
homomorphism of of sets, 339
fundamental groups, intertwined edge pairs, 140
159 interval, 344
by homotopic maps, 164 is connected, 68

---

374 Index
unit, 54 inverse, 343
invariance of dimension, 318, 319 translation, 59, 63
invariant length, 7, 347
combinatorial, 113, 142 lens space, 269
topological, 6 coverings of, 286
inverse Lie group, 10
image, 342 abelian, 11
in a group, 352 lift, 179, 180, 237
uniqueness, 353 lifting criterion, 240
left, 343 lifting problem, 239
map, 342 lifting property
of a path class, 153 homotopy, 238
right, 343, 346 of the circle, 181
isolated singular point, 192 path, 238
isometry, 8 of the circle, 181
isomorphic coverings, 258 unique, 237
isomorphism of the circle, 181
in a category, 171 limit of a sequence
of coverings, 258 in a discrete space, 20
of groups, 354 in a Hausdorff space, 32
problem, 203 in a metric space, 349
simplicial, 96 in a topological space, 20
theorem, covering, 260 in a trivial space, 20
theorem, first, 356 limit point, 26, 348
isotropic spacetime, 14 and closed sets, 26
compact, 76
k-skeleton, see skeleton vs. compact, 77, 78
Ker, see kernel vs. sequentially compact,
kernel, 354 77, 78
is a subgroup, 354 line
is normal, 355 long, 88
Klein bottle, 126 real, 2
covering, 253 segment, 347
presentation, 133 with two origins, 62
linear combination, 204
largest element, 341 formal, 97
latitude, 3 linear ordering, 341
laws of motion, Newton’s, 12 linear transformation, 20
least upper bound, 343 linearly independent, 204
Lebesgue number, 76 local criterion for continuity, 21
lemma, 76 local finiteness, see locally finite
left local homeomorphism, 24
action, 59 openness, 24
coset, 354 local section, 184, 236
coset space, 61 of a covering map, 236

---

Index 375
locally mathematical object, 338
compact, 81 maximal, 341
Hausdorff space, 81, 82, tree, 214
89 Mayer–Vietoris
connected, 72 sequence
Euclidean, 4, 30 cohomology, 335
implies first countable, 38 simplicial, 325
finite, 93, 96 singular, 309
path connected, 72 theorem
simply connected, 262 cohomology, 335
logarithmic function, 20 simplicial, 325
long exact homology sequence, singular, 292, 309
311 mechanics, classical, 12
long line, 88 member of a set, 338
longitude, 3 membership, 338
loop, 151 mesh, 317
based at a point, 151 metric, 348
constant, 151 discrete, 348
Lorentz metric, 14 Euclidean, 348
lower bound, 341 hyperbolic, 271
Lorentz, 14
main theorem space, 348
on compactness, 73 first countable, 38
on connectedness, 67 Hausdorff, 31
manifold, 1, 4, 33 second countable, 38
boundary, 35 subspace of, 40
classification, 6 topology, 19
complex, 33 minimal, 341
countable fundamental Mo¨bius
group, 189 band, 105, 176
homology of, 334 group, 272
is locally compact transformation, 272
Hausdorff, 83 modulo n, 356
is locally path connected, 72 Moise, Edwin, 105
product of, 51 monodromy theorem, 239
Riemannian, 8 morphism, 170
smooth, 33 induced, 172
topological, 33 motion, Newton’s laws of, 12
with boundary, 34, 334 multiple-valued function, 8
2-dimensional, 191 multiplication
zero-dimensional, 37 group, 352
map, 341 of cosets, 355
mapping, 341 of path classes, 153
mapping cylinder, 167 of paths, 152
Markov, A. A., 7 of words, 194

---

376 Index
N (set of natural numbers), 344 O(n) (orthogonal group), 11, 59,
n-dimensional 60
manifold, 33 object
topological manifold, 33 in a category, 170
n-holed torus, 129 mathematical, 338
universal covering, 275 odd map, 253
odd permutation, 353
n-manifold, 33
one-point compactification, 89
n-sphere, 44
one-point space, singular
singular homology, 309
homology, 299
n-torus, 51
one-point union, 55
as a coset space of Rn, 61
one-to-one
fundamental group, 189
correspondence, 342
n-tuple, ordered, 345
function, 342
naive set theory, 337
onto, 342
natural numbers, 344
open
natural orientation, 106
ball, 348
naturality of connecting is an open set, 349
homomorphisms, 312 cover, 32, 73
nearness, 18 in a metric space, 350
neighborhood, 18 of a subset, 73
basis, 32 cube, 29
countable, 32 map, 24
nested, 77 product of, 62
Euclidean, 30 vs. homeomorphism, 27
regular hyperbolic, 278 set
nested as a topological space, 19
cubes, 351 criterion for continuity,
350
neighborhood basis, 77
in a metric space, 348
sets, 76
in a topological space, 18
Newton’s laws of motion, 12
intersection, in a metric
nondegenerate base point, 212
space, 349
nonorientable surface, 144
intersection, in a
covering of, 253
topological space, 18
norm, 89, 347
is a manifold, 34
normal closure, 201
is Hausdorff, 31
normal covering, 245
is second countable, 33
normal subgroup, 354
union, in a metric space,
image, 356 349
north pole, 3, 45 union, in a topological
nowhere dense, 85 space, 18
nth homotopy group, 170 simplex, 93
nth power map, 191, 235 star, 114
null homotopic, 151 orbit, 60, 245

---

Index 377
criterion, 249 paraboloid, 3
space, 61, 266 parameters, 1
by free proper group partial ordering, 341
action, 268 partially ordered set, 341
order of a group, 353 particle, elementary, 14
order topology, 37 partition, 52, 340
ordered passing to the quotient, 56, 57
field, 343 homomorphism, 356
n-tuple, 345 pasting, 134
pair, 340 path, 69, 150
set class, 151
partially, 341 class identity, 153
totally, 37, 341 class inverse, 153
well, 88, 341 class multiplication, 153
ordering associativity, 153
linear, 341 class product, 153
partial, 341 associativity, 153
simple, 341 component, 72
total, 341 connected, 69
orientability is combinatorially locally, 72
invariant, 115 connectivity relation, 71
orientable homotopic, 151
pseudomanifold, 334 homotopy, 151
simplicial complex, 107 and composition, 158
surface, 144, 229 is an equivalence relation,
orientation 151
induced, 107 lifting property, 238
natural, 106 of the circle, 181
of a simplex, 105 multiplication, 152
of a simplicial complex, 107 grouping, 154
oriented presentation, 144 homotopy invariance, 152
oriented simplex, 106 product, 152
origins, line with two, 62 grouping, 154
orthogonal group, 11, 59, 60 homotopy invariance, 152
special, 11 reverse, 153
periodic edge path, 119
π1(X) (fundamental group), 155 periodic trajectory, 14
π1(X,q) (fundamental group), permutation, 342
152 even, 353
P2 (projective plane), 119 group, 353
Pn (real projective space), 55 odd, 353
P(S) (power set), 339 plane, 3
pair, ordered, 340 curve, 2
pancakes, 234 geometry, 7
parabola, 2 projective, 119

---

378 Index
Poincar´e topologically equivalent,
conjecture, 6 133
homomorphism, 305 standard, 133, 137
Poincar´e, Henri, 4, 6 surface, 132
point, 18 and fundamental group,
at infinity, ideal, 12 217
pointed classification, 137
homotopy category, 173 product
topological category, 171 Cartesian, 340, 346
topological space, 171 finite, 346
polar coordinates, 3 infinite, 346
direct, 353
pole
dot, 347
north, 3, 45
free, 195
south, 45
in a category, 174
polygon
uniqueness, 174
geodesic, 273
map, 50
regular geodesic, 274
of closed maps, 62
polygonal presentation, 130
of compact spaces, 74
geometric realization, 131
of covering maps, 253
topologically equivalent, 133
of locally compact
polygonal region, 123
Hausdorff spaces, 83
polyhedron, 100
of manifolds, 51
Euclidean, 94
of open maps, 62
fundamental group, 230
of path classes, 153
homology, 334
of paths, 152
is Hausdorff, 114
of quotient maps, 86
is locally path connected,
of topological groups, 59
114
of words, 194
polynomial, 20
open sets, 48
position, general, 92
space, 48
positivity
connectedness, 67
of metric, 348
fundamental group, 189
of norm, 89 Hausdorff, 50
power map, 191, 235 second countable, 50
power set, 339 topology, 48
axiom, 339 associativity, 50
partial ordering, 341 basis, 48, 50
precompact, 82 characteristic property, 49
presentation infinite, 49, 177
and Seifert–Van Kampen on Rn, 48
theorem, 211 uniqueness, 49
of a group, 201, 202 projection
polygonal, 130 from a Cartesian product,
geometric realization, 131 346

---

Index 379
from a product space, 50 by free proper group action,
is a quotient map, 62 268
in a category, 174 by group action, 61
onto a quotient group, 355 descending to, 56, 57
onto a quotient space, 52 group, 355
stereographic, 45, 187 map, 52
and one-point characterization, 57
compactification, 89 composition, 53
projective exponential, 61, 235
plane, 119 restriction, 53
covering, 253 of a compact space, 74
Euler characteristic, 143 of a manifold, 269
fundamental group, 220, of a topological group, 63
247 passing to, 56, 57
presentation, 133 second countable, 54
quotient of disk, 122 space, 52
connectedness, 67
quotient of sphere, 121
uniqueness, 57
quotient of square, 122
topology, 52
space
characteristic property, 56
as orbit space, 61
complex, 12, 62
R (set of real numbers), 343
covering, 253
Rn (n-dimensional Euclidean
homology, 334
space), 347
is a manifold, 62
R(cid:22)S(cid:23) (free vector space), 97
real, 55
Rad´o, Tibor, 104
transformation, 12
range, 341, 342
proper
rank
face, 93
of a finitely generated
group action, 266
abelian group, 206
on locally compact
of a free abelian group, 205
Hausdorff space, 267
rational function, 20
quotient, 268
rational numbers, 344
local homeomorphism, 253
real line, 2
map, 84
real numbers, 343
is closed, 84
uniqueness, 343
subset, 338
real projective space, 55
properly discontinuous group
is a manifold, 62
action, 268
real vector spaces, category of,
property, topological, 4
171
pseudomanifold, 334 realization, geometric, 97, 99
of a polygonal presentation,
Q (set of rational numbers), 344 131
quantum field theory, 14 reduced edge path, 101
quotient reduced word, 195

---

380 Index
reduction algorithm, 196 rigid body, 13
reduction, elementary, 195 RING (category of rings), 171
reflecting, 134 rings
reflection map, 321 category of, 171
reflexive, 340 commutative, category of,
region, polygonal, 123 171
regular rotating, 134
Euclidean ball, 83 Russell’s paradox, 338, 339
geodesic polygon, 274 Russell, Bertrand, 338
hyperbolic neighborhood,
278 Sn (unit n-sphere), 44
point, of vector field, 192 sandwich
relabeling, 133 ham, 254
relation, 340 tofu, 254
equivalence, 52, 340 saturated, 52
generated by a relation, scheme, vertex, 96
340 Sch¨onflies theorem, 104
of a presentation, 202 second category, 86
relative homotopy, 151 second countable, 32
relative topology, 40 metric space, 38
relatively compact, 82 product space, 50
relativity, general, 14 quotient, 54
relator, 201 subspace, 42
reparametrization, 151 section, 184
restriction, 342 local, 184, 236
continuity of, 21, 41 of a covering map, 236
of quotient map, 53 segment, line, 347
retract, 160, 176 Seifert–Van Kampen theorem,
deformation, 161 211
strong deformation, 161 and presentations, 211
retraction, 160 proof, 221
deformation, 161 special cases, 212, 217
strong deformation, 161 semilocally simply connected,
reverse path, 153 265
revolution, surface of, 45 separation of a space, 65
Riemann surface, 9 sequence, 345
Riemannian geometry, 8 convergent
Riemannian manifold, 8 in a metric space, 349
right in a topological space, 20
action, 59 finite, 345
of fundamental group, 245 limit
coset, 354 in a discrete space, 20
inverse, 343, 346 in a metric space, 349
translation, 59 in a topological space, 20
right-handed, 107 in a trivial space, 20

---

Index 381
sequentially compact, 77 isomorphism, 96
vs. compact, 78 map, 93, 95
vs. limit point compact, 77, between abstract
78 complexes, 96
SET (category of sets), 171 Mayer–Vietoris sequence,
set, 338 325
difference, 339 simply connected, 156
membership, 338 covering, 261
of all sets, 339 locally, 262
theory, naive, 337 semilocally, 265
sets, category of, 171 sine curve, topologist’s, 69, 72,
sgn, 353 88
sheet, 9, 237 singleton, 339
short exact sequence, 296 singular
shrinking lemma, 82 boundary, 293, 294
side boundary operator, 293
of a geodesic, 274 chain, 293
of a simplex, 108 chain group, 293
SIMP (category of simplicial cochain, 329
complexes), 171 cohomology group, 329
simple graph, 101 cycle, 294
simple ordering, 341 homology groups, 295
simplex, 92 homotopy invariance, 300
abstract, 96 of a contractible space,
affine singular, 293 303
Euclidean, 96 of a disconnected space,
open, 93 298
oriented, 106 of a one-point space, 299
singular, 292 of spheres, 309
standard, 292 vs. simplicial, 326
simplices, see simplex zero-dimensional, 298
simplicial map, 292
boundary, 324 Mayer–Vietoris theorem,
boundary operator, 323 292
chain, 323 point, 12
complex isolated, 192
abstract, 96 of vector field, 192
dimension, 334 simplex, 292
Euclidean, 93 affine, 293
fundamental group, 230 subdivision operator, 316
complexes, category of, 171 size, not a topological property,
cycle, 324 22
homology groups, 324 skeleton
of a simplex, 324 of a Euclidean simplicial
vs. singular, 326 complex, 95

---

382 Index
of an abstract simplicial unit, 23, 44
complex, 96 in R3, 3
SL(n,C) (complex special linear with n handles, 129
group), 11 square root, complex, 8
SL(n,R) (special linear group), stable trajectory, 14
11 stack of pancakes, 234
Smale, Stephen, 5, 7 standard
small chain, 315 basis for Zn, 204
smallest element, 341 presentation, 133, 137
smooth dynamical system, 13 simplex, 292
smooth manifold, 33 star, open, 114
SO(n) (special orthogonal star-shaped, 162
group), 11 Steinitz, Ernst, 112
solid geometry, 7 stereographic projection, 45, 62,
south pole, 45 187
space, 18 and one-point
curve, 2 compactification, 89
discrete, 19 straight-line homotopy, 150
Euclidean, 347 strictly increasing, 345
Hausdorff, 31 string, 15
identification, 52 theory, 14
metric, 348 strong deformation retract, 161
product, 48 strong deformation retraction,
quotient, 52 161
topological, 18 structure theorem, covering
variable, 152 group, 250
space-filling curve, 188 SU(n) (special unitary group),
spacetime, 14 11
homogeneous and isotropic, subbasis, 36
14 subcategory, 171
special linear group, 11 full, 171
special loop, 190 subcomplex
special orthogonal group, 11 of a Euclidean simplicial
special unitary group, 11 complex, 95
specification axiom, 338 of an abstract simplicial
sphere, 3, 44 complex, 96
Euler characteristic, 143 subcover, 32, 73, 350
fundamental group, 188 countable, 32
is simply connected, 217 subdividing, 133
not a retract of the ball, 334 subdivision, 109
presentation, 133 barycentric, 110, 315
quotient of disk, 120 elementary, 112
quotient of square, 120 operator, singular, 316
singular homology, 309 subgraph, 101
turning inside out, 5 subgroup, 353

---

Index 383
normal, 354 universal covering of, 282
of a cyclic group, 357 surjective, 342
of a free abelian group, 205 symmetric, 340
of a topological group, 59, group, 353
61, 63 symmetry of a metric, 348
subsequence, 345
subset, 338 T2 (torus), 51
of a countable set, 344 Tn (n-torus), 51
proper, 338 terminal point of a path, 150
subspace, 39, 40 terminal vertex, 131
affine, 92 tetrahedron, 92
closed sets, 41 theta space, 162
Hausdorff, 42 Thurston geometrization
of a metric space, 40 conjecture, 7
of a subspace, 41 Thurston, William, 7
second countable, 42 Tietze, Heinrich, 112, 203
topology, 40 time variable, 152
basis for, 42 tofu sandwich theorem, 254
characteristic property, 41 TOP (topological category), 171
uniqueness, 47 TOP ∗ (pointed topological
sum category), 171
connected, 126 topological
is a manifold, 126 boundary, 35
with sphere, 129 category, 171
direct, 177 category, pointed, 171
in a category, 175 embedding, 40
uniqueness, 175 group, 58
in the category of groups, discrete, 58
199 discrete subgroup of, 270
in the topological category, fundamental group of, 191
177 product of, 59
supremum, 343 quotient of, 63
surface, 3, 117, 119 subgroup of, 59, 63
classification, 6 universal covering space
fundamental group of, 220 of, 290
abelianized, 228 invariance
nonorientable, 144 of Euler characteristic,
of genus n, 144 327
of revolution, 45 of homology groups, 296
orientable, 144 of the fundamental group,
presentation, 132 159
and fundamental group, invariant, 6
217 manifold, 33
classification, 137 property, 4, 22
Riemann, 9 space, 18

---

384 Index
topologically equivalent, 4, 22 left, 59, 63
presentations, 133 right, 59
topologist’s sine curve, 69, 72, 88 transpose of linear map, 173
topology, 4, 18 transposition, 353
algebraic, 6 tree, 163
discrete, 19 contractible, 163
disjoint union, 37 maximal, 214
Euclidean, 19 triangle inequality, 89, 348
generated by a basis, 27 for hyperbolic metric, 289
generated by a subbasis, 36 triangle, Euclidean, 7
metric, 19 triangulable, 100
product, 48 triangulation, 100
quotient, 52 of 1-manifolds, 102
relative, 40 of 2-manifolds, 104
subspace, 40 of 3-manifolds, 105
trivial, 19 trigonometric function, 20
torsion trivial group, 353
element, 205 trivial topology, 19
free, 205 turning the sphere inside out, 5
subgroup, 205 twisted edge pair, 139
torus, 3, 51 two origins, line with, 62
n-dimensional, 51 Tychonoff’s theorem, 75
as a coset space of Rn, 61 type, homotopy, 161
as a quotient of the square, (cid:6)
55, 79 (cid:2)α X α (disjoint union), 345
coverings of, 270, 286 X (union), 345
α α
Euler characteristic, 143 U(n) (unitary group), 11
fundamental group, 189, 220 U-small chain, 315
homeomorphic to doughnut uncountable set, 344
surface, 51, 80 unfolding, 135
n-holed, 129 union
presentation, 133 axiom, 339
total ordering, 341 connectedness of, 67
totally ordered set, 37, 341 countable, 344
trajectory disjoint, 340, 345
periodic, 14 topology, 37
stable, 14 of an indexed collection, 345
transformation of closed sets
elementary, 133 in a metric space, 349
linear, 20 in a topological space, 24
transitive, 340 of open sets
group action, 60 in a metric space, 349
transitivity of covering group, in a topological space, 18
249 of sets, 339
translation unique lifting property, 237

---

Index 385
of the circle, 181 of a simplex, 92
uniqueness of an abstract simplicial
of abelianization, 231 complex, 96
of covering spaces, 260 point, 124
of free abelian group, 208 scheme, 96
of free group, 201 terminal, 131
of free product, 199 vertices, see vertex
of product topology, 49 volume, 7, 254
of quotient spaces, 57
of subspace topology, 47 wedge of spaces, 55
unit fundamental group, 212, 213
ball in Rn, 22 singular homology, 334
circle, 45 well-ordered, 88, 341
interval, 54 well-ordering theorem, 88, 346
sphere, 23, 44 winding number, 179, 182
unitary group, 11 word, 130, 194
special, 11 empty, 194
universalcoefficienttheorem,330 problem, 203
universal covering, 261 reduced, 195
of n-holed torus, 275 world sheet, 15
of a topological group, 290
Z (set of integers), 344
of compact surfaces, 282
Z/(cid:22)n(cid:23) (integers modulo n), 356
space, 261
Z(cid:22)S(cid:23) (free abelian group), 204
existence, 262
zero-dimensional
universal mapping properties,
Euclidean space, 31, 347
174
homology, 298
upper bound, 341
manifold, 37
upper half space, 34
zigzag lemma, 310
Zorn’s lemma, 347
variety, algebraic, 12
VECT C (category of complex
vector spaces), 171
VECT R (category of real vector
spaces), 171
vector field, 192, 322
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

---

---

---
