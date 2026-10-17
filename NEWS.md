# ModalCens 0.3.0

* Added the Log-t (`"logt"`) distribution family, in which the logarithm of
  the response follows a Student-t distribution. The mode is reparameterized
  in closed form, and the family supports right-censoring and randomized
  quantile residuals. It reduces to the Log-Normal family as the degrees of
  freedom grow.
* New argument `nu` in `modal_cens()` for the degrees of freedom of the Log-t
  family, treated as known (default `4`). It is ignored by the other families.
* `summary()` reports the degrees of freedom when `family = "logt"`, and the
  fitted object stores them in the new element `nu`.
* A warning is issued when the Log-t dispersion estimate lies at the boundary
  of the region that guarantees an interior mode.

# ModalCens 0.2.0

* Added the Log-Logistic (`"loglogistic"`) and Birnbaum-Saunders (`"bisa"`) distribution families, providing highly flexible modeling options outside the exponential family framework. Both support mode reparameterization, right-censoring, and randomized quantile residuals.
* Added a caveat in the documentation regarding the strong parametric restriction of the Inverse Gaussian distribution.
* Added the Log-Normal (`"lognormal"`) distribution family, with mode
  reparameterization, right-censoring support, and randomized quantile
  residuals.

# ModalCens 0.1.0

* Initial release on CRAN.
