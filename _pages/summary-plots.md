---
title: "Project Summary"
layout: single
permalink: /summary/
author_profile: true
---
{% include toc %}

# Introduction

Neuroscience is the scientific study of the nervous system, a complex organ system inside every animal on planet Earth. Since its birth as a distinct scientific discipline in the 1950s and 1960s, neuroscience has concentrated its efforts on "interventionist" laboratory experiments with mice and rats, in which the experimenter manipulates some aspect of the nervous system and carefully observes the effects of that manipulation. This method has been very productive for the last 60 years, and has motivated the rapid development of ever more precise tools for physical and chemical manipulation of nervous system cells and molecules. Unfortunately, [these techniques have not been enough to meaningfully connect the cellular and molecular activity of nervous systems to the behaviour and well-being of whole organisms](https://www.cell.com/neuron/pdf/S0896-6273(16)31040-6.pdf). 

Several clues point to a need for neuroscience to expand its work out of the laboratory setting and "into the wild". Nervous systems evolved for millions of years into countless forms and in unknown, unpredictable environments before we built laboratories; yet, [the vast majority of brains we currently study are from only a few species which have been bred for generations in laboratory settings](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2605402/pdf/fnana-02-005.pdf). We are discovering that the [differences between an anaesthetized brain, a brain in a restrained animal, and a brain in a freely moving animal can be profound](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3184003/pdf/nihms-326476.pdf), even when studying neuroscience topics other than movement. We are also discovering that [nervous systems are incredibly sensitive to the details of both their immediate context and their past history](https://www.biorxiv.org/content/10.1101/058917v2). These clues, and more, have motivated me and my colleagues in the [Intelligent Systems Lab](http://www.kampff-lab.org/) to search for ways to validate laboratory results and techniques under more natural conditions and with larger, more diverse samples of research subjects. 

# "Surprising Minds": an experiment embedded in an exhibit

While looking for collaborators with whom I could study neuroscience topics in [cuttlefish](https://en.wikipedia.org/wiki/Cuttlefish), I developed a relationship with the Sea Life Centre in Brighton, UK, during the fall of 2016. I agreed to volunteer my time learning their marine animal husbandry procedures by helping with the daily tasks of maintaining the [Behind the Scenes](https://www.visitsealife.com/brighton/discover/behind-the-scenes-tour/) research laboratory space. In return, I would be allowed to conduct non-invasive behavioural experiments using their aquarium space, with newly hatched animals that the aquarium staff would help me raise. Unfortunately, no local cuttlefish eggs were found during the breeding seasons of 2017, and during the summer of 2017 a fault was found in one of the aquaculture systems, and the cuttlefish tanks had to be taken offline for repairs. 

When it became clear that I would not be able to proceed with cuttlefish behaviour experiments as planned, my PhD advisor, Dr. Adam Kampff, encouraged me to propose a behaviour experiment for humans which could take advantage of the huge quantity and diversity of people visiting the Sea Life Centre, especially during the summers when school groups from all around the world visited the aquarium. After meeting with Sea Life Brighton's display team and the communications manager at our London host institute, the Sainsbury Wellcome Centre, I was able to secure space and funding to develop and build an exhibit about intelligence, surprise, and how we can study neuroscience in both humans and cuttlefish. 

We decided to structure the experiment around eye-tracking, for two reasons. One is that both humans and cuttlefish have fluid-filled, camera-like eyes, and pay much more attention to what we see than to information from any other sense/sensor. The second reason is because changes to pupil size in response to light, surprise, and [cognitive load](https://en.wikipedia.org/wiki/Cognitive_load) have been well-studied under traditional laboratory conditions. We felt that by focusing on eye-tracking as a behavioural neuroscience method allowed us to talk about theoretical topics such as [convergent evolution](https://en.wikipedia.org/wiki/Convergent_evolution) of nervous systems across different species in addition to replicating and validating previous research with a much larger and diverse sample size. 

{% include figure image_path="/assets/images/PaperFigs/Fig1_OverallExhibitConceptDesign-01.jpg" alt="Overall exhibit concept and design" %}

During the first week of July 2017, "Surprising Minds" was installed next to the cuttlefish display tank in the [Victorian Arcade of the Sea Life Centre in Brighton](https://www.visitsealife.com/brighton/discover/aquarium-zones/). 

During July and August 2017, the exhibit was tended by a "host scientist", who invited visitors at the Sea Life Centre to interact with the exhibit, explained the experiment embedded in the exhibit, and engaged in discussions about neuroscience topics such as [optical illusions](https://en.wikipedia.org/wiki/Optical_illusion), [blindsight](https://en.wikipedia.org/wiki/Blindsight), and the [structure of the retina](https://en.wikipedia.org/wiki/Retina#Structure).

When visitors approached the exhibit, the host scientist invited them to look through the viewing plate and watch a 30 second long video clip while cameras record their eyes up close. Afterwards, the exhibit would replay the recording of their eyes so that visitors can see what their eyes do while they watch things. 

See Supplemental Figure 1a for details of the exhibit casing that held the experiment, including the original design of the viewing plate. 

{% include figure image_path="/assets/images/PaperFigs/Fig2a_ExperimentProtocol-01.jpg" alt="Experimental protocol" %}

Every time a visitor activated the exhibit by pressing a language button, three cameras were activated - the two infrared "eye cameras" housed in the viewing plate, which recorded people's eyes up close; and a usb web cam placed inside of the exhibit box, called the "world camera" or our "ground truth camera", which recorded the main display monitor inside the exhibit box. At the same time, the external monitors on the top and sides of the exhibit box would change to display the text "Do not disturb, Experiment in Progress".

See Supp. Fig. 1b for more documentation of the hardware components controlling the exhibit interaction and saving experiment data. 

{% include figure image_path="/assets/images/PaperFigs/Fig2b_ExperimentProtocolHardware-01.jpg" alt="Exhibit and experiment hardware setup" %}

After August 2017, the exhibit was briefly taken offline in order to enable the exhibit to run without a human host. The human host was replaced with informative text on the outside of the exhibit casing, and written directions for participating in the experiment were translated into 4 other languages besides English. See Supp. Fig. 1c and 1d for additional details on the upgrades made to the exhibit in order to automate the exhibit interaction and collection of experimental data. 

In order to analyse these videos, our analysis workflow needed to first synchronise all three videos, as the eye cameras and world camera ran at different frame rates. Then, for each frame in the eye recordings, our analysis workflow needed to find the pupil and measure the pupil's area and the center of the pupil's location in the frame. This information was then used to calculate changes in pupil size and motion. 

{% include figure image_path="/assets/images/PaperFigs/Fig3_AnalysisPipeline-01.jpg" alt="Analysis pipeline" %}

The exhibit turned out to be extremely popular. During the first month of automated data collection, the exhibit was activated 558 times, and by the time the exhibit had been running for a year, the exhibit had been activated a grand total of 24,641 times. 

Not everyone who activated the exhibit successfully completed the experiment. In the engagement plots below, a "good trial" is defined by whether or not our analysis workflow was able to reliably find and track a pupil throughout the experiment. If a pupil was not found by our algorithm for a stretch of 100 consecutive frames or longer, the entire trial was thrown out. 

{% include figure image_path="/assets/images/PaperFigs/Fig4a_EngagementByMonth-01.jpg" alt="Exhibit activations and visitor engagement, sorted by month" %}

{% include figure image_path="/assets/images/PaperFigs/Fig4b_EngagementByDayOfWeek-01.jpg" alt="Exhibit activations and visitor engagement, sorted by weekday" %}

As shown in figure 2a, each participant watched a calibration sequence, a unique video clip, and then a video clip of an octopus rapidly de-camouflaging. You can watch all six possible video experiences by scrolling to the bottom of this page, or by visiting [the Surprising Minds Stimuli YouTube playlist](https://www.youtube.com/playlist?list=PLQtAFaaG_zzwPUcP3q735-uooOP2_Eiz9){:target="_blank"}. 

Because the calibration sequence and octopus clip was experienced by all participants, we pooled calculations of changes in pupil size and motion across all "good trials" obtained for these sequences. The plots below show pupil size and motion from all the good trials obtained with the left eye camera (N=4407). 

{% include figure image_path="/assets/images/PaperFigs/Fig5a_PupilSizeCalibration-01.jpg" alt="Left pupil size during calibration sequence" %}



{% include figure image_path="/assets/images/PaperFigs/Fig5b_PupilSizeOctopus-01.jpg" alt="Left pupil size during octopus sequence" %}

{% include figure image_path="/assets/images/PaperFigs/Fig6a_PupilMotionCalibration-01.jpg" alt="Left pupil x-axis motion during calibration sequence" %}

{% include figure image_path="/assets/images/PaperFigs/Fig6b_PupilMotionOctopus-01.jpg" alt="Left pupil x-axis motion during octopus sequence" %}

{% include figure image_path="/assets/images/PaperFigs/Fig7a_PupilSizeMotionCalibration-01.jpg" alt="Left pupil, average size and average x-axis motion during calibration sequence" %}

{% include figure image_path="/assets/images/PaperFigs/Fig7b_PupilSizeMotionOctopus-01.jpg" alt="Left pupil, average size and average x-axis motion during octopus sequence" %}

{% include figure image_path="/assets/images/PaperFigs/Fig8a_InterestingMomentsOctopus-01.jpg" alt="Interesting moments in octopus sequence, found using population saccade statistics on left pupil x-axis motion" %}

{% include figure image_path="/assets/images/PaperFigs/Fig8b_InterestingMoments024-01.jpg" alt="Interesting moments in unique sequence 01, found using population saccade statistics on left pupil x-axis motion" %}

## Supplemental Figures

{% include figure image_path="/assets/images/PaperFigs/SuppFig1a_ExhibitBox-01.jpg" alt="Additional details on the fabrication of the exhibit" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig1b_ExhibitBox-01.jpg" alt="Additional details on the hardware inside the exhibit" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig1c_ExhibitBox-01.jpg" alt="Additional details on the improvements made in order to automate the exhibit" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig1d_ExhibitBox-01.jpg" alt="Additional details on the improvements made to the viewing port of the exhibit" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig2a_RightPupilSizeCalibration-01.jpg" alt="Right pupil size during calibration sequence" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig2b_RightPupilSizeOctopus-01.jpg" alt="Right pupil size during octopus sequence" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig2c_PupilSizeCircles-01.jpg" alt="Right and left pupil sizes during calibration and octopus sequences, as detected by the OpenCV method HoughCircles" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig3a_InterestingMoments025-01.jpg" alt="Interesting moments in unique sequence 02, found using population saccade statistics on left pupil x-axis motion" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig3b_InterestingMoments026-01.jpg" alt="Interesting moments in unique sequence 03, found using population saccade statistics on left pupil x-axis motion" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig3c_InterestingMoments027-01.jpg" alt="Interesting moments in unique sequence 04, found using population saccade statistics on left pupil x-axis motion" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig3d_InterestingMoments028-01.jpg" alt="Interesting moments in unique sequence 05, found using population saccade statistics on left pupil x-axis motion" %}

{% include figure image_path="/assets/images/PaperFigs/SuppFig3e_InterestingMoments029-01.jpg" alt="Interesting moments in unique sequence 06, found using population saccade statistics on left pupil x-axis motion" %}

## Exhibit Stimuli

{% include video id="1RNJI_5f50Y" provider="youtube" %}

{% include video id="cgJqYui9HZk" provider="youtube" %}

{% include video id="c2wdQVI8GF8" provider="youtube" %}

{% include video id="txw5nVIznRc" provider="youtube" %}

{% include video id="qdV6fI8M3M4" provider="youtube" %}

{% include video id="UFI8-j2xXpY" provider="youtube" %}

