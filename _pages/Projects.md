---
title: ""
permalink: /projects/
toc: true
toc_label: "Projects"
toc_icon: "cog"
toc_sticky: true
---


# Machine Learning

## GANGogh

![music]( {{ "assets/images/gangogh.png"" | relative_url }})

*(2017 Independent research project supervised by [Professor Andrea Danyluk](http://www.cs.williams.edu/~andrea/)).*

Generative Adversarial Networks are comprised of two deep neural networks pitted against one another in a zero-sum game. The aim of this project was to use GANs to generate novel pieces of art. The model was trained in Tensorflow on a distribution of art pieces gathered from wikiart.org. Our architecture leveraged the power of the improved Wasserstein metric in an extension of the typical AC-GAN framework that allowed us to condition our models on painting genre. In order to induce our generator to focus on learning the differences between genres, we additionally employed global conditioning and pre-training of the discriminator. Beyond generating quality image samples in genres such as Flower Paintings and Landscapes, we also demonstrated that GANGogh produced an effective art genre classifier, as its discriminator reached precision values of over 90% on our wikiart dataset.

Blog | Code | Framework | Collaborator
--- | --- | --- | ---
 [Medium](https://towardsdatascience.com/gangogh-creating-art-with-gans-8d087d8f74a1) | [Github](https://github.com/rkjones4/GANGogh) | TensorFlow |  Derrick Bonafilia


## Music Genre Classification

![music]( {{ "assets/images/genre.png"" | relative_url }})

*(2016 Machine Learning final project supervised by [Professor Andrea Danyluk](http://www.cs.williams.edu/~andrea/)).* 

For our final project, we explored using deep neural networks to predict the music genre of a song. With audio files from the 1000 song GTZAN dataset, we chose to treat music genre identification as a pixel-based classification task by transforming audio files into spectrograms that visualized variations in frequencies over time. Compared to previous approaches in this space, we did not transform our image into a set of dense-features, but rather fed our raw images into a simple convolutional neural network.
Through a series of iterations on data pre-processing, architecture choices, and hyper-parameter searches, we created a model with over 85% cross-validation accuracy on 10 genres of music. As the GTZAN dataset generally has too few examples on which to train an accurate deep neural network, we came up with an approach of splitting 30 second song samples into many shorter examples at training time. At prediction time, these sub-song splits were then combined into a single genre prediction through a softmax voting mechanism over the sum of the output values for each split in the sample.

Framework | Collaborator
 --- | --- 
TensorFlow | Derrick Bonafilia

## Facebook - Social Good ML

![sg]( {{ "assets/images/sg.png"" | relative_url }})

*(2017+ Facebook Software Engineer).* 

Located within Facebook’s Social Good team, the Charitable Giving Machine Learning group has a mission to foster a global community of giving through increasing the distribution and efficiency of on-platform fundraising activity. My work has involved creating and improving a number of machine learning systems that span from News Feed classifiers to natural language processing models aimed to identify posts that indicate the intent to create a fundraiser. 
So far, the team has raised over 1 billion dollars through on platform donations. My efforts in this space have been responsible for over 25% of the team's top-line growth since I’ve joined the team and has helped millions of people across the globe raise funds for the causes that matter to them.

# Graphics

## Procedurally Generated Landscapes

![landscape]( {{ "assets/images/landscape.png"" | relative_url }})

*(2016 Graphics midterm project taught by [Professor Morgan McGuire](https://www.cs.williams.edu/~morgan/)).*

The goal of this project was to procedurally generate unique stylized low-polygon worlds that evoked imagery of the Irish countryside. The terrain was produced through a series of operations on various cuts of Perlin noise, which both Separated chunks of the world into different Biomes and produced the basis of the underlying mesh. To complete the stylized effect, we implemented a mesh simplification technique through point sampling based on the gradient of the terrain and triangulation methods. The final coloring of the mesh was based on a combination of Voronoi diagrams for the farmland and elevation and slope rules for the other Biomes. 

Report | Language/Framework | Collaborator(s)
--- | --- | ---
[Landscape Generation](https://www.cs.williams.edu/~morgan/cs371-f16/gallery/4-midterm/terrain/report.md.html) | C++/G3D | Melanie Subbiah, Yi-Tong Tseo, and Cole Erickson

## Simulating and Rending Water

![water]( {{ "assets/images/water.png"" | relative_url }})

*(2016 Graphics final project taught by [Professor Morgan McGuire](https://www.cs.williams.edu/~morgan/)).* 

Our project was designed to both simulate and render realistic representations of water. The PBD particle simulation was backed by NVIDIA’s FleX engine, which output both locations of permanent water particles and transitory foam that was formed when neighboring particles had kinetic energies that surpassed a given threshold. With each iteration of the particle engine, surface meshes were re-generated using the marching cubes algorithm. The final rendering was done using path-tracing, and took into account Beer-Lambert coloring, fake caustics, refraction, and reflection effects. 

Video | Code | Language/Framework | Collaborator(s) 
--- | --- | --- | -- 
[Water Video](https://www.youtube.com/watch?v=FS6nkQwO7pY) | [GitHub](https://github.com/YitongTseo/WaterSimulationAndRendering) | C++/G3D+Flex | Melanie Subbiah, Yi-Tong Tseo, and Cole Erickson

# Programming

## Encoding Information with Images and Memory

![valt]( {{ "assets/images/mindburnr.png"" | relative_url }})

*(2015 Summer Research Assistant working with [Professor Brent Heeringa](http://www.cs.williams.edu/~heeringa/)).*

Collaborated with Nola Gordon to help develop a prototype information protection system through error-sensitive encodings using recognizable images. Most of our work focused on building out multiple variants of the service that were used to validate the efficacy of potential approaches in a series of Amazon Mechanical Turk experiments. This project has since served as inspiration for [Valt](https://valt.io/), a company started by Professor Heeringa based on this line of investigation.

## Seam Carving

![sc]( {{ "assets/images/seam.png"" | relative_url }})

*(2014 Data Structures final project taught by [Professor Morgan McGuire](https://www.cs.williams.edu/~morgan/)).*

Implemented Avidan and Shamir’s Seam Carving Algorithm in C++. Created a python program that offered multiple low-energy calculation strategies and the ability to mark parts of an image as "to be conserved" or "to be removed". After this course-project, I created an Android app that used a more memory efficient (but slower) Seam Carving algorithm to create square images designed for Instagram. 

Report | Collaborator(s)
--- | ---
[Seam Carving](/pdfs/carving.pdf) | Zijie Zhu, Julia Goldman, Yiheng Zhang

## Customized A/B Testing Framework

![d3]( {{ "assets/images/deltoid.png"" | relative_url }})

*(2016 Software Engineering Intern at Facebook)*

Interned on the A/B testing platform [team](https://www.youtube.com/watch?v=Iw40wdwkkLA). Over the course of my internship, I worked full-stack (Python, PHP/Hack, SQL, Javascript) to build out a tool for ad-hoc statistical analysis of custom experiment data sets and integrated that tool into the existing infrastructure. It’s still widely used by many data scientist at Facebook today.
