# dawg

[Directed Acyclic Word Graph](http://en.wikipedia.org/wiki/Directed_acyclic_word_graph) implementation in Go, with fuzzy search of words in the graph.

# Usage

Import the library:

    import "github.com/ftbe/dawg"

Use it:
```go
    dawg := dawg.CreateDAWGFromFile(os.Args[1])
    for _, word := range dawg.Search(dawg, "aging", 2, 50, true, true) {
        fmt.Println(word)
    }
```
