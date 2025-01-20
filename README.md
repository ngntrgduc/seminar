My Seminar coursework at the University of Science - VNUHCM, 2024.

- **Topic**: Handling Missing Data (Xử lý dữ liệu khuyết)
- **Language**: Vietnamese
- **Supervisor**: [Dr. Hoang Van Ha](https://sites.google.com/view/hoangvanha/)
<!-- - **Graded**:  -->
<!-- - **Summary**: Đề tài nghiên cứu các phương pháp xử lý dữ liệu khuyết cho mô hình hồi quy tuyến tính. Nội dung chính của đề tài là nghiên cứu về dự đoán Bayes đối với các cơ chế dữ liệu khuyết khác nhau, bao gồm MCAR, MAR và MNAR. Tiếp theo, đề tài đề xuất sử dụng mạng thần kinh (neural network) để xử lý mô hình với dữ liệu khuyết. -->

### Overview
In this course, I try to understand, rephrase, and implement the neural network from the paper ["NeuMiss networks: differentiable programming for supervised learning with missing values"](https://proceedings.neurips.cc/paper/2020/hash/42ae1544956fbe6e09242e6cd752444c-Abstract.html) (NeurIPS 2020). 
Though the paper still contains some small errors, this is still an interesting work that focuses on handling missing data in linear regression problems by using a neural network, so-called NeuMiss.

### Repo's structure
- `notebooks/`: Contain Jupyter notebooks to demonstrate some experiments
   - `Neumann_series_approximation.ipynb`: Numerical experiment for matrix inverse approximation using Neumann series
   - `NeuMiss_network.ipynb`: Reimplement NeuMiss network architecture and some experiments with different settings
   - `NeuMiss_sota_network.ipynb`: Testing NeuMiss from authors' later work:  ["What’s a good imputation to predict with missing values?"](https://papers.nips.cc/paper/2021/file/5fe8fdc79ce292c39c5f209d734b7206-Paper.pdf) (2021)
   - `NeuMiss_vs_Others.ipynb`: Experimenting with other impute-then-regress methods
- `report/`: Contain [report's pdf](/report/Seminar.pdf) and LaTeX code
- `slide/`: Contain [slide's pdf](/slide/slide.pdf) and LaTeX code


### Further works
Due to my skill issues, and the shortage of time ⌛, I could not do and learn more in this course 🥲. However, here are some ideas/questions/todos I wish I had time to work on:
- Make the network work on GPU
- Research on better architecture from authors' later work
   - Implement functionality for classification problem
- The assumption for data (Gaussian), MNAR setting (Gaussian self-masking), and other assumptions are still strong/restrictive.
   - Integrated with Random Matrix Theory (?) -> Remove the assumption for Gaussian data.
   - Agnostic statistics/Agnostic learning (?)
- Compare to more methods: 
   - Mixture of models: Gaussians Mixture Model (GMM)
   - Hierarchical models
   - Imputations: Optimal Transport, PCA, Matrix Completion,...
   - Neural Network models: GAIN, MisGAN, MIWAE, [StableMiss](https://arxiv.org/abs/2305.11197),...
   - NeuMiss (Morvan et al. - 2021): NeuMiss can be used for non-linear models by joining it with a MLP,...
   - [NeuMISE](https://arxiv.org/abs/2406.16484): For missingness shift (or can be view as data drift/shift) -> Use for realtime application?
- This network is considered a deep neural network. What if there's a small amount of data? Then which method is the best?
- Experiment with more real-world datasets, with linear regression problems
- How can NeuMiss be extended to work on large datasets?
- How do outliers affect the model performance?
- How do categorical variables and continuous variables affect the network?

### Resources:
- https://github.com/marineLM/NeuMiss (The architecture I reimplemented is the same as this)
- https://github.com/marineLM/NeuMiss_sota
- [NeuMiss' poster](https://marinelm.github.io/files/Neurips2020_poster.pdf)
- [NeuMiss' slide](https://marinelm.github.io/files/20201207_Montpellier_NeuMiss.pdf)
- [Supervised learning with missing values - Julie Josse](https://juliejosse.com/wp-content/uploads/2022/06/ecosseNovember2020.pdf)
- http://bigdatasummerinst.sph.umich.edu/wiki2022/images/1/1d/Missing_Data.pdf
