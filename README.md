# Quantum-Linearized-Networks

Paper Link - https://www.researchgate.net/publication/393361459_SOTA_for_Image_Classification_using_Quantum_Linear_Circuits

Five Approaches have been tried to implement the algorithm discussed in paper - But only this one is working for now , and research is currently going on in the remaining
Approaches , but this CNN approach requires Quantum Features to work and hence demands the Classical Preprocessing via NN , a way which was not intended to be used ,
but unfortunately diverse training of unitary (as we dont yet how to cross corelate the unitaries - Because form our paper - Deterministic INrterpretation of NN we can safely say
NN are having (B**A)*d paths , where A is the number of piecewise linearities of the Activation Function and B is the size of the vector and d is the depth of the NN , with each path
leading to linear equation at the end , but the weights and biases for all path remain the same , it is only the range of element x and hence the piecewise fucntion that it approximates
changes ...) - We via the algorithm paper wanted to find the paths and crosscorelation to simulate this paths for given datasets manually , but more research is neede in this...
So for now we have implemented 2nd approach....    
) directly does not work given the features of train for test data , it tends to overfit .

# Five Approaches -

1. Separate UNitary for each sample vector of the training data to learn the feature vectors.
2. Quantum Features Extraction via CNN and then using Quantum Circuits for Future Inference - Draw Back - Train CNN needs to used to infer quantum features from New Test Data
3. SVM Scoring Approach - Multiunitary for different Classes and also for different data points within classes - Various Strategies of SVM - Works  - This can be a substitute to method 1 - Will be uploaded later 
4. Converting the Input Vector to VanderMonde Matrix (Various Polynomial Basis can be used) and then Making it unitary by Unitary Encoding - Research in Progress - But no any advantage in preliminary results  
5. Kernalization by addition of Features to the amplitude encocding - As MNIST is degree 2 dataset , so degree 2 features and cross realated Degree 1 features will suffice - Kernalization - Only Linear UNitary will 
 will be able to distinguish the Kernel Vectors into their respective classes , without any changes to the architecture.

Note - The final deployment on Quantum Computing will be U-Final-Classifier@U_Mappingforithsample@InputQubitGroundState , to do this one can refer the Quantum Basic Amplitude Encoding Code uploaded in the repository earlier.
