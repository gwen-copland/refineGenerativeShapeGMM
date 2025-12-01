# refineGenerativeShapeGMM

This is a code to refine the generative model capabilities of Shape-based Gaussian Mixture Model, or ShapeGMM, to preform molecular modeling of unfolded protein structures. The code will have the user read an MD trajectory and necessary libraries into Jupyter Notebook, fit ShapeGMM to the data, fit the GMM object to a Kronecker State-Model, and create a new GMM object with minimized means and calculated Hessian from the minimized energies. gmm3n.py is a library that will store the proper covariances, weights, and means of the trejctory. 

---

✅ **Features**:

* An example of this generative model is run using alanine dipeptide.
  
---

## 📦 Installation

Directions to install

```bash
git clone https://github.com/mccullaghlab/vonMisesMixtureModel.git
cd vonMisesMixtureModel
pip install .
```

**Dependencies**:

* `numpy`
* `scipy`
* `shapeGMM`
* `pytest` (for running tests)

---

## 🧐 Usage

```python

```

---

## 🧠 API Overview

### `???`

Initialize the mixture model.

| Parameter      | Description                                   |
| -------------- | --------------------------------------------- |
| `n_components` | Number of clusters                            |
| `small_lambda` | Use small lambda approximation (default True) |
| `max_iter`     | Maximum EM iterations                         |
| `tol`          | Convergence threshold for log-likelihood      |
| `device`       | 'cuda' or 'cpu'                               |
| `verbose`      | Print progress during fitting                 |

---

### 🔧 Key Methods

| Method                        | Description                                            |
| ----------------------------- | ------------------------------------------------------ |
| `fit(data)`                   | Fit model to angular data of shape `(N, 2)`            |
| `predict(data)`               | Predict cluster assignments and compute log-likelihood |
| `ln_pdf(data)`                | Log-density under the fitted model                     |
| `pdf(data)`                   | Probability density under the fitted model             |
| `aic(data)`                   | Akaike Information Criterion                           |
| `bic(data)`                   | Bayesian Information Criterion                         |
| `icl(data)`                   | Integrated Complete Likelihood                         |
| `plot_scatter_clusters(data)` | Visualize 2D clusters                                  |

---

## 🛠️ Testing

To run the unit tests:

```bash
pytest tests/
```

---

## 🙌 Contributing

Contributions are welcome! Please open an issue or pull request if you'd like to contribute. A `CONTRIBUTING.md` will be added soon.

---

## 📄 License

This project is licensed under the MIT License. See [`LICENSE`](LICENSE) for details.

