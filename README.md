Sample project showing how to use Bazel to build iOS and Android apps using a
monorepo.

Companion blog post: https://tulipemoutarde.be/posts/bazel-for-mobile-apps-part-1/

# Usage

## iOS

    $ bazel build //AppA-iOS
    $ bazel build //Lib-Swift:Lib_Swift
    $ bazel build @Rx//:RxSwift
    $ bazel build @Rx//:RxCocoa

To run the app, generate an XCode project with Tulsi.
