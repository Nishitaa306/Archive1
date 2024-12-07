<h1>For postgre sql</h1>
\c cis_audit;

\dn

\dt public.*

ALTER SCHEMA public OWNER TO cis_audit_user;

GRANT USAGE ON SCHEMA public TO cis_audit_user;
GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public TO cis_audit_user;
GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA public TO cis_audit_user;
ALTER DEFAULT PRIVILEGES IN SCHEMA public GRANT ALL ON TABLES TO cis_audit_user;
ALTER DEFAULT PRIVILEGES IN SCHEMA public GRANT ALL ON SEQUENCES TO cis_audit_user;
