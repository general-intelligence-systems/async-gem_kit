# async-gem_kit

A template for creating async-native Ruby gems in the `Async::` namespace,
laid out like [`async-matrix`](https://github.com/general-intelligence-systems/async-matrix)
and the rest of the [Socketry](https://github.com/socketry) ecosystem: nested
modules, a matching directory tree, and the `async` gem as a runtime dependency.

## Usage

```bash
git clone https://github.com/general-intelligence-systems/async-gem_kit
cd async-gem_kit
bin/rename-gem async-http
bin/update-spec
bin/choose-license
bin/increment-version patch
bin/release-gem
```

**Every hyphen in the gem name is a directory boundary**; the last segment is the
file (and the deepest module). Underscores stay within a segment and camelize.
The name must contain at least one hyphen.

| gem name | file | module |
|---|---|---|
| `async-http` | `lib/async/http.rb` | `Async::Http` |
| `async-container` | `lib/async/container.rb` | `Async::Container` |
| `async-job-processor-redis` | `lib/async/job/processor/redis.rb` | `Async::Job::Processor::Redis` |
| `async-job-adapter-active_job` | `lib/async/job/adapter/active_job.rb` | `Async::Job::Adapter::ActiveJob` |
| `async-http-protocol-http3` | `lib/async/http/protocol/http3.rb` | `Async::Http::Protocol::Http3` |
