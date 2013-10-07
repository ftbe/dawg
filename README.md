# dawg

[Directed Acyclic Word Graph](http://en.wikipedia.org/wiki/Directed_acyclic_word_graph) implementation in Go, with fuzzy search of words in the graph.

# Usage

Import the library:

    import "github.com/ftbe/dawg"

Use it:
```go
    graph, err := dawg.CreateDAWGFromFile(os.Args[1])
    if err != nil {
        // Do something
        return
    }
    words, err := dawg.Search(graph, "aging", 2, 50, true, true)
    if err != nil {
        // Do something
        return
    }
    for _, word := range words {
        fmt.Println(word)
    }
```
