var mysql = require('mysql');

var con = mysql.createConnection({
    host: '157.245.58.124',
    user: 'shibly_user',
    password: 'Shibly@159',
    database: 'shibly_test_db'
});


con.connect(function(err) {
  if (err) throw err;
  console.log("Connected!");

});


const timestamp = Math.round(new Date() / 1000); 

  //Insert a record in the "customers" table:
  var sql = "INSERT INTO generator_monitoring2 (device_id, dev_status,start_time,end_time,dev_time,total_time) VALUES ('0001', 0,'"+timestamp+"','"+timestamp+"',0,1)";
  con.query(sql, function (err, result) {
    if (err) throw err;
    console.log("1 record inserted");
  });


  var sql = "INSERT INTO generator_monitoring2 (device_id, dev_status,start_time,end_time,dev_time,total_time) VALUES ('0002', 0,'"+timestamp+"','"+timestamp+"',0,1)";
  con.query(sql, function (err, result) {
    if (err) throw err;
    console.log("1 record inserted");
  });

  var sql = "INSERT INTO generator_monitoring2 (device_id, dev_status,start_time,end_time,dev_time,total_time) VALUES ('0003', 0,'"+timestamp+"','"+(timestamp+1)+"',0,1)";
  con.query(sql, function (err, result) {
    if (err) throw err;
    console.log("1 record inserted");
  });

