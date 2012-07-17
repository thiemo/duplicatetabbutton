task :default do
  build_dir = "build/duplicatetabbutton.safariextension"

  FileUtils.rm_rf( build_dir )
  FileUtils.mkdir_p( build_dir )

  assets = [
    "etc/*",
    "img/*",
    "src/*"
  ]

  assets.each do |glob|
    Dir.glob( glob ).each do |src|
      puts "linking #{src}"
      dest = "#{build_dir}/#{File.basename( src )}"
      FileUtils.mkdir_p( File.dirname( dest ) )
      FileUtils.link( src, dest )
    end
  end
end
