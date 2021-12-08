# Summary

The project was to make a facial recognition machine learning program.  This program used the k nearest neighbors (kNN) algorithm.  The kNN algorithm finds the k nearest points to a test point and assigns the majority outcome of the neighbors to the test point classification.  

Since some datasets can be large, timing for running the project is important.  If one were to rely solely on Python "for loops", the kNN algorthm would not run to completion in a reasonable amout of time.  For a facial recognition program such a coding approach is not feasible; however, if one employs the speed of the numpy library then the machnine learning can be performed efficiently.  Timing of the differences in these approaches for a small dataset showed that the numpy approach was 1000 times faster than the naive Python "for loops" approach.

While there are different machine learning algorithms for facial recognition, this simple algorithm was able to acheive an accuracy of 95%.  