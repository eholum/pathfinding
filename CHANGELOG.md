
v4.8.2 / 2024-01-14
==================

  * fix(dfs_reach): visit nodes in the documented order

v4.8.1 / 2024-01-07
==================

  * fix(yen): revert "Routes are already sorted by cost and path len"
  * test(yen): add test for checking Yen algorithm output ordering
  * chore(pre-commit): add conventional commit check
  * chore: use deprecate_until attribute instead of deprecated

v4.8.0 / 2023-12-22
==================

  * feat(matrix): add `Matrix::transpose()`
  * feat(matrix): add `Matrix::column_iter()`

v4.7.0 / 2023-12-21
==================

  * feat(grid): add `Grid::constrain()`
  * feat(matrix): add `Matrix::constrain()`
  * feat(utils): add `constrain()`

v4.6.0 / 2023-12-14
==================

  * feat(matrix): implement DoubleEndedIterator for RowIterator

v4.5.0 / 2023-12-14
==================

  * feat(matrix): add swap method
  * chore(msrv): update minimum required Rust version to 1.70.0
  * chore: use bool::is_some_and

v4.4.0 / 2023-11-30
==================

  * feat: new `dijkstra_reach()` function
  * fix(doc): remove useless explicit links

v4.3.4 / 2023-11-29
==================

  * fix(edmondskarp): better panic messages
  * fix(matrix): better panic messages
  * fix(style): apply clippy fixes
  * fix(doc): typo

v4.3.3 / 2023-11-13
==================

  * fix(yen): return all loopless paths
  * chore(cargo deny): fix warning in configuration file
  * chore(deps): update rust crate indexmap to 2.1.0
  * chore(deps): update rust crate thiserror to 1.0.50
  * chore(deps): update rust crate regex to 1.10.2
  * chore(deps): update rust crate num-traits to 0.2.17

v4.3.2 / 2023-09-22
==================

  * New remaining_low_bounds() method for {Bfs,Dfs}Reachable
  * Migrate to the evenfurther GitHub organization
  * fix(deps): update rust crate thiserror to 1.0.48
  * Use or_default() in test

v4.3.1 / 2023-08-02
==================

  * Move `cycle_detection` module into `directed` and deprecate the former
  * Update indexmap requirement from 1.9.2 to 2.0.0
  * Style: use `or_default()` rather than `or_insert_with()` with default value
  * Style: do not use `bool::then()` in `filter_map()`
  * Style: make `partial_cmp` use `cmp`
  * Style: reformat with let/else support
  * Use codspeed-criterion-compat everywhere, do not require criterion

v4.3.0 / 2023-05-30
==================

  * Allow creating a Matrix based on a function from position to value
  * Make method cancel_flow of edmondskarp only cancel the minimum amount of flow among all edges along a path, instead of the maximum, in order to avoid negative flows
  * Use sort_unstable_by() instead of sort_unstable_by_key()
  * New Grid example for from_coordinates() method
  * Use RemSP and path splitting
  * Remove optimization which gives worst benchmark results
  * Integrate CodSpeed
  * Update criterion requirement from 0.4.0 to 0.5.1
  * Make Kuhn-Munkres benchmarks reproducible

v4.2.1 / 2023-01-17
==================

  * Document that A*/Dijkstra/Fringe/idA* costs must be non-negative
  * Upgrade dependencies
  * Use new clippy lint name
  * Add bench for separate_components
  * Bench Kuhn-Munkres algorithm
  * Remove itertools dependency
  * Remove unnecessary .into_iter() in tests

v4.2.0 / 2022-12-25
==================

  * Add Grid::from_coordinates()
  * Add the possibility to display the grid with reversed line order
  * Add more Grid documentation

v4.1.1 / 2022-12-14
==================

  * Better performances in Grid, Kruskal and Edmonds-Karp

v4.1.0 / 2022-12-14
==================

  * Add Matrix::items() and Matrix::items_mut()
  * Rename Matrix::indices() as Matrix::keys() and deprecate Matrix::indices()
  * Clarify the ordering of coordinate tuples in Matrix
  * Add more Grid documentation
  * Enable clippy pedantic mode by default

v4.0.1 / 2022-12-12
==================

  * Improve bfs performance
  * Add documentation for possible errors and panics

v4.0.0 / 2022-11-30
==================

  * Add move_in_direction and in_direction to utils
  * Make some function const
  * Cleanups
  * Count paths
  * Add minimum_cut capability to EdmondsKarp
  * Bump MSRV to 1.65.0
  * Update dependencies

v3.0.14 / 2022-10-03
==================

  * Use into_keys() where appropriate
  * Add fake regex dev dependency
  * Use boolean::then_some()
  * Update criterion requirement from 0.3.4 to 0.4.0
  * Optimize Yen's algorithm
  * Routes are already sorted by cost and path len

v3.0.13 / 2022-06-16
==================

  * Document possibility of looping endlessly in kuhn_munkres related functions
  * Use matches!() to simplify expression

v3.0.12 / 2022-04-13
==================

  * Add two algorithms (Floyd and Brent) to detect cycles
  * Deprecate absdiff() in favor of Rust 1.60 abs_diff()
  * Remove double must-use

v3.0.11 / 2022-03-11
==================

  * Introduce `Grid::{bfs,dfs}_reachable()` and `deprecate Grid::reachable()`
  * Remove `Copy` bound on predicate of `Matrix::{bfs,dfs}_reachable()`
  * Use anonymous lifetimes when appropriate
  * Add example for `kuhn_munkres()`

v3.0.10 / 2022-02-14
====================

  * Remove unused `Matrix::uninit`/`Matrix::assume_init()`
  * Remove remaining `debug_assert!()` calls

v3.0.9 / 2022-02-02
===================

  * Add conversion from `Matrix<bool>` to `Grid`
  * Add `Grid` equality
  * Add `Matrix::map()`

v3.0.8 / 2022-01-24
===================

  * Add `Matrix::new_uninit()` and `Matrix::assume_init()`
  * Forbid all missing or partially missing docs
  * Mark iterators as fused

v3.0.7 / 2022-01-23
===================

  * Deprecate `Matrix::reachable()` for `Matrix::bfs_reachable(`) and
    `Matrix::dfs_reachable()`
  * Add `dfs_reach()`
  * Use an enumeration to represent `MatrixFormatError`

v3.0.6 / 2022-01-12
===================

  * Add MSRV and check for consistency
  * Add `#[must_use]` on `Weights` trait
  * Use thiserror crate to build `MatrixFormatError`
  * Add an example for `Grid` as `Debug`

v3.0.5 / 2021-12-13
===================

  * Alternate `Grid` debug mode

v3.0.4 / 2021-12-12
===================

  * Add `Grid::reachable()`
  * Add `Matrix::get()` and `Matrix::get_mut()`

v3.0.3 / 2021-12-09
===================

  * Add `Matrix::reachable()`
  * Better `Matrix` corner cases documentation

v3.0.2 / 2021-12-09
===================

  * Remove references in `Grid` methods
  * Remove more references in `Matrix` methods

v3.0.1 / 2021-12-09
===================

  * Remove unnecessary `Clone` bounds

v3.0.0 / 2021-12-09
===================

  * Use tuples instead of tuples reference for `Matrix` index
