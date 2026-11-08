# clojure-test-suite-runner

Runs the [clojure-test-suite](https://github.com/jank-lang/clojure-test-suite) on [Clojerl](https://github.com/clojerl/clojerl).

## Use

Add the runner to the `rebar.config` of the test suite:

```erlang
{deps, [{clojerl, {git, "https://github.com/clojerl/clojerl", {tag, "0.9.1"}}},
        {clojure_test_suite_runner,
         {git, "https://github.com/clojerl/clojure-test-suite-runner", {tag, "v0.1.0"}}}]}.
{plugins, [{rebar3_clojerl, "0.8.8"}]}.
```

Run it from the root of the test suite:

```bash
rebar3 clojerl run -m clojure-test-suite.runner
```

The runner reads the tests from `test/**/*.cljc` in the current directory.
