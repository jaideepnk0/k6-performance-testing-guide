# k6-performance-testing-guide

Installation using Docker:
Run command: docker pull loadimpact/k6

running tests using Docker:
# When using the `k6` docker image, you can't just give the script name since
# the script file will not be available to the container as it runs. Instead
# you must tell k6 to read `stdin` by passing the file name as `-`. Then you
# pipe the actual file into the container with `<` or equivalent. This will
# cause the file to be redirected into the container and be read by k6.

docker run -i loadimpact/k6 run - <script.js
