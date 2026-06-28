## Guidelines

**Compound nouns**
Productive compound nouns (noun + noun, adjective + noun, and preposition + noun) are split into their semantic head and prefix added with `:mod`. Unproductive compounds (verb + noun) are annotated with the full word. 
E.g.: *schildersloopbaan* (N + N) and *slaapkamer* (V + N)
```
(l / loopbaan
    :mod (s / schilder))

(s / slaapkamer) 
```

**Contractions**
Contracted words are written out in full. 
E.g.: *zo'n* and *'t* 
```
(z / zo-een)

(h / het)
```

**Figurative speech**
Mainly in *The Little Prince* figurative speech is used. 
E.g.: *Grote mensen*
```
(m / mensen
    mod: (g / groot))
```

**Sayings**
A new non-core role was developed specifically for sayings in order to distinguish between metaphorical text and literal text. The role is used by adding the words of the sayings with `:mod`. 
E.g.: 
```
:spreekwoord (o / op
    :mod (g / goed
        :mod (g2 / geluk)))
```

**Multiple word expressions**
In cases where a multiple word expression can be represented with a single word synonym, was opted for rather than using a multiple word expression.
E.g.: *op een keer*
```
(o / ooit)
```

**Implicit reference**
If a sentece refers to something mentioned in a previous sentence, the referenced thing is explicitly annotated to avoid ambiguity. 
E.g.: *Die is maar één keer gezien...* (referring to a planet mentioned in the sentence before)
```
(p / planeet
    :mod (d / die))
```

**Intonation**
This is adapted from the English AMR guidelines, with the slight adjustment of writing the intonation in Dutch rather than English.
E.g.: Something being said in a condescending manner
```
:mode neerbuigend
```
