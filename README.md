This repository tests Git submodules.

Clone this repository in PhpStorm and it should fetch automatically the submodules test_sub1 and test_sub2.
You can test commits with test_main2 (commits to a submodule hier should appear and the same the other direction).

After a commit to a submodule, the reference in the main repository has changed. This needs an own commit in the main directory.
PhpStorm does automatically a "git submodule update --remote" on each project update which means, that the last commit is fetched.
Then you can the following code to ignore changes of the submodule reference in the main repository:

git update-index --assume-unchanged -- test_sub2 test_sub1