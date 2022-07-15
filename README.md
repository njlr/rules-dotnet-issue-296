# rules-dotnet-issue-296

```bash
bazel build //...
sha256sum ./bazel-bin/bundle.tar

bazel clean

bazel build //...
sha256sum ./bazel-bin/bundle.tar
```
