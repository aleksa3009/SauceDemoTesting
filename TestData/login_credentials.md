## Known Test Users

| Username               | Password       | Expected Behavior                         |
|------------------------|----------------|------------------------------------------|
| standard_user          | secret_sauce   | Successful login                         |
| locked_out_user        | secret_sauce   | Login blocked, error message shown      |
| problem_user           | secret_sauce   | App misbehaves (broken images, glitches)|
| performance_glitch_user| secret_sauce   | Slow loading but login succeeds          |
| error_user             | secret_sauce   | Causes error responses on certain actions|
| visual_user            | secret_sauce   | Used for visual UI testing                |
