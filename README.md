# Setup steps for new project

Make a .ruby-version file with your chosen ruby version. Create a Gemfile with your gems. Run the following commands to make a lockfile.

nix flake init --template github:bobvanderlinden/nixpkgs-ruby#
nix develop
bundle lock
bundix

Now you can add gems to the buildInputs and enable direnv. Reload the environment and you are ready to work with your chosen version of Ruby and associated Gems.

direnv allow <foldername>

Credit to Bob van der Linden <bobvanderlinden@gmail.com> for creating https://github.com/bobvanderlinden/nixpkgs-ruby