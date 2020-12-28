# gosimports

![](https://github.com/rinchsan/gosimports/workflows/CI/badge.svg)
![](https://img.shields.io/github/release/rinchsan/gosimports.svg?colorB=7E7E7E)

Simpler goimports, hard fork of `golang.org/x/tools/cmd/goimports`

## Installation

```bash
go get github.com/rinchsan/gosimports/cmd/gosimports
```

## Example

```go
import (
	"bufio"

	// comment

	"golang.org/x/tools/internal/imports"

	"errors"
	gocmd "golang.org/x/tools/internal/gocommand"
	"flag"

	"runtime" // comment
	_ "runtime/pprof"
	"strings"

)
```

↓ `$ gosimports -w`

```go
import (
	"bufio"
	"errors"
	"flag"
	"runtime"
	_ "runtime/pprof"
	"strings"

	gocmd "golang.org/x/tools/internal/gocommand"
	"golang.org/x/tools/internal/imports"
)
```
