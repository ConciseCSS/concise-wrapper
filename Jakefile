desc('Compile the files of Concise CSS')
task('concise', {async: true}, () => {
  jake.exec('concisecss compile concise.scss dist/concise.css', {
    printStdout: true,
    printStderr: true
  }, complete)
})

desc('Minify CSS')
task('minify', ['concise'], {async: true}, () => {
  jake.exec('cssnano dist/concise.css dist/concise.min.css', {
    printStdout: true,
    printStderr: true
  }, complete)
})

desc('Build the files')
task('default', ['concise', 'minify'])
