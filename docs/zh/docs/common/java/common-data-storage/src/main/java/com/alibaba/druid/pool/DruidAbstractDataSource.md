# 基础信息

|      |      |
|------|------|
| 名称 | DruidAbstractDataSource |
| 编码语言 | .java |
| 代码路径 | WeFe/common/java/common-data-storage/src/main/java/com/alibaba/druid/pool/DruidAbstractDataSource.java |
| 包名 | com.alibaba.druid.pool |
| 依赖项 | ['com.alibaba.druid.DruidRuntimeException', 'com.alibaba.druid.filter.Filter', 'com.alibaba.druid.filter.FilterChainImpl', 'com.alibaba.druid.filter.FilterManager', 'com.alibaba.druid.pool.vendor.NullExceptionSorter', 'com.alibaba.druid.proxy.jdbc.DataSourceProxy', 'com.alibaba.druid.proxy.jdbc.TransactionInfo', 'com.alibaba.druid.stat.JdbcDataSourceStat', 'com.alibaba.druid.stat.JdbcSqlStat', 'com.alibaba.druid.stat.JdbcStatManager', 'com.alibaba.druid.support.logging.Log', 'com.alibaba.druid.support.logging.LogFactory', 'com.alibaba.druid.util', 'javax.management.JMException', 'javax.management.ObjectName', 'javax.management.openmbean.CompositeDataSupport', 'javax.security.auth.callback.NameCallback', 'javax.security.auth.callback.PasswordCallback', 'javax.sql.DataSource', 'java.io.PrintWriter', 'java.io.Serializable', 'java.sql', 'java.util.Date', 'java.util', 'java.util.concurrent.CopyOnWriteArrayList', 'java.util.concurrent.ScheduledExecutorService', 'java.util.concurrent.atomic.AtomicIntegerFieldUpdater', 'java.util.concurrent.atomic.AtomicLongFieldUpdater', 'java.util.concurrent.locks.Condition', 'java.util.concurrent.locks.ReentrantLock', 'java.util.logging.Logger'] |
| 概述说明 |  |

# 说明



# 类列表 Class Summary

| 名称   | 类型  | 说明 |
|-------|------|-------------|
| DruidAbstractDataSource | class |  |



## 类 DruidAbstractDataSource

|      |      |
|------|------|
| 访问范围 | public abstract |
| 类型 | class |
| 名称 | DruidAbstractDataSource |
| 说明 |  |


### UML类图




### 内部方法调用关系图



### 字段列表 Field List

| 名称  | 类型  | 说明 |
|-------|-------|------|
| destroyCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "destroyCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| cachedPreparedStatementDeleteCount = 0L | long |  |
| errorCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "errorCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| DEFAULT_MAX_WAIT = -1 | int |  |
| DEFAULT_TEST_ON_RETURN = false | boolean |  |
| creatingCountUpdater = AtomicIntegerFieldUpdater.newUpdater(DruidAbstractDataSource.class, "creatingCount") | AtomicIntegerFieldUpdater<DruidAbstractDataSource> |  |
| cachedPreparedStatementCount = 0L | long |  |
| inited = false | boolean |  |
| maxPoolPreparedStatementPerConnectionSize = 10 | int |  |
| createErrorCountUpdater = AtomicIntegerFieldUpdater.newUpdater(DruidAbstractDataSource.class, "createErrorCount") | AtomicIntegerFieldUpdater<DruidAbstractDataSource> |  |
| onFatalErrorMaxActive = 0 | int |  |
| sharePreparedStatements = false | boolean |  |
| initedTime | Date |  |
| maxIdle = DEFAULT_MAX_IDLE | int |  |
| onFatalError = false | boolean |  |
| executeCount = 0L | long |  |
| statementIdSeedUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "statementIdSeed") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| breakAfterAcquireFailure = false | boolean |  |
| isMySql = false | boolean |  |
| minIdle = DEFAULT_MIN_IDLE | int |  |
| isOracle = false | boolean |  |
| connectionIdSeedUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "connectionIdSeed") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| timeBetweenLogStatsMillis | long |  |
| fatalErrorCount = 0 | int |  |
| useLocalSessionState = true | boolean |  |
| phyMaxUseCount = -1 | long |  |
| initVariants = false | boolean |  |
| defaultCatalog = null | String |  |
| phyTimeoutMillis = DEFAULT_PHY_TIMEOUT_MILLIS | long |  |
| resultSetIdSeed = 50000L | long |  |
| cachedPreparedStatementDeleteCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "cachedPreparedStatementDeleteCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| failContinuous = 0 | int |  |
| dupCloseCount = 0L | long |  |
| statLogger = new DruidDataSourceStatLoggerImpl() | DruidDataSourceStatLogger |  |
| driver | Driver |  |
| timeBetweenEvictionRunsMillis = DEFAULT_TIME_BETWEEN_EVICTION_RUNS_MILLIS | long |  |
| dbType | String |  |
| validationQuery = DEFAULT_VALIDATION_QUERY | String |  |
| DEFAULT_MIN_IDLE = 0 | int |  |
| createStartNanos = 0L | long |  |
| initExceptionThrow = true | boolean |  |
| DEFAULT_MAX_IDLE = 8 | int |  |
| createStartNanosUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "createStartNanos") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| preparedStatementCount = 0L | long |  |
| poolPreparedStatements = false | boolean |  |
| destroyCount = 0L | long |  |
| dupCloseCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "dupCloseCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| DEFAULT_MAX_ACTIVE_SIZE = 8 | int |  |
| cachedPreparedStatementHitCount = 0L | long |  |
| testWhileIdle = DEFAULT_WHILE_IDLE | boolean |  |
| rollbackCount = 0L | long |  |
| directCreateCount = 0 | int |  |
| useUnfairLock = null | Boolean |  |
| testOnReturn = DEFAULT_TEST_ON_RETURN | boolean |  |
| commitCount = 0L | long |  |
| DEFAULT_INITIAL_SIZE = 0 | int |  |
| closedPreparedStatementCount = 0L | long |  |
| LOG = LogFactory.getLog(DruidAbstractDataSource.class) | Log |  |
| creatingCount = 0 | int |  |
| startTransactionCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "startTransactionCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| testOnBorrow = DEFAULT_TEST_ON_BORROW | boolean |  |
| startTransactionCount = 0L | long |  |
| createErrorCount = 0 | int |  |
| metaDataIdSeedUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "metaDataIdSeed") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| serialVersionUID = 1L | long |  |
| activeConnectionLock = new ReentrantLock() | ReentrantLock |  |
| createCount = 0L | long |  |
| notFullTimeoutRetryCount = 0 | int |  |
| transactionIdSeedUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "transactionIdSeed") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| createdTime = new Date() | Date |  |
| maxWait = DEFAULT_MAX_WAIT | long |  |
| resultSetIdSeedUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "resultSetIdSeed") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| transactionThresholdMillis = 0L | long |  |
| lastCreateStartTimeMillis | long |  |
| id | long |  |
| maxActive = DEFAULT_MAX_ACTIVE_SIZE | int |  |
| metaDataIdSeed = 80000L | long |  |
| useOracleImplicitCache = true | boolean |  |
| maxWaitThreadCount = -1 | int |  |
| validationQueryTimeout = -1 | int |  |
| lastCreateErrorTimeMillis | long |  |
| PRESENT = new Object() | Object |  |
| initialSize = DEFAULT_INITIAL_SIZE | int |  |
| transactionIdSeed = 60000L | long |  |
| errorCount = 0L | long |  |
| logWriter = new PrintWriter(System.out) | PrintWriter |  |
| lastCreateError | Throwable |  |
| activeConnections = new IdentityHashMap<DruidPooledConnection, Object>() | Map<DruidPooledConnection, Object> |  |
| statementIdSeed = 20000L | long |  |
| lastErrorTimeMillis | long |  |
| validConnectionChecker = null | ValidConnectionChecker |  |
| connectionErrorRetryAttempts = 1 | int |  |
| connectProperties = new Properties() | Properties |  |
| connectionIdSeed = 10000L | long |  |
| lock | ReentrantLock |  |
| timeBetweenConnectErrorMillis = DEFAULT_TIME_BETWEEN_CONNECT_ERROR_MILLIS | long |  |
| driverClassLoader | ClassLoader |  |
| createError | Throwable |  |
| lastFatalError = null | Throwable |  |
| passwordCallback | PasswordCallback |  |
| driverClass | String |  |
| executeCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "executeCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| jdbcUrl | String |  |
| logAbandoned | boolean |  |
| executeBatchCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "executeBatchCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| password | String |  |
| removeAbandonedTimeoutMillis = 300 * 1000 | long |  |
| maxOpenPreparedStatements = -1 | int |  |
| notEmpty | Condition |  |
| executeUpdateCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "executeUpdateCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| lastError | Throwable |  |
| initGlobalVariants = false | boolean |  |
| failContinuousUpdater = AtomicIntegerFieldUpdater.newUpdater(DruidAbstractDataSource.class, "failContinuous") | AtomicIntegerFieldUpdater<DruidAbstractDataSource> |  |
| defaultTransactionIsolation | Integer |  |
| name | String |  |
| executeQueryCount = 0L | long |  |
| objectName | ObjectName |  |
| keepAliveBetweenTimeMillis = DEFAULT_TIME_BETWEEN_EVICTION_RUNS_MILLIS * 2 | long |  |
| connectionInitSqls | List<String> |  |
| failContinuousTimeMillisUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "failContinuousTimeMillis") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| defaultReadOnly | Boolean |  |
| dupCloseLogEnable = false | boolean |  |
| maxEvictableIdleTimeMillis = DEFAULT_MAX_EVICTABLE_IDLE_TIME_MILLIS | long |  |
| fatalErrorCountLastShrink = 0 | int |  |
| removeAbandoned | boolean |  |
| createScheduler | ScheduledExecutorService |  |
| defaultAutoCommit = true | boolean |  |
| empty | Condition |  |
| transactionHistogram = new Histogram(1,            10,            100,            1000,            10 * 1000,            100 * 1000) | Histogram |  |
| executeUpdateCount = 0L | long |  |
| minEvictableIdleTimeMillis = DEFAULT_MIN_EVICTABLE_IDLE_TIME_MILLIS | long |  |
| destroyScheduler | ScheduledExecutorService |  |
| DEFAULT_PHY_TIMEOUT_MILLIS = -1 | long |  |
| cachedPreparedStatementMissCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "cachedPreparedStatementMissCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| numTestsPerEvictionRun = DEFAULT_NUM_TESTS_PER_EVICTION_RUN | int |  |
| failContinuousTimeMillis = 0L | long |  |
| accessToUnderlyingConnectionAllowed = true | boolean |  |
| lastFatalErrorTimeMillis = 0 | long |  |
| userCallback | NameCallback |  |
| DEFAULT_MIN_EVICTABLE_IDLE_TIME_MILLIS = 1000L * 60L * 30L | long |  |
| filters = new CopyOnWriteArrayList<Filter>() | List<Filter> |  |
| cachedPreparedStatementCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "cachedPreparedStatementCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| failFast = false | boolean |  |
| DEFAULT_NUM_TESTS_PER_EVICTION_RUN = 3 | int |  |
| DEFAULT_MAX_EVICTABLE_IDLE_TIME_MILLIS = 1000L * 60L * 60L * 7 | long |  |
| executeBatchCount = 0L | long |  |
| closedPreparedStatementCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "closedPreparedStatementCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| maxCreateTaskCount = 3 | int |  |
| username | String |  |
| transactionQueryTimeout | int |  |
| DEFAULT_TIME_BETWEEN_CONNECT_ERROR_MILLIS = 500 | long |  |
| preparedStatementCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "preparedStatementCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| asyncCloseConnectionEnable = false | boolean |  |
| queryTimeout | int |  |
| DEFAULT_TIME_BETWEEN_EVICTION_RUNS_MILLIS = 60 * 1000L | long |  |
| cachedPreparedStatementHitCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "cachedPreparedStatementHitCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| DEFAULT_WHILE_IDLE = true | boolean |  |
| executeQueryCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "executeQueryCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| rollbackCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "rollbackCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| exceptionSorter = null | ExceptionSorter |  |
| createTimespan | long |  |
| commitCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "commitCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| clearFiltersEnable = true | boolean |  |
| DEFAULT_TEST_ON_BORROW = false | boolean |  |
| createCountUpdater = AtomicLongFieldUpdater.newUpdater(DruidAbstractDataSource.class, "createCount") | AtomicLongFieldUpdater<DruidAbstractDataSource> |  |
| lastFatalErrorSql = null | String |  |
| cachedPreparedStatementMissCount = 0L | long |  |
| DEFAULT_VALIDATION_QUERY = null | String |  |
| directCreateCountUpdater = AtomicIntegerFieldUpdater.newUpdater(DruidAbstractDataSource.class, "directCreateCount") | AtomicIntegerFieldUpdater<DruidAbstractDataSource> |  |

### 方法列表

| 名称  | 类型  | 说明 |
|-------|-------|------|
| getUsername | String |  |
| setName | void |  |
| isInitVariants | boolean |  |
| getDriverClassName | String |  |
| getCreatedTime | Date |  |
| isLogAbandoned | boolean |  |
| setCreateScheduler | void |  |
| setValidationQuery | void |  |
| setRemoveAbandoned | void |  |
| incrementStartTransactionCount | void |  |
| getMaxPoolPreparedStatementPerConnectionSize | int |  |
| setPoolPreparedStatements | void |  |
| setUsername | void |  |
| incrementCachedPreparedStatementHitCount | void |  |
| isPoolPreparedStatements | boolean |  |
| validateConnection | void |  |
| getPreparedStatementCount | long |  |
| getCachedPreparedStatementAccessCount | long |  |
| getProxyFilters | List<Filter> |  |
| incrementPreparedStatementCount | void |  |
| incrementExecuteBatchCount | void |  |
| getLogWriter | PrintWriter |  |
| setInitVariants | void |  |
| testConnectionInternal | boolean |  |
| getDefaultReadOnly | Boolean |  |
| setExceptionSorterClassName | void |  |
| setFilters | void |  |
| incrementClosedPreparedStatementCount | void |  |
| setDriverClassLoader | void |  |
| setDefaultAutoCommit | void |  |
| incrementExecuteUpdateCount | void |  |
| setInitialSize | void |  |
| incrementExecuteQueryCount | void |  |
| isAccessToUnderlyingConnectionAllowed | boolean |  |
| getLastCreateError | Throwable |  |
| getTimeBetweenEvictionRunsMillis | long |  |
| getAndResetExecuteCount | long |  |
| getInitialSize | int |  |
| getCachedPreparedStatementHitCount | long |  |
| setNumTestsPerEvictionRun | void |  |
| getValidationQueryTimeout | int |  |
| isUseUnfairLock | boolean |  |
| getRollbackCount | long |  |
| getPassword | String |  |
| isRemoveAbandoned | boolean |  |
| getNumTestsPerEvictionRun | int |  |
| getMaxWaitThreadCount | int |  |
| setPhyMaxUseCount | void |  |
| getPhyMaxUseCount | long |  |
| setPhyTimeoutMillis | void |  |
| setMaxWaitThreadCount | void |  |
| getPhyTimeoutMillis | long |  |
| setMaxEvictableIdleTimeMillis | void |  |
| setMaxCreateTaskCount | void |  |
| getMaxEvictableIdleTimeMillis | long |  |
| getMaxCreateTaskCount | int |  |
| getUserCallback | NameCallback |  |
| setKeepAliveBetweenTimeMillis | void |  |
| getValidationQuery | String |  |
| isInited | boolean |  |
| getConnectProperties | Properties |  |
| getKeepAliveBetweenTimeMillis | long |  |
| setDestroyScheduler | void |  |
| setMinEvictableIdleTimeMillis | void |  |
| getDestroyScheduler | ScheduledExecutorService |  |
| getCreateScheduler | ScheduledExecutorService |  |
| setAsyncCloseConnectionEnable | void |  |
| isAsyncCloseConnectionEnable | boolean |  |
| discardConnection | void |  |
| getMaxOpenPreparedStatements | int |  |
| setLogAbandoned | void |  |
| discardConnection | void |  |
| setTimeBetweenConnectErrorMillis | void |  |
| cloneTo | void |  |
| getTimeBetweenConnectErrorMillis | long |  |
| closePreapredStatement | void |  |
| setConnectionInitSqls | void |  |
| getParentLogger | Logger |  |
| getRemoveAbandonedTimeout | int |  |
| getConnectionInitSqls | Collection<String> |  |
| getProperties | String |  |
| addConnectionProperty | void |  |
| getRawDriverMinorVersion | int |  |
| setDbType | void |  |
| getRawDriverMajorVersion | int |  |
| getDbType | String |  |
| setRemoveAbandonedTimeout | void |  |
| setPasswordCallbackClassName | void |  |
| setValidConnectionCheckerClassName | void |  |
| getValidConnectionCheckerClassName | String |  |
| getCompositeData | CompositeDataSupport |  |
| setValidConnectionChecker | void |  |
| initPhysicalConnection | void |  |
| getMinEvictableIdleTimeMillis | long |  |
| getValidConnectionChecker | ValidConnectionChecker |  |
| setRemoveAbandonedTimeoutMillis | void |  |
| getID | long |  |
| recycle | void |  |
| setSharePreparedStatements | void |  |
| handleConnectionException | void |  |
| isSharePreparedStatements | boolean |  |
| handleConnectionException | void |  |
| setMaxPoolPreparedStatementPerConnectionSize | void |  |
| initPhysicalConnection | void |  |
| initStatement | void |  |
| getRemoveAbandonedTimeoutMillis | long |  |
| incrementDupCloseCount | void |  |
| createTransactionId | long |  |
| createResultSetId | long |  |
| createMetaDataId | long |  |
| getActivePeak | int |  |
| getStartTransactionCount | long |  |
| createStatementId | long |  |
| incrementRollbackCount | void |  |
| createConnectionId | long |  |
| setClearFiltersEnable | void |  |
| createPhysicalConnection | Connection |  |
| setTransactionQueryTimeout | void |  |
| incrementCommitCount | void |  |
| getMaxIdle | int |  |
| isClearFiltersEnable | boolean |  |
| getCommitCount | long |  |
| isBreakAfterAcquireFailure | boolean |  |
| setMinIdle | void |  |
| setMaxActive | void |  |
| setUseLocalSessionState | void |  |
| getRawDriver | Driver |  |
| getTransactionHistogramRanges | long[] |  |
| getMinIdle | int |  |
| setOracle | void |  |
| getCreateTimespanMillis | long |  |
| getTransactionHistogramValues | long[] |  |
| setNotFullTimeoutRetryCount | void |  |
| getExecuteCount | long |  |
| createPhysicalConnection | PhysicalConnectionInfo |  |
| getCreateTimespanNano | long |  |
| isOracle | boolean |  |
| setBreakAfterAcquireFailure | void |  |
| logTransaction | void |  |
| getNotFullTimeoutRetryCount | int |  |
| getActiveConnectionStackTrace | List<String> |  |
| setTransactionThresholdMillis | void |  |
| getStatLogger | DruidDataSourceStatLogger |  |
| getCachedPreparedStatementMissCount | long |  |
| setMaxWait | void |  |
| getActiveConnections | Set<DruidPooledConnection> |  |
| getTransactionThresholdMillis | long |  |
| getMaxWait | long |  |
| testConnectionInternal | boolean |  |
| setValidationQueryTimeout | void |  |
| setCreateError | void |  |
| getConnectionErrorRetryAttempts | int |  |
| isUseLocalSessionState | boolean |  |
| setExceptionSorter | void |  |
| setStatLoggerClassName | void |  |
| setQueryTimeout | void |  |
| setExceptionSorter | void |  |
| incrementCachedPreparedStatementMissCount | void |  |
| getExceptionSorterClassName | String |  |
| getQueryTimeout | int |  |
| setMaxOpenPreparedStatements | void |  |
| setUserCallback | void |  |
| getExecuteUpdateCount | long |  |
| incrementCachedPreparedStatementDeleteCount | void |  |
| getExceptionSorter | ExceptionSorter |  |
| setStatLogger | void |  |
| setFailContinuous | void |  |
| decrementCachedPreparedStatementCount | void |  |
| getDriverMinorVersion | int |  |
| setProxyFilters | void |  |
| setPasswordCallback | void |  |
| getDupCloseCount | long |  |
| incrementCachedPreparedStatementCount | void |  |
| getDriverMajorVersion | int |  |
| getCachedPreparedStatementDeleteCount | long |  |
| getPasswordCallback | PasswordCallback |  |
| getTransactionHistogram | Histogram |  |
| setDriver | void |  |
| setDefaultCatalog | void |  |
| getTimeBetweenLogStatsMillis | long |  |
| setObjectName | void |  |
| getDriver | Driver |  |
| getDefaultCatalog | String |  |
| getFilterClasses | String[] |  |
| getObjectName | ObjectName |  |
| getLoginTimeout | int |  |
| setDefaultTransactionIsolation | void |  |
| getCachedPreparedStatementCount | long |  |
| setDupCloseLogEnable | void |  |
| setLoginTimeout | void |  |
| getDefaultTransactionIsolation | Integer |  |
| isDupCloseLogEnable | boolean |  |
| setLogWriter | void |  |
| setDefaultReadOnly | void |  |
| getDriverClassLoader | ClassLoader |  |
| isDefaultAutoCommit | boolean |  |
| incrementExecuteCount | void |  |
| setTimeBetweenLogStatsMillis | void |  |
| setDriverClassName | void |  |
| setPassword | void |  |
| setTestWhileIdle | void |  |
| getName | String |  |
| getExecuteCount2 | long |  |
| setUseUnfairLock | void |  |
| isInitGlobalVariants | boolean |  |
| addFilters | void |  |
| isTestWhileIdle | boolean |  |
| isFailContinuous | boolean |  |
| setMaxIdle | void |  |
| isInitExceptionThrow | boolean |  |
| setUrl | void |  |
| setTestOnReturn | void |  |
| getRawJdbcUrl | String |  |
| isTestOnReturn | boolean |  |
| getExecuteQueryCount | long |  |
| getTransactionQueryTimeout | int |  |
| getUrl | String |  |
| setTestOnBorrow | void |  |
| getLastCreateErrorTime | Date |  |
| setInitGlobalVariants | void |  |
| isTestOnBorrow | boolean |  |
| getLastCreateErrorTimeMillis | long |  |
| getExecuteBatchCount | long |  |
| setAccessToUnderlyingConnectionAllowed | void |  |
| setConnectionErrorRetryAttempts | void |  |
| getLastErrorTime | Date |  |
| getMaxActive | int |  |
| getLastErrorTimeMillis | long |  |
| setConnectProperties | void |  |
| getCreateErrorCount | long |  |
| getLastError | Throwable |  |
| setTimeBetweenEvictionRunsMillis | void |  |
| getClosedPreparedStatementCount | long |  |
| setUseOracleImplicitCache | void |  |
| clearFilters | void |  |
| setConnectionProperties | void |  |
| isUseOracleImplicitCache | boolean |  |
| isFailFast | boolean |  |
| setFailFast | void |  |
| getOnFatalErrorMaxActive | int |  |
| setOnFatalErrorMaxActive | void |  |
| isOnFatalError | boolean |  |
| setInitExceptionThrow | void |  |




