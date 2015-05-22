require 'rake/clean'

$build_dir = '_site'
$epub_dir = '_epub'
$fixed_dir = '_fixed'

desc 'Build and check standard and kindle epubs'
task default: [:check_standard, :check_kindle ]

desc 'Build standard epub'
task standard_epub: [:standard_content, $epub_dir] do
  epub 'standard'
end

desc 'Build kindle epub'
task kindle_epub: [:kindle_content, $epub_dir] do
  epub 'kindle'
end

desc 'Check standard epub'
task check_standard: [:standard_epub] do
  check 'standard'
end

desc 'Check kindle epub'
task check_kindle: [:kindle_epub] do
  check 'kindle'
end

desc 'Build kindle content files'
task kindle_content: [] do
  build 'kindle'
end

desc 'Build standard content files'
task standard_content: [] do
  build 'standard'
end

def build(edition)
  runcommand "jekyll build --destination=#{content_dir(edition)} --config=_config.yaml,_#{edition}-edition.yaml"
end

def check(edition)
  runcommand("epubcheck #{epub_file(edition)}")
end

def content_dir(edition)
  "#{$build_dir}/#{edition}"
end

def epub(edition)
  epub_file = File.expand_path(epub_file(edition))
  rm_f epub_file
  runcommand("cd #{$fixed_dir}; zip #{epub_file} -rX0 mimetype")
  runcommand("cd #{$fixed_dir}; zip #{epub_file} -rDX9 \. -x mimetype .DS_Store")
  runcommand("cd #{content_dir(edition)}; zip #{epub_file} -rDX9 \. -x .DS_Store")
end

def epub_file(edition)
  "#{$epub_dir}/#{edition}.epub"
end

def runcommand(command, redirect: true, background: false)
    full_command = "#{command}#{' 2>&1' if redirect}#{' &' if background}"
    puts ">>> #{full_command}"
    IO.popen(full_command).each_line{|line| puts line}
end

desc 'Clobber all files, then build and validate the epub file.'
task fresh: [:clobber, :default]

directory $epub_dir

CLEAN.include $build_dir, $epub_dir
