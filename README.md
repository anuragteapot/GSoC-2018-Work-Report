<p align="center">
  <img width="556" height="112" src="https://github.com/Anu1601CS/GSoC-2018-Work-Report/blob/master/src/gsoc.png">
</p>

My proposal for **Improved Override Management** was selected as an project under **Google Summer of Code 2018**. I worked with the organisation [Joomla](https://github.com/joomla/). My mentors are **Astrid** ([@astridx](https://github.com/astridx)) **Allon Moritz** ([@laoneo](https://github.com/laoneo)) **zero-24** ([@zero-24](https://github.com/zero-24)).

## Goal

This project adds the feature to Joomla which check for upgrades, if the template file is changed where an override exists, it notifies the user that one of core file of his template overrides is changed with the update, to avoid security issues or functionality issue and he can adjust his override before anyone can notice.

## Results

Considering that we were able to meet all our planned goals, and also initiate the work on our additional goals, I'd say we were able to surpass the expectations of the project.

My first task under the official `GSoC` period was to implement the `Transposed Convolutional Layer` along with implementing a number of tests. Next, we also implemented the support for `Layer Normalization` and `Atrous Convolution Layers`. While completing the above tasks, I also uncovered a number of bugs in the implementation of the convolution toolbox, which was fixed alongside these tasks. The biggest milestone of Phase I was undoubtedly the completion of Kris' pending work on the standard `GAN` module, which was merged within a week from the Phase I. 

A lot of heavy lifting was done during Phase II as well. We decided on the idea of using the existing `GAN` module as a base for `DCGAN` and went ahead with directly testing a `DCGAN` network. While we were getting really good results with the stochastic implementations of the above architectures, it took almost ~72 hours for `GAN` and ~90 hours for `DCGAN` to converge on the full `MNIST` datasets. Thereon, we decided to work on optimizing our code for a couple of weeks, and as a result, we added the support for mini-batches in our `GAN` module. This allowed us to bring the training time under ~7 hours! This is almost ~1.5 times the speed of a `Tensorflow` network on the same input! Another major objective we achieved was the implementation of `Wasserstein GAN`, adding both the weight clipping and gradient-penalty variants. The work for optimizer separation was also taken under Phase II, and we were able to wrap up all our planned goals by the end of the second phase itself! Here are some images that we generated on the full 70,000 image `MNIST` dataset:


We spent most of our time during Phase III running experiments on different datasets, and implementing the long pending `RBM` and `Spike and Slab RBM` modules. I also spent some time optimizing the `ANN` infrastructure, which led to a ~30% speedup for the `FFN` and ~22% speedup for the `RNN` networks. I had a few other cool features in mind as well, but probably we'll be working on them after `GSoC` is over.

<p align="left">
  <img width="485" height="274" src="https://github.com/Anu1601cs/GSoC-2018-Work-Report/blob/master/src/mlpack.png">
</p>



### Links To Commits and Pull Requests

[Commits](https://github.com/joomla-projects/gsoc18_override_management/pulls?q=is%3Apr+author%3AAnu1601CS+is%3Aclosed)

[Quick icon in control panel.](https://github.com/joomla-projects/gsoc18_override_management/pull/39)

[New feature show status in each templates.](https://github.com/joomla-projects/gsoc18_override_management/pull/47)

[New api to support two form in one page.](https://github.com/joomla-projects/gsoc18_override_management/pull/36)

[List of updated override files in template manager.](https://github.com/joomla-projects/gsoc18_override_management/pull/30)

[Test and notification after update.](https://github.com/joomla-projects/gsoc18_override_management/pull/16)

[Implement the diff view and core file view in template manager.](https://github.com/joomla-projects/gsoc18_override_management/pull/9)

[Test and implementation of diff view.](https://github.com/joomla-projects/gsoc18_override_management/pull/6)

[Load correct core files of override files.](https://github.com/joomla-projects/gsoc18_override_management/pull/2)


## Conclusion

Joining Joomla and its community is a turning point in my life. Because it made me get familiar with the open source projects, how things deals and prepare for long term support and well as backward compatibility. I learned lot of things which I would have never learned without this project.

The success of this project is my mentors and the Joomla community, everyone helped me a lot in his field when I needed help. So, a special thanks to all for love and support :) 

And, I am also thankful to `Google` for the opportunity to work on this project, which helped me learn a lot in such a short period of time.
