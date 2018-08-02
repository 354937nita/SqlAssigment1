
--query 1.

select ename||','||''||job"Employee and Title" from emp;
--query 2.

select empno||','||ename||','||job||','||mgr||','||hiredate||','||sal||','||comm||','||deptno "THE_OUTPUT" from emp;
--query 3.

select ename,sal from emp where sal>2000 and sal<5000;
--query 4.

select ename,job,hiredate from emp where HIREDATE between '20-feb-98' and '1-may-98';
--query 5.

select ename,deptno from emp where deptno in (20,50);

--query 6.

select ename,job from emp where mgr is null;

--query 7.

select ename,sal,comm from emp where comm is not null order by sal desc, comm desc;

--query 8.

select empno,ename,sal, round(sal+sal*155)"NEW SALARY" from emp ;

--query 9.

select empno,ename,sal, round(sal+sal*155-sal)"INCREASE" from emp ;


--query 10.

select initcap(ename)"INITIAL_CAP",lengTH(ename)"LENGTH" from emp where ENAME like 'J%' or ENAME like 'A%' or ENAME like 'M%' ;

--query 11.

select distinct job,loc, dept.deptno from emp, dept where emp.deptno=dept.deptno and dept.deptno=20;

--query 12.

select ename, dept.DNAME from emp, dept where emp.deptno=dept.deptno and  ename like '%a%' ;

--query 13.

select ename, job,dept.deptno,dept.DNAME from emp, dept where emp.deptno=dept.deptno and loc='TORONTO';
--query 14.

select e.deptno Department,e.ename Employee, m.ename Colleague from emp e join emp m on (e.deptno=m.deptno) where (e.empno<>m.empno) order by e.deptno,e.empno,m.empno;

--query 15.

select e.ename"Employee",e.hiredate"Emp Hired", m.ename "Manager",m.hiredate"Mgr_Hired" from emp e join emp m on (e.empno<>m.empno) where e.hiredate<m.hiredate;

--query 16.

select round(max(sal))"Maximum",round(min(sal))"Minimum",round(sum(sal))"Sum",round(avg(sal))"Average" from emp;

--query 17.
select count(mgr) from emp;

--query 18.
select count(*)TOTAL ,SUM(DECODE(TO_CHAR(hiredate,'YYYY'),1995,1,0))"1995",SUM(DECODE(TO_CHAR(hiredate,'YYYY'),1996,1,0))"1996",SUM(DECODE(TO_CHAR(hiredate,'YYYY'),1997,1,0))"1997",SUM(DECODE(TO_CHAR(hiredate,'YYYY'),1998,1,0))"1998" from emp;

--query 19.
select JOB,sum(decode(deptno,20,sal))"DEPT 20",sum(decode(deptno,80,sal))"DEPT 80",sum(decode(deptno,90,sal))"DEPT 90",sum(sal)"Total"  from emp GROUP BY JOB;

--query 20.
select distinct e.eNAME,e.empno from emp e, emp d where e.deptno=d.deptno and e.ename like '%U%';

--query 21.
select eNAME,deptno,sal from emp where (deptno,sal) in (select deptno,sal from emp where comm is not null);

--query 22.
select eNAME,hiredate,sal from emp where (sal,comm)=(select sal,comm from emp where ename LIKE 'KOCHHAR');

--query 23.
select empno"EMPLOYEE_ID",ename"LAST_NAME",sal"SALARY" from emp where sal>(select avg(sal) from emp) order by sal;



