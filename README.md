Steps reproduce an error:

```
cd gem3 && bundle install
> Bundle complete!

cd ../gem2 && bundle install
> Bundle complete!

cd ../gem1/ && bundle install
> Could not find gem 'gem3', which is required by gem 'gem2', in any of the sources.
```
Looks like the culprit is runtime dependency [here](https://github.com/vbyno/gems_path_example/blob/master/gem2/gem2.gemspec#L28-L29)
