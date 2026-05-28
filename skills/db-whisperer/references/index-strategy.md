# Index Strategy Reference

1. Start from a real query plan, not a guess.
2. Index columns used by selective filters before columns used only for output.
3. For composite indexes, put equality predicates before range predicates.
4. Match index order to common `ORDER BY` clauses when it avoids sorting.
5. Avoid indexes on very low-cardinality columns unless paired with a selective column.
6. Prefer partial indexes when only a subset of rows is queried often.
7. Use covering indexes for hot reads only when added write cost is acceptable.
8. Remove duplicate and unused indexes after verifying usage metrics.
9. Every new index slows writes and consumes cache; justify it with workload data.
10. On Postgres, use `CREATE INDEX CONCURRENTLY` for production-sized tables.
11. On MySQL, check online DDL support for the engine and version.
12. On SQLite, index creation blocks writes; schedule it deliberately.
13. On MongoDB, align compound index order with equality, sort, and range needs.
14. Do not index every foreign key blindly; inspect actual access patterns.
15. Validate with before/after plans and representative row counts.
16. Watch for stale statistics; run analyze when estimates are clearly wrong.
17. Avoid expression indexes unless the query uses the same expression.
18. Treat unique indexes as data constraints, not only performance tools.
19. For large backfills, add indexes after bulk load when possible.
20. Document the query each index exists to support.
21. Recheck index value after product behavior or filters change.
