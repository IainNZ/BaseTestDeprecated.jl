# BaseTestDeprecated

[![Build Status](https://travis-ci.org/IainNZ/BaseTestDeprecated.jl.svg?branch=master)](https://travis-ci.org/IainNZ/BaseTestDeprecated.jl)

The `Base.Test` module changed substantially internally in
`v0.5`. Most use cases are unaffected, but some features
such as `with_handler` were removed. This pacakge provides
the previous `Base.Test` functionality so that packages.

### Usage

Replace `using Base.Test` with:

```julia
if VERSION >= v"0.5-"
    using BaseTestDeprecated
    const Test = BaseTestDeprecated
else
    using Base.Test
end
```