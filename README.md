## What's poppin'?

I'm Brandon (he/they) and I'm a graduate student doing computational chemistry at the University of Wisconsin-Madison.

## My projects

### [CliffordNumbers.jl](https://github.com/brainandforce/CliffordNumbers.jl)

CliffordNumbers.jl implements Clifford algebras (also known as geometric algebras) as fundamental numeric types in Julia, just like complex numbers and quaternions (which are Clifford algebras themselves), hence the term "Clifford number". Clifford numbers are treated as scalars for the sake of broadcasting, and are only indexed by a special type that references the basis blades of the algebra.

The first goal of this package is to provide extremely high performance implementations of common operations like geometric products, wedge products, and more. Unlike many other implementations that use matrix representations of the Clifford algebra to perform calcuations, this package uses an additive representation where each coefficient associated with a basis blade is provided, which leads to significant gains in readability of internal code and performance of products beyond the geometric product. All types exported by this package are representable as plain bits, meaning that they can be stored inline in arrays for faster operations. For algebras up to five dimensions, all operations are allocation-free (this is due to Julia's tuple inlining limit of 32 elements), and in practice this can be maintained in six-dimensional algebras with sparse multivector representations: types are provided for even and odd multivectors as well as k-vectors, and the promotion system seamlessly integrates them in operations. There are no dependencies on other packages, not even StaticArrays or LinearAlgebra from the standard library.

The second goal of this package is to provide a convenient entry point for those wanting to incorporate tools from geometric algebra. This package does not require more general familiarity with abstract algebra; only basic geometric algebra knowledge is assumed. Ideally, not even linear algebra knowledge should be necessary for users.

### [Electrum.jl](https://github.com/brainandforce/Electrum.jl)

Electrum.jl is a package that provides types, functions, and other tools for working with data associated with crystal structures, including unit cell basis vectors, atomic positions, associated grids of data, and more. It provides tools such as data import from commonly used computational chemistry software (currently supporting abinit, VASP, and LAMMPS), properly scaled Fourier transforms and gradients, and more.

## My interests

### Geometric algebra

[Geometric algebra](https://en.wikipedia.org/wiki/Geometric_algebra) is the study of Clifford algebras (usually real Clifford algebras equipped with various metrics) and their application to problems in ways that admit a simple geometric interpretation. One of their core strengths is that they often contain elements that behave like imaginary numbers (in that they square to –1) but have concrete geometric interpretations as oriented areas or elements which perform some kind of rotation.

Geometric algebras come in many flavors, including vanilla geometric algebra (VGA), a drop-in replacement for the vector algebra used throughout physics, [projective geometric algebra (PGA)](http://projectivegeometricalgebra.org/), a variant which uses a degenerate metric to model points, lines, planes, and other primitives that may be useful if you are interested in computer graphics, and conformal geometric algebra (CGA), which uses a non-positive-definite metric and supports everything supported by PGA plus circles, spheres, and more.

The broader community is based around [bivector.net](https://bivector.net) and you can find me in the forums or the Discord server, usually in physics-related discussions. I am primarily interested in the application of vanilla and projective geometric algebras to problems in solid-state chemistry, especially problems involving crystal symmetries. Secondarily, I am interested in the use of vanilla geometric algebras as a tool to provide geometric interpretations of quantum theories; in particular, providing concrete geometric interpretations for their imaginary units.

### Mechanical keyboards

While I'm not involved in any software projects for mechanical keyboards at the moment, I am an enthusiast who has way too many keyboards to deal with. If you'd like to contribute to the software side of the mechanical keyboard community, I'd strongly suggest [ZMK](https://zmk.dev/), a Bluetooth-capable firmware based on Zephyr RTOS written in part by [a friend of mine](https://github.com/nicell).

## Support me

Much of the software development I do is either part of my work as a graduate student or as a hobby. **I don't expect donations or payment for my hobby projects,** but if you're so inclined, [my Ko-Fi is here.](https://ko-fi.com/brainandforce) 

<!--
**brainandforce/brainandforce** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
