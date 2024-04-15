# Async-Await

function getDeta(data) {
    return new Promise((reselve, reject)=>{
        setTimeout(() => {
            console.log('data = ' + data);
            reselve("success")
        }, 2000);
    });
};

async function getAllDeta() {
    await getDeta('one');
    await getDeta('two');
    await getDeta('three');

};
getAllDeta();
