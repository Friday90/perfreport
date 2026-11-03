# Lab 3 Project Notes

The original C++ program uses Windows APIs to read CPU, memory, uptime, and
disk data. The Rust version reads those values using the `sysinfo` crate,
which provides one interface across Windows and Linux. The existing score
thresholds and ratings are unchanged. Unit tests cover normal usage,
intermediate penalties, high penalties, and the exact threshold boundaries.

The Dockerfile uses a separate build stage and a smaller runtime stage. The
GitHub Actions workflow checks formatting, runs Clippy, builds the Rust
program, and runs tests before the container build job is allowed to begin.

**AI help used:** ChatGPT helped complete the four Rust TODO sections using
the instructor's handout, add scoring tests, and prepare the documentation.
Before submitting, I will run the code and check the output myself.
