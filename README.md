# Scanner

## Initialization

```go
func NewScanner(input string) *Scanner
```

## Navigation

```go
func (s *Scanner) Current() rune
func (s *Scanner) PeekNext() rune
func (s *Scanner) Previous() rune
func (s *Scanner) Peek(offset int) rune
func (s *Scanner) Take() rune
func (s *Scanner) Retreat() rune
func (s *Scanner) Skip()
func (s *Scanner) SkipN(n int)
```

## Position Information

```go
func (s *Scanner) Position() int
func (s *Scanner) Line() int
func (s *Scanner) Column() int
func (s *Scanner) Location() string
func (s *Scanner) SetLocation(line, column int)
func (s *Scanner) EOF() bool
func (s *Scanner) Len() int
```

## Bookmarks

```go
func (s *Scanner) Mark() int
func (s *Scanner) Reset(mark int)
```

## Text Extraction

```go
func (s *Scanner) Slice(start, end int) string
func (s *Scanner) SliceFrom(start int) string
func (s *Scanner) Remaining() string
```

## Pattern Matching

```go
func (s *Scanner) Match(expected rune) bool
func (s *Scanner) MatchAny(chars ...rune) bool
func (s *Scanner) MatchString(expected string) bool
```

## Consumption

```go
func (s *Scanner) ConsumeWhile(predicate func(rune) bool) string
func (s *Scanner) ConsumeUntil(predicate func(rune) bool) string
func (s *Scanner) ConsumeN(n int) string
```

## Search

```go
func (s *Scanner) Find(target rune) bool
func (s *Scanner) FindString(target string) bool
```

## Whitespace Handling

```go
func (s *Scanner) SkipWhitespace()
func isWhitespace(ch rune) bool
```

## Utilities

```go
func (s *Scanner) ColumnAt(pos int) int
```
