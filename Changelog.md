## 1.4.0

- Add option to specify headers in encode - added in #34 by
  [@barruumrex](https://github.com/barruumrex)

## 1.3.3

- Fix empty streams raising a lexer error - raised in #28 by [@kiliancs](https://github.com/kiliancs)

## 1.3.2

- Cleanup, removing some unused defaults in function headers to remove compile
  time warnings

## 1.3.1

- Fix `:strip_cells` not stripping cells when multible options are specified - #29 by [@tomjoro](https://github.com/tomjoro)

## 1.3.0

- Now supports linebreaks inside escaped fields (#13)
- Raises an error when row length mismatches accross rows
- Uses [parallel_stream](https://github.com/beatrichartz/parallel_stream) for parallelism

## 1.2.4

- Fix encoding of double quotes

## 1.2.3

- Fix a condition where headers: true would enumerate the whole file once before parsing

## 1.2.2

- Fix default num_pipes argument to evaluate num_pipes dependent on scheduler at runtime
- Test utf-8 files with BOM
- Syntax and mix updates for elixir 1.2

## 1.2.1

- Decoder performance optimisations

## 1.2.0

- Use `Stream.transform/4` - incompatible with Elixir < `1.1.0`

## 1.1.5

- Decoder refactor from `Stream.resource/3` to `Stream.transform/3` in order to
  get more predictable stream behaviour
- Rows now get processed in order
- Fix a bug where stream would get evaluated before being decoded

## 1.1.4

- Fix a bug where headers could be out of order

## 1.1.3

- Fix a bug where headers could get parsed as the first row

## 1.1.2

- Fix a bug where calls to decode with num_pipes: 1 would yield varying
  results due to leftover state in decoder message queue

## 1.1.1

- Rescue from errors in stream producer to get more predictable behaviour
  in case of failure

## 1.1.0

- Better error messages when encountering invalid encodings

## 1.0.1

- Indicate `consolidate_protocols` for better encoding performance

## 1.0.0

- Use bytes as separators

## 0.2.3

- Add benchmarking

## 0.2.2

- Use utf-8 bytes instead of codepoints for multi-byte parsing

## 0.2.1

- Fix handling of multi-byte utf-8 characters

## 0.2.0

- Implement encoder protocol
