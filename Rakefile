task :default do
  build_dir = "build/duplicatetabbutton.safariextension"

  FileUtils.rm_rf( build_dir )
  FileUtils.mkdir_p( build_dir )

  assets = [
    "Icon-32.png",
    "icon-48.png",
    "Icon-64.png",
    "index.html",
    "Info.plist",
    "Settings.plist",
    "ToolbarIcon.png"
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
