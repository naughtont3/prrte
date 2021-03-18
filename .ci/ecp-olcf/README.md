ECP-CI at OLCF
--------------
[![pipeline status](https://code.ornl.gov/ecpcitest/ompi-x/naughtont3-prrte/badges/olcf-ecp-ci/pipeline.svg)](https://code.ornl.gov/ecpcitest/ompi-x/naughtont3-prrte/-/commits/olcf-ecp-ci)

CI Tests that run on OLCF resources via ECP project.

Brief summary:
 - PRRTE GitHub mirrored at OLCF GitLab (pull approx 30-minutes)
 - Builds source tree
    - autogen, configure, make install, make check, make examples
 - Runs tests in batch allocation with single node
 - Currently using 18-node Power9 ["Ascent" machine at OLCF](https://docs.olcf.ornl.gov/systems/ascent_user_guide.html)
 - Tests run using hostfile from allocation (e.g., `$LSB_DJOB_HOSTFILE`)
 - The CI status/results are reported back to GitHub via a python script (`build-status.py`)
    - See also: https://ecp-ci.gitlab.io/docs/guides/build-status-gitlab.html
    - Note: The `BUILDSTATUS_TOKEN` is defined in GitLab and contains a
      personal access token (`repo:status`) for the upstream GitHub user.
