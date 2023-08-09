# aug9
[3:09 pm, 08/08/2023] Sowzzz Rv: 2)mysql> select u.uadd from user u,installs i,panel p where u.uno=i.uno and p.pvno=i.pvno and p.capacity=(select max(capacity) from panel p);

3)select u.uadd from user u,installs i,panel p where u.uno=i.uno and p.pvno=i.pvno and p.pvtype='monocrystalline';
[3:14 pm, 08/08/2023] Sowzzz Rv: 6)select p.pvtype,sum(i.charge)/(select count(*) from installs i where itype=’commercial’)from panel p,installs i where i.pvno=p.pvno and itype=’commercial’ group by p.pvtype;
[3:17 pm, 08/08/2023] Sowzzz Rv: 5)mysql> SELECT d.dname, COUNT(d.tin_no)
    -> FROM distributor d
    -> JOIN installs i ON d.tin_no = i.tin_no
    -> JOIN panel p ON p.pvno = i.pvno
    -> WHERE i.idate = (SELECT MIN(idate) FROM installs)
    -> GROUP BY d.dname;
[3:31 pm, 08/08/2023] Sowzzz Rv: 1)mysql> select count(p.pvno),d.tin_no from panel p,distributor d,installs i where i.pvno=p.pvno and i.tin_no=d.tin_no and i.itype='domestic' group by d.tin_no limit 1;
