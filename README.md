# csharp-stuff

Learning C# and .NET by building **Stride**, a tool that reads the GPS file (GPX) from a run,
works out distance, pace, climb and splits, and draws the route as a poster.
It ends up with a command-line tool, a web API and a native AOT binary, all sharing one library.

## Layout

| Folder | What's there |
|---|---|
| [`learning/`](learning/) | The first steps before Stride: hello, pace calculator, a week of runs, classes / records / structs |
| [`stride/`](stride/) | The project: one solution, four projects |

```
stride/
├── Stride.slnx
├── src/Stride.Core/      library: model, GPX reading, maths, poster (no Console)
├── src/Stride.Cli/       command-line tool
├── src/Stride.Api/       web API (POST /stats, POST /poster)
└── tests/Stride.Checks/  tests
```

## Run

Needs the .NET 10 SDK.

```sh
cd stride
dotnet build
dotnet run --project src/Stride.Cli -- stats ../data/run.gpx
dotnet run --project src/Stride.Api --urls http://127.0.0.1:5080
dotnet test
```

## Progress

| Part | Status |
|---|---|
| A: first steps | |
| B: Stride Core + CLI | |
| Tests | |
| Web API | |
| Parallel year in review | |
| P/Invoke, Span, native AOT | |

✅ done · 🟨 in progress

## Data

`data/` holds generated sample runs only. Real GPX files contain where you live and run, so keep your own out of a public repo.
