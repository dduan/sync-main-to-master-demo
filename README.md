# How to rename 'master' branch responsibly

To rename 'master' branch to something else, we should be considerate of
existing consumers of our repositories. The best way to rename it is to execute
a proper deprecation plan.

This plan may include best-effort communication to users, and contributors
(referred to as users from now on).  But more importantly, we should consider
keeping `master` around for a grace period for users to migrate their build
processes, scripts, etc.

This repo includes a GitHub workflow that take some simple step to ensure
a `main` branch is synchronized to `master`. Use it during your grace period by
including
[.github/workflows/sync-to-master.yml](.github/workflows/sync-to-master.yml) in
your projects `.github/workflows` directory. Its content should be relatively
easy to understand and customize. It assumes you no longer update `master`.

*There's no need to do this for new projects' repositories, of course.*

## LICENCE

MIT. See [LICENSE.md](LICENSE.md).
