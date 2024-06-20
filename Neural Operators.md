
### Fourier Neural Operator: 

https://arxiv.org/abs/2010.08895
https://youtu.be/IaS72aHrJKE?si=plDu6NodaIGWC3_Z

Basicallyis kind of taking a regular neural network layer added jpeg compression before it, and jpeg decompression after it, then built a network and trained it on navier stokes images to predict the next images. The reason i say jpeg is because the heart of jpeg is transforming an image into the frequency domain using a fourier-like function, the extra processing jpeg does is mostly non-destructive(duh you want your compressed version to be as close to the original), plus a neural network would probably not be impeded by the extra processing, and their method throws away some of the modes of the fourier transform too.

